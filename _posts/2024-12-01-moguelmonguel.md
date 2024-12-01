---
title: 몽글몽글
date: 2024-10-14
categories: [Projects, AI]
tags: [anomaly-detection, deep-learning]
---


<div class="project-container">
  <div class="project-section info-section">
    <h2>프로젝트 정보</h2>
    <div class="project-info">
      <img src="assets/img/main-page.png" alt="몽글몽글 메인 페이지">
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
              <li><strong>이미지 텍스트 추출</strong>: <strong>EasyOCR</strong>과 <strong>Pororo</strong> 모델을 결합하여 <strong>한글 텍스트 인식률 개선</strong></li>
              <li><strong>텍스트 교정 및 재구성</strong>: <strong>GPT-4o</strong>를 활용한 OCR 결과물 후처리
                <ul>
                  <li>오타 및 띄어쓰기 교정</li>
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
            <h3>성과</h3>
            <ul class="feature-list">
              <li><strong>OCR</strong>과 <strong>LLM</strong>의 결합으로 <strong>텍스트 추출 성능 개선</strong></li>
              <li>구조가 다양한 가정통신문에서도 <strong>필요한 정보 정확하게 추출</strong>하는 시스템 구현</li>
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
  <img src="assets/img/infra.png" alt="몽글몽글 인프라 구조도">
  <img src="assets/img/system.png" alt="몽글몽글 시스템 아키텍처">
</div>

<script src="/assets/js/projects.js"></script>
