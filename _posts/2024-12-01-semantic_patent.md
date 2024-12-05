---
title: "의미기반 유사특허 검색시스템"
date: 2023-02-22
categories: [Projects, AI]
tags: [Flask, Dash, PostgreSQL, 특허검색, 데이터시각화, 대시보드, 데이터베이스]
---

<div class="project-container">
  <div class="project-section info-section">
    <h2>프로젝트 소개</h2>
    <div class="project-info">
      <img src="assets/img/semantic/semantic-main.png" alt="의미기반 유사특허 검색시스템 메인화면">
      <p>
        대학 및 출연(연)과 기술 수요기업 간 공공기술의 기술이전 과정에서 발생하는<br>
        특허 검색의 한계를 개선하고, 특허 분석 프로세스를 효율화하기 위한 의미기반 검색시스템입니다.
      </p>
      <strong>Github</strong> Private Repository<br>
      <strong>개발 기간</strong> 2023.01 - 2023.02 (2개월)<br>
      <strong>인원</strong> 2명<br>
      <strong>역할</strong> 데이터분석 인턴<br>
      <strong>기여도</strong> 80%<br>
      <strong>개발환경</strong> NVIDIA GeForce RTX 3090 32GB<br>
      <strong>기술 스택</strong>
      <div class="tech-badges">
        <div class="badge-group">
          <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
          <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" alt="PyTorch">
          <img src="https://img.shields.io/badge/Faiss-00A1EA?style=for-the-badge&logo=Faiss&logoColor=white" alt="Faiss">
        </div>
        <div class="badge-group">
          <img src="https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white" alt="Flask">
          <img src="https://img.shields.io/badge/Dash-008DE4?style=for-the-badge&logo=dash&logoColor=white" alt="Dash">
          <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL">
        </div>
      </div>
    </div>
  </div>

  <div class="project-section main-features">
    <h2>주요 구현 기능</h2>
    <div class="features-tabs">
      <div class="tab-buttons">
        <button class="tab-button active" data-tab="feature1"><strong>의미기반 검색시스템</strong></button>
        <button class="tab-button" data-tab="feature2"><strong>Interactive 시각화</strong></button>
      </div>
      <div class="tab-content active" id="feature1">
        <div class="feature-item">
          <h3>1. 의미기반 유사특허 검색시스템</h3>
          <div class="section-content">
            <div class="tech-badges">
              <div class="badge-group">
                <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" alt="PyTorch">
                <img src="https://img.shields.io/badge/Faiss-00A1EA?style=for-the-badge&logo=Faiss&logoColor=white" alt="Faiss">
              </div>
            </div>
            <h3>주요 기능</h3>
            <ul class="feature-list">
              <li><strong>S-BERT 모델</strong> 기반의 문장 임베딩 시스템 구축</li>
              <li>특허명과 요약문에 대한 <strong>개별 유사도 측정</strong> 및 <strong>가중치 기반 통합 검색</strong></li>
              <li>약 <strong>158만건</strong>의 KIPRIS 특허 서지정보 기반 <strong>Vector DB</strong> 구축</li>
            </ul>
            <img src="assets/img/semantic/sbert.png" alt="의미기반 유사특허 검색시스템 SBERT">
            <img src="assets/img/semantic/semantic-ir-arch.png" alt="의미기반 유사특허 검색시스템 검색시스템 아키텍처">
            <h3>Technical Challenges & Solutions</h3>
            <ul class="feature-list">
              <li>
                <strong>도메인 특화 모델 개발</strong><br><br>
                특허 문서는 전문적인 용어와 복잡한 기술 설명이 많아 일반적인 언어 모델로는 정확한 의미 파악이 어렵습니다.
                이를 해결하기 위해 <strong>KorNLI, KorSTS 데이터셋</strong>으로 사전 학습된 S-BERT 모델에 <strong>Domain Adaptation</strong> 기법을 적용했습니다.<br><br>
                특허 문서의 특성을 반영하여 특허명과 요약문에 대해 각각 다른 가중치를 적용하는 통합 검색 방식을 구현했습니다.
                이를 통해 키워드 기반 검색에서 발생하던 세부 기술 내용 불일치 문제를 해결했습니다.<br><br>
                그 결과 검색 시간이 평균 <strong>1분 34초에서 58초로 단축</strong>되었고, 검색 정확도도 크게 향상되었습니다.
              </li>
            </ul>
          </div>
        </div>
      </div>
      <div class="tab-content" id="feature2">
        <div class="feature-item">
          <h3>2. Interactive 시각화 API</h3>
          <div class="section-content">
            <div class="tech-badges">
              <div class="badge-group">
                <img src="https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white" alt="Flask">
                <img src="https://img.shields.io/badge/Dash-008DE4?style=for-the-badge&logo=dash&logoColor=white" alt="Dash">
                <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL">
              </div>
            </div>
            <h3>주요 기능</h3>
            <ul class="feature-list">
              <li><strong>특허평가 지수</strong> 시각화 대시보드 구현</li>
              <li>유사 특허 간 <strong>객관적 비교 및 평가</strong> 기능</li>
              <li>직관적인 <strong>특허 선별 인터페이스</strong> 제공</li>
            </ul>
            <img src="assets/img/semantic/result1.png" alt="의미기반 유사특허 검색시스템 검색결과1">
            <img src="assets/img/semantic/result2.png" alt="의미기반 유사특허 검색시스템 검색결과2">
            <h3>Technical Challenges & Solutions</h3>
            <ul class="feature-list">
              <li>
                <strong>대규모 데이터 시각화 최적화</strong><br><br>
                <strong>158만건</strong>의 특허 데이터를 실시간으로 처리하고 시각화하는 과정에서 성능 이슈가 발생했습니다.
                특히 유사도 기반 그래프 생성 시 렌더링 시간이 길어지는 문제가 있었습니다.<br><br>
                이를 해결하기 위해 <strong>PostgreSQL 인덱싱을 최적화</strong>하고, <strong>Dash의 캐싱 기능</strong>을 활용했습니다.
                또한 필요한 데이터만 선택적으로 로드하는 방식을 적용하여 시각화 성능을 개선했습니다.<br><br>
                그 결과 관련특허 조사 연구원 15명을 대상으로 한 설문에서 <strong>검색 결과의 정확성, 속도, 
                업무 적용 가능성</strong> 등에서 <strong>80% 이상의 긍정적인 평가</strong>를 받았습니다.
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="project-section achievements">
    <h2>프로젝트 성과</h2>
    <ul class="feature-list">
      <li>검색 시간 <strong>62% 단축</strong> (평균 1분 34초 → 58초)</li>
      <li>관련특허 조사 연구원 15명 대상 설문 결과 <strong>80% 이상 긍정적 평가</strong></li>
      <li><strong>키워드 기반 검색의 한계를 극복</strong>한 의미기반 검색 시스템 구축</li>
      <li><strong>특허 분석 프로세스 효율화</strong> 달성</li>
    </ul>
  </div>
</div>

<script src="/assets/js/projects.js"></script>