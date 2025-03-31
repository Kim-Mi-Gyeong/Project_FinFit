# FinFit - 개인 맞춤형 스마트 헬스케어 시스템

FinFit은 건강검진 데이터를 기반으로 질병 예측, 체형 분석, 운동 추천, 병원 매칭, 우울증 예측 등 다양한 건강 서비스를 통합 제공하는 Flask 기반 웹 애플리케이션입니다.

---

## 목차
1. 소개  
2. 프로젝트 진행 관리  
3. 사용 기술 스택  
4. 화면 구성  
5. 데이터 흐름도
6. 사용자 흐름도  
7. 아키텍처  
8. How to Test  

---

## 1. 소개

- 건강 데이터를 입력하면 체형 분석, 질병 예측, 운동 추천, 우울증 분석, 병원 추천을 받을 수 있는 AI 통합 헬스케어 시스템
- 챗봇(Fit봇)을 통해 각 기능에 대한 설명 및 추천까지 함께 제공
- 사용자 맞춤형 시각화 및 건강 개선 방향 제공

---

## 2. 프로젝트 진행 관리

- 일정 관리: Notion
- 협업 도구: GitHub Projects
- 브랜치 전략: `main`, `develop`, `feature/*`

---

## 3. 사용 기술 스택

### ▪ Environment
- VS Code
- Git / GitHub
- Jupyter Notebook

### ▪ Frontend
- HTML5, CSS3, Bootstrap 5
- JavaScript (Jinja2)
- Plotly.js, Chart.js
- AJAX (jQuery)

### ▪ Backend
- Python, Flask, Flask-Restful

### ▪ AI / ML
- Scikit-learn, XGBoost, LightGBM, CatBoost
- Pandas, NumPy, Matplotlib
- conic-gradient, Mediapipe, OpenCV
- Web Speech API (TTS), Naver Map API

---

## 4. 주요 기능 및 담당 업무

### ● 질병 예측 (담당: Simon)
- 사용자 건강검진 데이터를 기반으로 전처리 후,
  **XGBoost 기반 다중 분류 모델**을 활용해 당뇨병, 고혈압, 고지혈증 등의 질환 위험도를 예측합니다.
- 예측된 위험도는 등급(정상/주의/위험)으로 분류되며,
  Plotly 기반 시각화를 통해 사용자에게 직관적으로 제공됩니다.
- 관련 파일: `disease_views.py`, `disease.html`

---

### ● 병원 추천 (담당: Bradley)
- 질병 예측 결과와 사용자 입력값(`city`, `town`)을 기반으로
  **CSV 병원 데이터**와 **Naver 지도 API**를 연동하여
  사용자의 지역에 맞는 병원을 추천합니다.
- 예측된 질환에 따라 관련 진료과(예: 내과, 정신건강의학과 등)를 자동 필터링합니다.
- 관련 파일: `hospital_views.py`, `hospital.html`

---

### ● 우울증 예측 (담당: Woo)
- 기본 건강정보와 함께 **PHQ-9 설문 결과**를 수집하여,
  **로지스틱 회귀 모델** 및 규칙기반 분류 로직으로 우울증 단계를 예측합니다.
- 수면 시간 및 건강 지표와의 상관관계를 분석하여
  사용자에게 정신 건강 분석 결과와 코멘트를 제공합니다.
- 관련 파일: `depression_views.py`, `depression.html`

---

### ● 체형 예측 및 운동 추천 (담당: Mia)
- 입력된 키와 몸무게를 기반으로 BMI를 계산한 뒤,
  **Random Forest 기반 BMI 분류기**로 체형을 분류합니다.
- 체형에 따라 운동 효과(근력/체중조절 등), 난이도 필터링을 통해
  맞춤형 운동 영상을 추천합니다.
- 도넛 차트, conic-gradient 애니메이션, 체형 아이콘 등 다양한 시각화 포함.
- 관련 파일: `exercise_views.py`, `exercise.html`

---

### ● 운동 자세 교정 (담당: Michael)
- 사용자의 실시간 웹캠 영상에서 **Mediapipe pose detection 모델**로 관절 좌표를 추출하고,
  무릎-발끝 정렬, 각도 계산 등 기준에 따라 스쿼트 정확도를 분석합니다.
- 동작 오류 발생 시 **텍스트 피드백**과 **TTS 음성 안내**를 제공합니다.
- 관련 파일: `squat_views.py`, `static/js/squat.js`

---

### ● 챗봇 (Fit봇) (담당: Simon, Bradley)
- 페이지별로 등록된 **키워드 기반 응답 사전(page_responses)**을 우선 활용하며,
  해당 키워드가 없을 경우 **Gemini API(gemini-1.5-flash)**를 호출해
  페이지 맥락에 맞는 실시간 LLM 응답을 생성합니다.
- 핵심만 간결하게 설명하는 프롬프트 설계로 사용자 피로도를 줄이고
  기능/결과 해석/건강 가이드를 실시간 제공합니다.
- 관련 파일: `chatbot_views.py`

---

## 5. 데이터 흐름도 및 사용자 흐름도

---

## 6. 아키텍처

### ▪ Directory 구조

