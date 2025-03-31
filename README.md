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

| 주요 기능 | 설명 |
|--------|------|
| 메인 페이지 | 전체 기능 소개 및 바로가기 버튼 |
| 건강 정보 입력 | 사용자 키, 몸무게, 혈압 등 입력 폼 |
| 체형 분석 & 운동 추천 | BMI 기반 체형 예측 결과 및 운동 영상 추천 |
| 질병 예측 & 병원 추천 | 질병 분류 결과 및 지역 병원 리스트 제공 |
| 우울증 예측 | PHQ-9 설문 + 수면 시간 분석 |
| 챗봇(Fit봇) | 페이지별 안내 및 사용자 응대 |

---

## 5. 데이터 흐름도

1. 건강정보 입력  
2. 체형 분석 및 질병 예측  
3. 결과 기반 운동/병원 추천 or 우울증 분석  
4. Fit봇의 피드백 및 추가 정보 제공

---

## 6. 사용자 흐름도

- 사용자 입력 → 전처리 → 모델 예측 → 결과 분석 및 시각화 → 서비스 제공

---

## 7. 아키텍처

### ▪ Directory 구조

