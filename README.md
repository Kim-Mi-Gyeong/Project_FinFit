# FinFit - 개인 맞춤형 스마트 헬스케어 시스템

FinFit은 건강검진 데이터를 기반으로 질병 예측, 체형 분석, 운동 추천, 병원 매칭, 우울증 예측 등 다양한 건강 서비스를 통합 제공하는 Flask 기반 웹 애플리케이션입니다.

---

## 목차
1. 소개  
2. 프로젝트 진행 관리  
3. 사용 기술 스택  
4. 화면 구성  
5. 데이터 흐름도 및 사용자 흐름도  
6. 아키텍처  
7. How to Test  

---

## 1. 소개

- 건강 데이터를 입력하면 체형 분석, 질병 예측, 운동 추천, 우울증 분석, 병원 추천을 받을 수 있는 AI 통합 헬스케어 시스템
- 챗봇(Fit봇)을 통해 각 기능에 대한 설명 및 추천까지 함께 제공
- 사용자 맞춤형 시각화 및 건강 개선 방향 제공

---

## 2. 프로젝트 진행 관리

![image](https://github.com/user-attachments/assets/7a16587a-5eb2-4be4-bfa9-fa67d59f96f1)


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

4. 주요 기능 및 담당 업무
주요 기능	설명	담당자
질병 예측	- 건강검진 데이터를 기반으로 RandomForest 기반 다중 분류 모델을 활용해 당뇨병, 고혈압, 고지혈증 등의 질환 위험도를 예측
- 예측된 위험도는 등급(정상/주의/위험)으로 분류되며, Plotly 기반 시각화를 통해 사용자에게 직관적으로 제공	Simon
병원 추천	- 건강검진 데이터를 기반으로 Random Forest 분류 모델을 활용해 질병 유무를 예측
- 예측 결과에서 특정 질병(고혈압, 당뇨, 고지혈증 등)이 있는 사용자에 한해,
입력값(city, town)을 기준으로 지역 내 병원을 추천
- 병원 데이터는 CSV 기반 의료기관 정보를 사용하며, Naver 지도 API를 연동하여 시각적 위치 정보를 제공	Bradley
우울증 예측	- 기본 건강정보와 PHQ-9 설문 데이터를 기반으로, XGBoost 모델 및 규칙 기반 로직을 활용하여 우울증 위험 단계를 예측
- 예측 결과에 따라 사용자의 정신 건강 상태를 분석하고, 위험 수준에 따른 코멘트를 제공	Woo
체형 예측 및 운동 추천	- 입력된 키와 몸무게를 기반으로 BMI를 계산한 뒤, Random Forest 기반 BMI 분류기로 체형을 분류
- 체형에 따라 운동 효과(근력/체중조절 등), 난이도 필터링을 통해 맞춤형 운동 영상을 추천
- 도넛 차트, conic-gradient 애니메이션, 체형 아이콘 등 다양한 시각화	Mia
운동 자세 교정	- 사용자의 실시간 웹캠 영상에서 Mediapipe pose detection 모델로 관절 좌표를 추출하고, 무릎-발끝 정렬, 각도 계산 등 기준에 따라 스쿼트 정확도를 분석
- 동작 오류 발생 시 Gemini 피드백과 TTS 음성 안내를 제공	Michael
챗봇 (Fit봇)	- 페이지별로 등록된 키워드 기반 응답 사전(page_responses)을 우선 활용하며, 해당 키워드가 없을 경우 Gemini API(gemini-1.5-flash)를 호출해 페이지 맥락에 맞는 실시간 LLM 응답을 생성
- 핵심만 간결하게 설명하는 프롬프트 설계로 사용자 피로도를 줄이고 기능/결과 해석/건강 가이드를 실시간 제공	Simon, Bradley

## 5. 데이터 흐름도

1. 건강정보 입력  
2. 체형 분석 및 질병 예측  
3. 결과 기반 운동/병원 추천 or 우울증 분석  
4. Fit봇의 피드백 및 추가 정보 제공

---

## 6. 사용자 흐름도

- 사용자 입력 → 전처리 → 모델 예측 → 결과 분석 및 시각화 → 서비스 제공

---

## 6. 아키텍처

### ▪ Directory 구조

