<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <title>FinFit 프로젝트 소개</title>
  <style>
    body {
      font-family: 'Arial', sans-serif;
      line-height: 1.8;
      background: #f7f9fa;
      color: #222;
      padding: 2rem;
      max-width: 900px;
      margin: auto;
    }
    h1, h2 {
      color: #1e88e5;
    }
    h1 {
      text-align: center;
      margin-bottom: 2rem;
    }
    section {
      margin-bottom: 2.5rem;
    }
    table {
      border-collapse: collapse;
      width: 100%;
      margin-top: 1rem;
    }
    table, th, td {
      border: 1px solid #ccc;
    }
    th, td {
      padding: 0.6rem;
      text-align: center;
    }
    code {
      background: #eee;
      padding: 0.2rem 0.4rem;
      border-radius: 4px;
    }
  </style>
</head>
<body>

  <h1>FinFit - 개인 맞춤형 스마트 헬스케어 시스템</h1>

  <section>
    <h2>1. 서비스 소개 (개요)</h2>
    <p>
      FinFit은 건강검진 데이터를 기반으로 질병 예측, 체형 분석, 운동 추천, 병원 매칭, 우울증 예측 등 다양한 건강 서비스를 통합 제공하는 Flask 기반 웹 애플리케이션입니다.
    </p>
  </section>

  <section>
    <h2>2. 주요 기능 및 담당 업무</h2>
    <table>
      <tr>
        <th>기능</th>
        <th>설명</th>
        <th>담당자</th>
      </tr>
      <tr>
        <td>질병 예측</td>
        <td>건강정보 기반 당뇨/고혈압/고지혈증 예측 및 시각화</td>
        <td>전체</td>
      </tr>
      <tr>
        <td>병원 추천</td>
        <td>예측 결과 기반 지역 병원 추천</td>
        <td>전체</td>
      </tr>
      <tr>
        <td>우울증 예측</td>
        <td>PHQ-9 설문 기반 우울 단계 예측</td>
        <td>전체</td>
      </tr>
      <tr>
        <td>체형 분석 및 운동 추천</td>
        <td>BMI 기반 체형 예측 + 운동 영상 추천</td>
        <td>Mia</td>
      </tr>
      <tr>
        <td>운동 자세 교정</td>
        <td>Webcam 기반 실시간 스쿼트 자세 분석</td>
        <td>Michael</td>
      </tr>
      <tr>
        <td>챗봇 (Fit봇)</td>
        <td>페이지별 기능 설명 및 사용자 가이드</td>
        <td>전체</td>
      </tr>
    </table>
  </section>

  <section>
    <h2>3. 프로젝트 목표</h2>
    <ul>
      <li>AI 기반 건강 예측 및 분석 시스템 구현</li>
      <li>운동 영상 추천 + 자세 분석 기능 통합</li>
      <li>지역 기반 병원 매칭 기능 연계</li>
      <li>챗봇을 통한 사용자 친화적 UX 제공</li>
    </ul>
  </section>

  <section>
    <h2>4. 프로젝트 진행 관리</h2>
    <ul>
      <li>관리 툴: Notion + GitHub Projects</li>
      <li>브랜치 전략: <code>main</code>, <code>develop</code>, <code>feature/*</code></li>
      <li>일정: 기능 단위 마일스톤 + 주간 회고</li>
    </ul>
  </section>

  <section>
    <h2>5. 스킬 앤 툴스</h2>
    <ul>
      <li><strong>Frontend:</strong> HTML, CSS, Bootstrap, JavaScript, Jinja2</li>
      <li><strong>Backend:</strong> Python, Flask, Flask-Restful</li>
      <li><strong>AI/ML:</strong> Scikit-learn, XGBoost, LightGBM, CatBoost</li>
      <li><strong>시각화:</strong> Matplotlib, Plotly, conic-gradient</li>
      <li><strong>기타:</strong> OpenCV, Mediapipe, Naver Map API, Web Speech API</li>
    </ul>
  </section>

  <section>
    <h2>6. 데이터 흐름도 / 사용자 흐름도</h2>
    <ul>
      <li>사용자 정보 입력 → BMI 계산 → 질병/우울증 예측 → 운동/병원 추천</li>
      <li>예측 결과 → 시각화 및 챗봇 안내 → 맞춤형 건강 루틴 제공</li>
    </ul>
  </section>

  <section>
    <h2>7. 계층 구조 (Flask 기반)</h2>
    <pre>
FinFit/
├── templates/
│   ├── main.html, exercise.html, ...
├── static/
│   └── css,
