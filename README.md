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

| 주요 기능               | 설명                                                                                                                                          | 담당자            |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------------------|
| 질병 예측              | 사용자 건강검진 데이터를 기반으로 전처리 후, **XGBoost 기반 다중 분류 모델**을 통해 당뇨, 고혈압, 고지혈증 위험도를 예측하고 Plotly로 시각화함. <br> (파일: `disease_views.py`, `disease.html`) | Simon             |
| 병원 추천              | 예측된 질병 결과와 사용자 지역 정보(`city`, `town`)를 기반으로 **CSV 병원 데이터 + Naver 지도 API**를 활용해 맞춤형 병원을 추천함. <br> (파일: `hospital_views.py`, `hospital.html`) | Bradley           |
| 우울증 예측            | 건강정보 + PHQ-9 설문 데이터를 수집하여 **로지스틱 회귀 모델 + 규칙기반 분류**로 우울증 단계를 분류하고, 수면 분석과 정신건강 코멘트를 함께 제공함. <br> (파일: `depression_views.py`, `depression.html`) | Woo               |
| 체형 예측 및 운동 추천 | 키, 몸무게로 BMI를 계산하고 **Random Forest 기반 체형 분류 모델**을 활용하여 체형을 예측 후, 효과/난이도 기준으로 운동 영상을 필터링해 추천함. <br> 도넛 차트, conic-gradient, 체형 아이콘 등 시각화 포함. <br> (파일: `exercise_views.py`, `exercise.html`) | Mia               |
| 운동 자세 교정         | 실시간 웹캠 영상에서 **Mediapipe pose detection**으로 관절 위치 추출 → 자세 오류 분석 및 **TTS 음성 피드백** 제공. <br> (파일: `squat_views.py`, `static/js/squat.js`) | Michael           |
| 챗봇 (Fit봇)            | 페이지별 **키워드 응답 사전** 기반 응답 → 미응답 시 **Gemini API(gemini-1.5-flash)** 호출하여 LLM 기반 실시간 맥락형 답변 제공. <br> (파일: `chatbot_views.py`) | Simon, Bradley    |

---

## 5. 데이터 흐름도 및 사용자 흐름도

---

## 6. 아키텍처

### ▪ Directory 구조

