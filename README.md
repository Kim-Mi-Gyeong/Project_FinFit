<small>

# ■ FinFit - 개인 맞춤형 헬스케어 서비스 💪

FinFit은 건강 검진 데이터와 AI 예측 모델을 활용하여 사용자의 건강 상태를 정밀 분석하고 맞춤형 솔루션을 제공하는 스마트 헬스케어 서비스입니다.  
생활 습관 개선부터 병원 연계까지, 체계적인 건강 관리 시스템을 통해 누구나 쉽게 건강을 유지하고 더 나은 미래를 준비할 수 있도록 지원합니다.

---

## 📅 프로젝트 개요

| 항목           | 내용 |
|----------------|------|
| **개발 기간**   | 2025년 2월 24일(월) ~ 2025년 4월 1일(화) |
| **프로젝트 목표** | - AI 질병 예측과 그래프로 보는 건강 분석<br>- 질병 별 위치기반 병원 매칭 서비스<br>- 체형 분석을 통한 건강 맞춤 운동 솔루션 제공<br>- 검진 데이터 기반 우울증 예측 및 맞춤 정보 제공<br>- AI 분석을 통한 정확한 운동 자세 교정 서비스 |

---

## 📚 목차

1. 소개  
2. 기능별 요약  
3. 프로젝트 진행 관리  
4. Stacks  
5. 기능 구현  
6. 데이터 & 사용자 흐름도  
7. Architecture  
8. How to Test

---

## 👥 소개

<table style="width: 100%; table-layout: fixed; border-spacing: 0; text-align: center;">
  <tr>
    <td>
      <img src="image.png" width="120"><br>
      <b>이한세 (Michael)</b><br><i># Squat Analysis</i>
    </td>
    <td>
      <img src="image1.png" width="120"><br>
      <b>김미경 (Mia)</b><br><i># Body & Workout</i>
    </td>
    <td>
      <img src="image3.png" width="120"><br>
      <b>이준혁 (Simon)</b><br><i># Disease Risk</i>
    </td>
    <td>
      <img src="image5.png" width="120"><br>
      <b>하연우 (Woo)</b><br><i># Mental Health</i>
    </td>
    <td>
      <img src="image4.png" width="120"><br>
      <b>이기성 (Bradley)</b><br><i># Hospital Match</i>
    </td>
  </tr>
</table>

---

## 🔍 기능별 상세 요약

| 기능 | 설명 |
|------|------|
| **스쿼트 자세 교정** | OpenCV와 MediaPipe를 이용한 실시간 무릎 관절 각도 추적 및 정확도 분석. Gemini AI 피드백 시스템과 리포트 시각화 기능 포함. |
| **체형 예측 및 운동 추천** | 성별, 연령, BMI를 기반으로 체형 분류 후 운동 난이도·효과 필터링 제공. 도넛 차트 및 체형 아이콘 시각화 포함. |
| **질병 예측** | 건강검진 데이터를 기반으로 RandomForest 모델을 통해 당뇨, 고혈압, 고지혈증 예측. 암 리스크, 2D/3D 시각화 지원. |
| **우울증 예측** | PHQ-9 설문 + 수면 정보 기반 XGBoost 모델로 우울증 단계 예측. SHAP 요인 분석 + 심리 코멘트 자동 생성 기능 포함. |
| **병원 추천** | 예측된 질병에 따라 사용자 지역 기반 병원 추천(Naver 지도 API 연동). 병원명, 주소, 위치 정보 제공. |

---

## 📊 프로젝트 진행 관리

![progress](https://github.com/user-attachments/assets/7a16587a-5eb2-4be4-bfa9-fa67d59f96f1)

---

## 🛠️ Stacks

### Language
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)

### Backend
![Flask](https://img.shields.io/badge/Flask-000000?style=flat&logo=flask&logoColor=white)
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=flat&logo=mariadb&logoColor=white)

### Frontend
![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?style=flat&logo=bootstrap&logoColor=white)
![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?style=flat&logo=chartdotjs&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)

### Data / ML
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-FF6600?style=flat&logo=xgboost&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-3F4F75?style=flat&logo=plotly&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat)
![Seaborn](https://img.shields.io/badge/Seaborn-3C5A6F?style=flat&logo=seaborn&logoColor=white)
![SHAP](https://img.shields.io/badge/SHAP-FFA500?style=flat)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat&logo=opencv&logoColor=white)
![MediaPipe](https://img.shields.io/badge/MediaPipe-F7931E?style=flat)

### External Services
![YouTube API](https://img.shields.io/badge/YouTube_API-FF0000?style=flat&logo=youtube&logoColor=white)
![Naver API](https://img.shields.io/badge/Naver_API-03C75A?style=flat)
![Gemini API](https://img.shields.io/badge/Google_Generative_AI-4285F4?style=flat&logo=google&logoColor=white)

---

## 🧭 데이터 & 사용자 흐름도

<img src="사용자흐름도(최종).png" alt="FinFit 사용자 흐름도" width="700">

---

# ■ Architecture 🗂️
<pre>
  
📂cosmetic_project/<br>
│──📂cos/<br>
│   ├── init.py                       # Flask 애플리케이션 초기화<br>
│   ├── word2vec_model.py             # Word2Vec 모델 학습 및 로드<br>
│   ├── 📂data/                       # 화장품 성분 데이터 (CSV 등)<br>
│   ├── 📂ingrements_faiss_index/     # FAISS 벡터 검색 인덱스 저장소<br>
│   ├── 📂static/                     # CSS, JS 파일 등 정적 파일<br>
│   ├── 📂templates/                  # HTML 템플릿<br>
│   ├── 📂views/                      # Flask 라우팅 및 API 처리<br>
│   │   ├── visualization_views.py     # 시각화 API<br>
│   │   ├── search_views.py            # 검색 API (FAISS 기반)<br>
│   │   ├── chatbot_views.py           # 챗봇 API<br>
│   │   ├── chart_views.py             # 차트 데이터 API<br>
│   │   ├── main_views.py              # 메인 페이지 API<br>
</pre>

## ■ How to Test 🧪

> 아래 테스트는 `Flask` 서버 실행 후 `http://localhost:5000` 접속 시 확인할 수 있습니다.

| 테스트 항목 | 경로 | 주요 확인 내용 |
|-------------|------|----------------|
| 메인 페이지 | `/` | 전체 기능 링크 및 UI 연결 확인 |
| 사용자 정보 입력 | `/customer` | 성별·나이·키·몸무게·도시·지역 입력 후 DB 저장 |
| 스쿼트 분석 | `/squat` | 웹캠 기반 실시간 자세 추적 + 반복 수·피드백 확인 |
| 체형 예측 & 운동 추천 | `/exercise` | BMI 기반 체형 분류 + 난이도별 운동 영상 추천 |
| 질병 예측 | `/disease` | 당뇨·고혈압·고지혈증 예측 그래프 + 암 위험도 시각화 |
| 우울증 예측 | `/depression` | PHQ-9 기반 우울 단계 분석 + 수면 차트, AI 코멘트 확인 |
| 병원 추천 | `/hospital` | 지역 내 질병별 내과 병원 자동 추천 (Naver 지도 연동) |

🧩 모든 테스트는 가상환경(`venv`)에서 Flask 실행 후, 브라우저 기반으로 진행합니다.


</small>

