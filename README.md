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

| 주요 기능               | 설명                                                                 | 담당자              |
|------------------------|----------------------------------------------------------------------|---------------------|
| 질병 예측              | - 데이터를 기반으로 당뇨병, 고지혈증, 고혈압 등 주요 만성질환 예측 및 시각화              | Simon               |
| 병원 추천              | - 예측된 질환 위험도를 반영하여 사용자의 지역 기반 맞춤 병원 정보를 추천                           | Bradley             |
| 우울증 예측            | - 수면 시간 및 설문 데이터를 바탕으로 우울증 단계 분류 및 정신 건강 상태 분석               | Woo                 |
| 체형 예측 및 운동 추천 | - BMI 등 신체 지표 기반 체형 분류 후, 분석 결과에 따라 개인 맞춤 운동 영상 추천                  | Mia                 |
| 운동 자세 교정         | - 실시간 pose detection 모델을 활용한 스쿼트 자세 분석 및 피드백 제공                               | Michael             |
| 챗봇 (Fit봇)            | - 페이지 맥락에 따라 건강 정보, 기능 설명, 결과 해석 등을 인터페이스로 실시간 안내                    | Simon, Bradley      |

---

## 5. 데이터 흐름도 및 사용자 흐름도

---

## 6. 아키텍처

### ▪ Directory 구조

