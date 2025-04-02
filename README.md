<small>

# ■ FinFit - 개인 맞춤형 헬스케어 서비스 💪

FinFit은 건강 검진 데이터와 AI 예측 모델을 활용하여 사용자의 건강 상태를 정밀 분석하고 맞춤형 솔루션을 제공하는 스마트 헬스케어 서비스를 제공합니다. 또한, 바쁜 현대인을 위해 생활 습관 개선부터 병원 연계까지 체계적인 건강 관리 시스템을 제공하여, 누구나 쉽게 건강을 유지하고 더 나은 미래를 준비할 수 있도록 지원합니다. <br>

<table>
  <thead>
    <tr>
      <th>항목</th>
      <th>내용</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>개발 기간 🗓️</td>
      <td>
        2025년 2월 24일(월) ~ 2025년 4월 1일(화)
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      </td>
    </tr>
    <tr>
      <td>프로젝트 목표</td>
      <td>
        - AI 질병 예측과 그래프로 보는 건강 분석<br>
        - 질병 별 위치기반 병원 매칭 서비스<br>
        - 체형 분석을 통한 건강 맞춤 운동 솔루션 제공<br>
        - 검진 데이터 기반 우울증 예측 및 맞춤 정보 제공<br>
        - AI 분석을 통한 정확한 운동 자세 교정 서비스
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
      </td>
    </tr>
  </tbody>
</table>

## ■ 목차 📚
1. 소개  
2. 프로젝트 진행 관리  
3. 사용 기술 스택  
4. 화면 구성  
5. 데이터 흐름도 및 사용자 흐름도  
6. 아키텍처  
7. How to Test

<h2>■ 소개 🧑‍🤝‍🧑</h2>

<table style="width: 100%; table-layout: fixed; border-spacing: 0; text-align: center;">
  <tr>
    <td style="width: 20%; padding: 10px; vertical-align: middle;">
      <div>
        <img src="image.png" alt="이한세" width="160" height="200"><br><br>
        <strong>이한세 (Michael)</strong><br>
        <em style="color:#f0a500;"># Squat Analysis</em>
      </div>
    </td>
    <td style="width: 20%; padding: 10px; vertical-align: middle;">
      <div>
        <img src="image1.png" alt="김미경" width="160" height="200"><br><br>
        <strong>김미경 (Mia)</strong><br>
        <em style="color:#f0a500;"># Body & Workout</em>
      </div>
    </td>
    <td style="width: 20%; padding: 10px; vertical-align: middle;">
      <div>
        <img src="image3.png" alt="이준혁" width="160" height="200"><br><br>
        <strong>이준혁 (Simon)</strong><br>
        <em style="color:#f0a500;"># Disease Risk</em>
      </div>
    </td>
    <td style="width: 20%; padding: 10px; vertical-align: middle;">
      <div>
        <img src="image5.png" alt="하연우" width="160" height="200"><br><br>
        <strong>하연우 (Woo)</strong><br>
        <em style="color:#f0a500;"># Mental Health </em>
      </div>
    </td>
    <td style="width: 20%; padding: 10px; vertical-align: middle;">
      <div>
        <img src="image4.png" alt="이기성" width="160" height="200"><br><br>
        <strong>이기성 (Bradley)</strong><br>
        <em style="color:#f0a500;"># Hospital Match</em>
      </div>
    </td>
  </tr>
</table>

## ■ 기능별 상세 요약 🔍

| 기능 | 이름 (영문) | 설명 |
|------|-------------|------|
| 🏋 운동 자세 교정 | Squat Analysis | 사용자의 스쿼트 자세를 **OpenCV와 MediaPipe**를 이용해 실시간으로 추적하고, **양쪽 무릎 관절 각도**를 기반으로 반복 횟수와 정확도를 분석합니다. <br> 분석된 자세 정보는 **Gemini 기반 AI 피드백 시스템**을 통해 교정 코멘트와 리포트 이미지로 시각화되며, **자세 개선 여부 추적 기능**도 포함되어 있습니다. |
| 🧬 체형 예측 및 운동 추천 | Body & Workout | 사용자의 성별, 연령, BMI 등을 기반으로 **랜덤 포레스트 모델**로 체형을 예측하고, 예측된 체형에 따라 운동 난이도(초급~고급)를 구분하여 맞춤형 운동 영상을 추천합니다. <br> 또한 **운동 목적(근력, 감량 등)에 따른 효과별 필터링 추천**과 함께, **CSV 기반 운동 데이터 + Plotly 시각화**로 구성된 콘텐츠를 제공합니다. |
| 💉 질병 예측 | Disease Risk | 건강검진 데이터를 기반으로 **당뇨, 고혈압, 고지혈증 등의 유병 확률을 RandomForest 모델로 예측**하고, 위험도는 **막대 그래프 + 툴팁**으로 시각화됩니다. <br> 추가로 **암 위험도 분석**, **2D 레이더 차트 및 3D 정육면체 시각화**를 통해 사용자의 **전반적인 건강 상태를 종합적으로 분석**합니다. |
| 🧠 우울증 예측 | Mental Health | PHQ-9 설문, 수면 시간, 건강검진 데이터를 기반으로 **우울증 단계를 AI 모델이 예측(없음~심각)**하고, 결과는 **수면 연관 차트**로 시각화됩니다. <br> **Gemini 기반 챗봇이 심리 분석 코멘트**를 자동 생성하며, **SHAP 분석**을 통해 예측에 영향을 준 **주요 요인 설명 기능**도 제공합니다. |
| 🏥 병원 추천 | Hospital Match | 사용자 건강검진 데이터를 기반으로 **질병 유무(당뇨, 고지혈증, 고혈압)를 예측**하고, 위험이 감지되면 **사용자 지역(city, town) 내 '내과' 병원 5곳을 자동 추천**합니다. <br> 추천 정보에는 **병원명, 주소, 전화번호, 위도·경도**가 포함되며, **CSV 기반 병원 정보 + 시각적 위치 연동(Naver 지도 API)** 기능도 함께 구성되어 있습니다. |


## ■  프로젝트 진행 관리 📊

![image](https://github.com/user-attachments/assets/7a16587a-5eb2-4be4-bfa9-fa67d59f96f1)

## ■ Stacks 🛠️

## Language
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)

## Backend(server)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat&logo=flask&logoColor=white)
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=flat&logo=mariadb&logoColor=white)

## Frontend
![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?style=flat&logo=bootstrap&logoColor=white)
![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?style=flat&logo=chartdotjs&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)

## Data Science / ML
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat)
<br>
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-FF6600?style=flat&logo=xgboost&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-3C5A6F?style=flat&logo=seaborn&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-000000?style=flat&logo=langchain&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat&logo=tensorflow&logoColor=white)

## API & External Services
![YouTube API](https://img.shields.io/badge/YouTube_API-FF0000?style=flat&logo=youtube&logoColor=white)
![Naver API](https://img.shields.io/badge/Naver_API-03C75A?style=flat)
![Gemini API](https://img.shields.io/badge/Google_Generative_AI-4285F4?style=flat&logo=google&logoColor=white)
![gRPC](https://img.shields.io/badge/gRPC-3F4C8C?style=flat&logo=grpc&logoColor=white)

## Dev Tools
![VS Code](https://img.shields.io/badge/VS_Code-007ACC?style=flat&logo=visualstudiocode&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)
![venv](https://img.shields.io/badge/venv-3C3C3C?style=flat&logo=python&logoColor=white)


## 데이터 흐름도, 사용자 흐름도 🔄
> 사용자 행동경로와 데이터기반 모델흐름, URL구조를 정리한 것입니다.

<img src="사용자흐름도(최종).png" alt="FinFit 사용자 흐름도" width="700">
<br>

## ■  아키텍처

### ▪ Directory 구조

</small>

