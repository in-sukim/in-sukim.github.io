---
title: "웹페이지 관리자 대시보드"
date: 2023-12-24
categories: [Projects, Data Analytics]
tags: [대시보드, 데이터시각화, 데이터베이스, 웹개발, 실시간데이터, 검색분석, PostgreSQL, Tableau]
---

<div class="project-container">
  <div class="project-section info-section">
    <h2>프로젝트 소개</h2>
    <div class="project-info">
      <img src="assets/img/interactive/interactive-main.png" alt="웹페이지 관리자 대시보드 메인화면" style="width: 70%; height: 70%; display: block; margin: 20px auto;">
      <p>
        웹사이트 방문자 검색어 및 기업데이터에 대한 관리자 통계 대시보드를 구축하여,<br>
        데이터 기반의 의사결정을 지원하는 프로젝트입니다.
      </p>
      <strong>개발 기간</strong> 2023.12(3주)<br>
      <strong>인원</strong> 2명<br>
      <strong>역할</strong> 데이터 분석가<br>
      <strong>개발환경</strong> Window 10<br>
      <strong>기술 스택</strong>
      <div class="tech-badges">
        <div class="badge-group">
          <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" alt="PostgreSQL">
          <img src="https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=tableau&logoColor=white" alt="Tableau">
        </div>
      </div>
    </div>
  </div>

  <div class="project-section main-features">
    <h2>주요 구현 기능</h2>
    <div class="features-tabs">
      <div class="tab-buttons">
        <button class="tab-button active" data-tab="feature1"><strong>검색어 분석 대시보드</strong></button>
        <button class="tab-button" data-tab="feature2"><strong>데이터베이스 통합 관리</strong></button>
      </div>
      <div class="tab-content active" id="feature1">
        <div class="feature-item">
          <h3>1. 사이트 사용자 현황 대시보드</h3>
          <div class="section-content">
            <h3>주요 기능</h3>
            <ul class="feature-list">
              <li><strong>전체 내부망 데이터베이스 연동</strong>
                <ul>
                  <li><strong>사용자 검색 기록 실시간 수집</strong></li>
                  <li><strong>검색어 통계 자동 업데이트</strong></li>
                </ul>
              </li>
              <li><strong>필터 조건 적용</strong>
                <ul>
                  <li><strong>필터 기능</strong>을 통한 <strong>데이터 특정 조건 조회</strong></li>
                </ul>
              </li>
            </ul>
            <div class="image-slider">
              <button class="slider-button prev">&#10094;</button>
              <div class="slider-container">
                <div class="slider-track">
                  <div class="slide">
                    <img src="assets/img/interactive/inter-dashboard1.png" alt="웹페이지 관리자 대시보드 대시보드1">
                  </div>
                  <div class="slide">
                    <img src="assets/img/interactive/inter-dashboard2.png" alt="웹페이지 관리자 대시보드 대시보드2">
                  </div>
                  <div class="slide">
                    <img src="assets/img/interactive/inter-dashboard3.png" alt="웹페이지 관리자 대시보드 대시보드3">
                  </div>
                  <div class="slide">
                    <img src="assets/img/interactive/inter-dashboard4.png" alt="웹페이지 관리자 대시보드 대시보드4">
                  </div>
                </div>
              </div>
              <button class="slider-button next">&#10095;</button>
            </div>
          </div>
        </div>
      </div>
      <div class="tab-content" id="feature2">
        <div class="feature-item">
          <h3>2. 검색어 분석 대시보드</h3>
          <div class="section-content">
            <h3>주요 기능</h3>
            <ul class="feature-list">
              <li><strong>전체 내부망 데이터베이스 연동</strong>
                <ul>
                  <li><strong>사용자 검색 기록 실시간 수집</strong></li>
                  <li><strong>검색어 통계 자동 업데이트</strong></li>
                </ul>
              </li>
              <li><strong>검색어 패턴 분석</strong>
                <ul>
                  <li><strong>시간대별 검색량 추이</strong> 시각화</li>
                  <li><strong>워드클라우드</strong>를 통한 <strong>인기 검색어</strong> 시각화</li>
                  <li><strong>관련 특허 정보</strong> 연계 표시</li>
                </ul>
              </li>
            </ul>
            <div class="image-slider">
              <button class="slider-button prev">&#10094;</button>
              <div class="slider-container">
                <div class="slider-track">
                  <div class="slide">
                    <img src="assets/img/interactive/inter-keyword.png" alt="웹페이지 관리자 대시보드 검색어1">
                  </div>
                  <div class="slide">
                    <img src="assets/img/interactive/inter-keyword2.png" alt="웹페이지 관리자 대시보드 검색어2">
                  </div>
                </div>
              </div>
              <button class="slider-button next">&#10095;</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="project-section info-section">
    <h2>Technical Challenges & Solutions</h2>
    <div class="section-content">
      <ul class="feature-list">
        <li><strong>데이터 실시간성 문제</strong><br><br>
          <strong>내부망 데이터베이스</strong>의 데이터를 대시보드에 <strong>실시간</strong>으로 반영해야 했습니다. 초기에는 대시보드에서 사용되는 데이터들을 
          <strong>개별 SQL 쿼리</strong>로 연결하여 <strong>수동으로 업데이트</strong>하는 방식을 사용했으나, 이는 <strong>시스템 부하</strong>가 크고 <strong>실시간성</strong>이 떨어지는 
          문제가 있었습니다.<br><br>
          이를 해결하기 위해 <strong>Tableau Server</strong>를 도입하여 <strong>데이터 실시간 업데이트 파이프라인</strong>을 구축했습니다. 
          대시보드에서 사용되는 데이터들은 모두 <strong>사용자 지정 SQL 쿼리</strong>로 연결하고, 정리된 데이터셋을 모두 Tableau Server에 
          업로드하여 대시보드의 <strong>실시간 업데이트</strong>를 구현했습니다.
        </li>
        <li><strong>데이터 품질 관리</strong><br><br>
          다양한 소스에서 수집된 데이터의 <strong>품질 관리</strong>가 필요했습니다. 특히 검색어 데이터에서 <strong>특수문자, 공백</strong> 등으로 인한
          <strong>데이터 불일치</strong> 문제가 발생했습니다.<br><br>
          <strong>PostgreSQL</strong>의 <strong>정규식 함수</strong>를 활용하여 <strong>데이터 전처리 파이프라인</strong>을 구축했고, 이를 통해 <strong>데이터 정합성</strong>을 확보했습니다.
        </li>
      </ul>
    </div>
  </div>

  <div class="project-section info-section">
    <h2>주요 성과</h2>
    <div class="section-content">
      <ul class="feature-list">
        <li><strong>키워드 검색 로그</strong> <strong>241,490건</strong> 데이터 처리</li>
        <li><strong>데이터 업데이트 시간</strong> <strong>90% 단축</strong> (<strong>수동 30분 → 자동 3분</strong>)</li>
        <li><strong>관리자 검색어 분석 시간</strong> <strong>75% 절감</strong></li>
        <li><strong>회사 내부망 홈페이지</strong> 반영, <strong>플랫폼 데이터 관리 대시보드</strong> 구축</li>
      </ul>
    </div>
  </div>
</div>

<script src="/assets/js/projects.js"></script>