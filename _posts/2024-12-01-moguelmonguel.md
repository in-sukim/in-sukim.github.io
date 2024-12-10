---
title: 몽글몽글
date: 2024-10-14
categories: [Projects, AI]
tags: [FastAPI, LangChain, Milvus, PostgreSQL, OCR, GPT-4, 텍스트처리, AI서비스]
---

<div class="project-container">
  <div class="project-section info-section">
    <h2>프로젝트 소개</h2>
    <div class="project-info">
      <img src="assets/img/mong/main-page.png" alt="몽글몽글 메인 페이지">
      <p>
        어린이집 일정, 준비물 등 매일 쏟아지는 정보를 손쉽게 기록-관리하여,
        바쁜 일상 속 아이의 소중한 순간을 간직할 수 있도록 지원하는 AI 기반 육아 지원 서비스입니다.
      </p>
      <strong>Github</strong> <a href="https://github.com/in-sukim/Mongeul-ML">Link</a><br>
      <strong>개발 기간</strong> 2024.8.9 ~ 2024.10.14<br>
      <strong>인원</strong> 6명(FE:2, BE:2, AI:2)<br>
      <strong>역할</strong> AI 엔지니어<br>
      <strong>개발환경</strong> Window 10(WSL2 Ubuntu)<br>
      <strong>기술 스택</strong>
      <div class="tech-badges">
        <div class="badge-group">
          <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
          <img src="https://img.shields.io/badge/langchain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white" alt="langchain">
          <img src="https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white" alt="OpenAI">
          <img src="https://img.shields.io/badge/EasyOCR-2496ED?style=for-the-badge&logoColor=white" alt="EasyOCR">
          <img src="https://img.shields.io/badge/Pororo-FF6F00?style=for-the-badge&logoColor=white" alt="Pororo">
          <img src="https://img.shields.io/badge/DALL--E--3-412991?style=for-the-badge&logo=openai&logoColor=white" alt="DALL--E--3">
        </div>
        <div class="badge-group">
          <img src="https://img.shields.io/badge/Milvus-00A1EA?style=for-the-badge&logo=Milvus&logoColor=white" alt="Milvus">
          <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL">
          <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI">
          <img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" alt="Linux">
          <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker">
          <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git">
        </div>
      </div>
    </div>
  </div>

  <div class="project-section main-features">
    <h2>주요 구현 기능</h2>
    <div class="features-tabs">
      <div class="tab-buttons">
        <button class="tab-button active" data-tab="feature1"><strong>스마트 일정 관리</strong></button>
        <button class="tab-button" data-tab="feature2"><strong>내 아이 하루 동화</strong></button>
        <button class="tab-button" data-tab="feature3"><strong>대화형 AI 일기</strong></button>
      </div>
      <div class="tab-content active" id="feature1">
        <div class="feature-item">
          <h3>1. 스마트 일정 관리</h3>
          <div class="section-content">
            <div class="tech-badges">
              <div class="badge-group">
                <img src="https://img.shields.io/badge/OCR-2496ED?style=for-the-badge&logoColor=white" alt="OCR">
                <img src="https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white" alt="OpenAI">
                <img src="https://img.shields.io/badge/langchain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white" alt="langchain">
                <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI">
              </div>
            </div>
            <h3>주요 기능</h3>
            <ul class="feature-list">
              <li><strong>이미지 텍스트 추출</strong>: <strong>EasyOCR</strong>과 <strong>Pororo</strong> OCR 결과 <strong>GPT-4</strong>를 통해 텍스트 교정 및 재구성<br></li>
              <li><strong>텍스트 교정 및 재구성</strong>: <strong>GPT-4o</strong>를 활용한 OCR 결과물 후처리
                <ul>
                  <li><strong>오타 및 띄어쓰기 교정</strong></li>
                  <li><strong>한글 텍스트 인식률 개선</strong></li>
                  <li><strong>문맥</strong>을 고려한 <strong>텍스트 재구성</strong></li>
                </ul>
              </li>
              <li><strong>메타데이터 추출</strong>: <strong>JsonOutputParser</strong>를 통한 <strong>구조화된 데이터 추출</strong>
                <ul>
                  <li>일정, 준비물, 장소 등 <strong>주요 정보 자동 분류</strong></li>
                  <li><strong>캘린더 연동</strong>을 위한 데이터 포맷 변환</li>
                </ul>
              </li>
            </ul>
            <h3>Technical Challenges & Solutions</h3>
            <ul class="feature-list">
              <li>
                <strong>OCR 정확도 문제</strong><br><br>
                오픈소스 OCR Tesseract, EasyOCR, Pororo 모델들의 한국어 텍스트 인식 성능이 낮아 LLM을 통해 일정정보를 추출한 결과를 정성 평가했을 때 행사명, 날짜, 장소 등 주요 정보에 오타가 있는 채로 추출하는 등의 문제가 있었습니다.<br><br>
                프로젝트 개발 일정과 환경을 고려하여 OCR 모델의 파인튜닝은 따로 진행하지 않고, EasyOCR, Pororo 모델 결과를 병합하여 LLM을 통해 재구성 및 오타 교정을 하는 BettorOCR 라이브러리를 이용하였습니다.<br><br>
                일정정보를 추출할 수 없는 관련 없는 문서를 판단할 수 있도록 프롬프트 지시사항을 추가하고, 오타 교정 및 문맥 고려한 텍스트 재구성을 진행하였습니다. <br><br>그 결과 OCR 결과 한국어 인식성능이 크게 개선되었고, 추출된 일정정보 정량분석 결과 또한 큰 개선을 이루었습니다.
              </li>
              <li>
                <strong>메타데이터 추출 정확도</strong><br><br>
                가정통신문에는 다양한 정보가 있습니다. 그 중 저희가 추출하고자 했던 정보는 일정, 준비물, 장소 등이었습니다. 하지만 가정통신문의 형태가 다양하여 필수 정보를 잘 추출하지 못하고, 시간 정보의 형식이 매번 다르게 추출이 되어 벡엔드 API 스키마에 맞지 않는 문제가 발생하였습니다.<br><br>
                이 문제들을 해결하기 위해 커스텀 프롬프트 템플릿을 설계하고, 구조화된 데이터 추출을 위한 JsonOutputParser를 통해 필수 정보를 추출하는 시스템을 구축하였습니다.<br>
                주요 프롬프트 내용으로는 활동 추출 및 날짜별 그룹화, 날짜(시간) 형식 통일, 활동 정보 세부화(이름, 시작 및 종료 시간, 위치, 대상, 주요 정보 및 추가 설명) 등이 있습니다.<br><br>
                이를 통해 가정통신문으로부터 기억해야 할 정보를 추출, 변환하여 캘린더에 등록함으로써 사용자가 아이 관련하여 기억해야 할 정보를 쉽게 찾아볼 수 있도록 하였습니다.
              </li>
            </ul>
            <h3>성과</h3>
            <ul class="feature-list">
              <li><strong>OCR</strong>과 <strong>LLM</strong>의 결합으로 <strong>텍스트 추출 성능 개선</strong></li>
              <li>구조가 다양한 가정통신문에도 <strong>필요한 정보 정확하게 추출</strong>하는 시스템 구현</li>
            </ul>
            <div class="video-container">
              <video controls aria-label="몽글몽글 데모 영상">
                <source src="https://github.com/user-attachments/assets/c5ec79c8-9780-4ccc-828c-523d315ea3f0" type="video/mp4">
                <p>브라우저가 비디오를 지원하지 않습니다.</p>
              </video>
            </div>
          </div>
        </div>
      </div>
      <div class="tab-content" id="feature2">
        <div class="feature-item">
          <h3>2. 내 아이 하루 동화</h3>
          <div class="section-content">
            <div class="tech-badges">
              <div class="badge-group">
                <img src="https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white" alt="OpenAI">
                <img src="https://img.shields.io/badge/langchain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white" alt="langchain">
                <img src="https://img.shields.io/badge/Text2Image-40B5A4?style=for-the-badge&logo=Text2Image&logoColor=white" alt="Text2Image">
                <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI">
              </div>
            </div>
            <h3>주요 기능</h3>
            <ul class="feature-list">
              <li><strong>맞춤형 동화 생성</strong>: 아이의 일상을 동화로 재구성
                <ul>
                  <li><strong>사용자 입력 기반</strong> 스토리 생성</li>
                  <li><strong>연령대별 맞춤</strong> 어휘 및 문장 구조 적용</li>
                </ul>
              </li>
              <li><strong>이미지 생성 최적화</strong>: <strong>2x2 패널 분할 방식</strong> 적용
                <ul>
                  <li>장면 간 <strong>일관성</strong>을 위한 프롬프트 최적화</li>
                  <li><strong>4개 장면</strong>을 담은 패널 형식 이미지 생성</li>
                </ul>
              </li>
              <li><strong>스타일 일관성 유지</strong>: <strong>프롬프트 엔지니어링</strong> 고도화
                <ul>
                  <li><strong>캐릭터 특성 유지</strong>를 위한 프롬프트 템플릿 설계</li>
                  <li>캐릭터 및 그림체 <strong>일관성 개선</strong></li>
                </ul>
              </li>
            </ul>
            <h3>Technical Challenges & Solutions</h3>
            <ul class="feature-list">
              <li>
                <strong>연령별 맞춤형 스토리 생성</strong><br><br>
                아이의 연령에 따라 적절한 어휘 수준과 문장 구조를 적용하는 것이 중요했습니다. 또한 이미지 생성을 위한 프롬프트 또한 명확하게 설정해 줄 필요가 있었기 때문에 <a href="https://arxiv.org/pdf/2407.09467" target="_blank">선행 연구</a>를 참고하여 프롬프트를 설계하였습니다.<br>
                해당 논문의 주요 프롬프트 내용은 다음과 같습니다:
                <ul>
                  <li><strong>어휘 수준:</strong> 특정 연령대가 이해할 수 있는 포괄적인 언어 사용을 지정.</li>
                  <li><strong>서술 방식:</strong> 단순하고 명확한 단어를 사용하고, 복잡한 추론이 필요한 개념 지양.</li>
                  <li><strong>시각적 요소:</strong> 명확하게 그림으로 표현 가능한 대상과 상황만을 포함하도록 제한.</li>
                  <li><strong>정서적 측면:</strong> 긍정적인 표현을 사용하고 해피엔딩으로 마무리하도록 지정.</li>
                  <li><strong>내용 구성:</strong> 특정 요소에 초점을 맞추고 독자의 상상력을 자극하는 요소를 포함.</li>
                </ul>
                해당 프롬프트를 커스터마이징하여 아이 개인별 동화 내용을 생성하였습니다.
              </li>
              <br>
              <li>
                <strong>이미지 생성 최적화 문제</strong><br><br>
                기획한 동화 기능은 페이지별 텍스트,이미지로 이루어져야 했기 때문에 초기에는 각 장면마다 개별적으로 이미지를 생성하는 방식을 사용했습니다. 
                하지만 이 방식은 4개의 장면을 생성하는데 많은 시간이 소요되었고, API 호출 비용도 높았습니다. 또한 각 장면 간의 캐릭터 외형, 그림체 등의 일관성이 떨어지는 문제가 있었습니다.<br><br>
                처음 생성 동화 내용은 페이지 별 동화내용과 DALL-E 프롬프트의 형식으로 생성하였고, 페이지별 DALL-E 프롬프트를 통해 이미지를 생성하는 방식이었습니다. 그 결과 앞서 말한 문제점들이 발생하였습니다.<br><br>
                먼저 장면 간 캐릭터 외형, 그림체 일관성 문제를 해결하기 위해 등장인물 설명(이름, 외형적 특징)을 동화 내용 생성 시 포함하였고 페이지별 이미지 프롬프트에 주입하여 이미지를 생성하였습니다.<br>
                그 결과 일관성이 개선되었지만 여전히 만족하지 못할만한 수준이었습니다. <br>
                <div class="image-row" style="display: flex; justify-content: center; gap: 2px; margin: 20px 0;">
                  <img src="assets/img/mong/char_info_pic1.png" alt="등장인물 설명 추가 사진 1" style="width: auto; height: auto;">
                  <img src="assets/img/mong/char_info_pic2.png" alt="등장인물 설명 추가 사진 2" style="width: auto; height: auto;">
                  <img src="assets/img/mong/char_info_pic3.png" alt="등장인물 설명 추가 사진 3" style="width: auto; height: auto;">
                  <img src="assets/img/mong/char_info_pic4.png" alt="등장인물 설명 추가 사진 4" style="width: auto; height: auto;">
                </div>
                그 다음 시도한 방법은 2x2 패널 분할 방식입니다. 하나의 프롬프트로 4개의 장면이 포함된 이미지를 한 번에 생성 후 분할하는 방식입니다. 프롬프트 엔지니어링을 통해 각 패널의 장면을 명확히 구분하고, 캐릭터의 특성을 일관되게 유지하도록 했습니다.<br><br>
                그 결과 이미지 생성 횟수를 4장에서 1장으로 줄여 이미지 생성 비용 75%절감 및 생성 시간 87% 단축하였고, 캐릭터와 그림체의 일관성도 크게 개선되었습니다.
                <img src="assets/img/mong/panel-pic.png" alt="패널 분할 방식 사진" style="width: auto; height: auto;">
              </li>
            </ul>
            <h3>성과</h3>
            <ul class="feature-list">
              <li>이미지 생성 시간 <strong>87% 단축</strong></li>
              <li>비용 <strong>75% 절감</strong></li>
              <li>등장인물 및 그림 스타일 <strong>일관성 개선</strong></li>
            </ul>
            <div class="video-container">
              <video controls aria-label="몽글몽글 데모 영상">
                <source src="https://github.com/user-attachments/assets/52c45f1c-1f9f-47ec-90bc-951f1afb0d4e" type="video/mp4">
                <p>브라우저가 비디오를 지원하지 않습니다.</p>
              </video>
            </div>
          </div>
        </div>
      </div>
      <div class="tab-content" id="feature3">
        <div class="feature-item">
          <h3>3. 대화형 AI 일기 작성 도우미</h3>
          <div class="section-content">
            <div class="tech-badges">
              <div class="badge-group">
                <img src="https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white" alt="OpenAI">
                <img src="https://img.shields.io/badge/langchain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white" alt="langchain">
                <img src="https://img.shields.io/badge/Milvus-00A1EA?style=for-the-badge&logo=Milvus&logoColor=white" alt="Milvus">
                <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI">
                <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL">
              </div>
            </div>
            <h3>주요 기능</h3>
            <ul class="feature-list">
              <li><strong>ReAct 기반 대화 시스템</strong>: <strong>멀티턴 대화</strong> 지원
                <ul>
                  <li><strong>사용자 의도 파악</strong> 및 <strong>맥락 유지</strong></li>
                  <li><strong>예외 상황</strong> 자동 감지 및 대처</li>
                </ul>
              </li>
              <li><strong>지능형 작성 보조</strong>: <strong>Function Calling</strong> 활용
                <ul>
                  <li>대화를 통한 <strong>일기 작성 단계별 가이드</strong></li>
                  <li><strong>감정 분석</strong> 및 <strong>주요 키워드 추출</strong></li>
                  <li>맥락에 맞는 <strong>추가 질문 생성</strong></li>
                </ul>
              </li>
              <li><strong>하이브리드 검색 시스템</strong>
                <ul>
                  <li><strong>의미적 유사도</strong> 기반 검색</li>
                  <li><strong>LLM 생성 필터 표현식</strong>을 활용한 정확도 향상</li>
                </ul>
              </li>
            </ul>
            <h3>Technical Challenges & Solutions</h3>
            <ul class="feature-list">
              <li>
                <strong>대화 맥락 유지와 도구 활용</strong><br><br>
                일기 작성 과정에서 사용자와의 자연스러운 대화를 유지하면서, 필요한 시점에 적절한 도구(일기 작성/저장, 과거 정보 검색 등)를 활용해야 하는 문제가 있었습니다. 단순히 LLM의 응답만으로는 복잡한 작업 흐름을 처리하기 어려웠습니다.<br><br>
                이를 해결하기 위해 LangChain을 통해 ReAct Agent를 구현하였습니다. 에이전트는 사용자의 의도를 파악하고, 필요한 도구를 선택하여 작업을 수행하도록 설계했습니다. 특히 Function Calling을 통해 사용자에게 다양한 기능을 제공할 수 있게 했습니다.<br><br>
                그 결과 자연스러운 대화 흐름을 유지하면서도 사용자의 자연어 질의의 의도에 맞는 다양한 기능을 수행할 수 있게 되었습니다.<br><br>
              </li>
              <li>
                <strong>과거 정보 검색</strong><br><br>
                사용자가 과거 정보를 물어볼 때, "10일에 아이와 뭘 했지?"와 같은 질문에는 의미적 유사도 검색을 하기보다는 "10일"과 "아이와 부모가 함께 한 활동"과 같은 조건으로 필터를 적용하여 정보를 가져온다면 빠르게 정확한 정보를 찾을 수 있다고 판단하였습니다.<br><br>
                따라서 사용자가 과거 정보를 물어보는 의도일 때 LLM 기반으로 필터 표현식을 생성하고 결합하여 Vector Search에 적용하였습니다.<br><br>
                그 결과 사용자 질의에 특정한 조건이 있을 경우 빠른 검색 속도를 보장하고 적절한 정보를 검색할 수 있었습니다.
              </li>
            </ul>
            <h3>성과</h3>
            <ul class="feature-list">
              <li><strong>대화 맥락</strong>을 이해하고 일기 작성과 저장, 과거 기록 참조 등 필요한 도구를 선택하여 활용하는 <strong>에이전트 시스템</strong> 구현</li>
            </ul>
            <div class="video-container">
              <video controls aria-label="몽글몽글 데모 영상">
                <source src="https://github.com/user-attachments/assets/864f88d2-6bf7-449f-b9ec-2d733ff546d0" type="video/mp4">
                <p>브라우저가 비디오를 지원하지 않습니다.</p>
              </video>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<div class="architecture-diagram">
  <img src="assets/img/mong/infra.png" alt="몽글몽글 인프라 구조도">
  <img src="assets/img/mong/system.png" alt="몽글몽글 시스템 아키텍처">
</div>

<script src="/assets/js/projects.js"></script>


