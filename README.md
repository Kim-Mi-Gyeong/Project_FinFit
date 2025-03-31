# ■ FinFit - 개인 맞춤형 헬스케어 서비스 💪

FinFit은 건강 검진 데이터와 AI 예측 모델을 활용하여 사용자의 건강 상태를 정밀 분석하고 맞춤형 솔루션을 제공하는 스마트 헬스케어 서비스를 제공합니다. 또한, 바쁜 현대인을 위해 생활 습관 개선부터 병원 연계까지 체계적인 건강 관리 시스템을 제공하여, 누구나 쉽게 건강을 유지하고 더 나은 미래를 준비할 수 있도록 지원합니다.


---



## ■ 목차 📚
1. 소개  
2. 프로젝트 진행 관리  
3. 사용 기술 스택  
4. 화면 구성  
5. 데이터 흐름도 및 사용자 흐름도  
6. 아키텍처  
7. How to Test


---





## ■  소개 👨‍👩‍👧‍👦

- 건강 데이터를 입력하면 체형 분석, 질병 예측, 운동 추천, 우울증 분석, 병원 추천을 받을 수 있는 AI 통합 헬스케어 시스템
- 챗봇(Fit봇)을 통해 각 기능에 대한 설명 및 추천까지 함께 제공
- 사용자 맞춤형 시각화 및 건강 개선 방향 제공



---




## ■  프로젝트 진행 관리 📊

![image](https://github.com/user-attachments/assets/7a16587a-5eb2-4be4-bfa9-fa67d59f96f1)


## ■  Stacks 🛠️

## ▪ Language
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)



## ▪ Backend(server)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat&logo=flask&logoColor=white)
![MariaDB](https://img.shields.io/badge/MariaDB-003545?style=flat&logo=mariadb&logoColor=white)



## ▪ Frontend
![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?style=flat&logo=bootstrap&logoColor=white)
![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?style=flat&logo=chartdotjs&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)


## ▪ Data Science / ML
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


## ▪ API & External Services
![YouTube API](https://img.shields.io/badge/YouTube_API-FF0000?style=flat&logo=youtube&logoColor=white)
![Naver API](https://img.shields.io/badge/Naver_API-03C75A?style=flat)
![Gemini API](https://img.shields.io/badge/Google_Generative_AI-4285F4?style=flat&logo=google&logoColor=white)
![gRPC](https://img.shields.io/badge/gRPC-3F4C8C?style=flat&logo=grpc&logoColor=white)



## ▪ Dev Tools
![VS Code](https://img.shields.io/badge/VS_Code-007ACC?style=flat&logo=visualstudiocode&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)
![venv](https://img.shields.io/badge/venv-3C3C3C?style=flat&logo=python&logoColor=white)


---




## ■  주요 기능 및 담당 업무 🤖 

| 주요 기능               | 설명 | 담당자 |
|------------------------|------|--------|
| 질병 예측              | - 건강검진 데이터를 기반으로 **RandomForest 기반 다중 분류 모델**을 활용해 당뇨병, 고혈압, 고지혈증 등의 질환 위험도를 예측 <br> - 예측된 위험도는 등급(정상/주의/위험)으로 분류되며, Plotly 기반 시각화를 통해 사용자에게 직관적으로 제공 | Simon |
| 병원 추천              | - 건강검진 데이터를 기반으로 **Random Forest 분류 모델**을 활용해 질병 유무를 예측 <br> - 예측 결과에서 특정 질병(고혈압, 당뇨, 고지혈증 등)이 있는 사용자에 한해, <br> 입력값(`city`, `town`)을 기준으로 지역 내 병원을 추천 <br> - 병원 데이터는 **CSV 기반 의료기관 정보**를 사용하며, **Naver 지도 API**를 연동하여 시각적 위치 정보를 제공 | Bradley |
| 우울증 예측            | - 기본 건강정보와 PHQ-9 설문 데이터를 기반으로, XGBoost 모델 및 규칙 기반 로직을 활용하여 우울증 위험 단계를 예측 <br> - 예측 결과에 따라 사용자의 정신 건강 상태를 분석하고, 위험 수준에 따른 코멘트를 제공 | Woo |
| 체형 예측 및 운동 추천 | - 입력된 키와 몸무게를 기반으로 BMI를 계산한 뒤, **Random Forest 기반 BMI 분류기**로 체형을 분류 <br> - 체형에 따라 운동 효과(근력/체중조절 등), 난이도 필터링을 통해 맞춤형 운동 영상을 추천 <br> - 도넛 차트, conic-gradient 애니메이션, 체형 아이콘 등 다양한 시각화 | Mia |
| 운동 자세 교정         | - 사용자의 실시간 웹캠 영상에서 **Mediapipe pose detection 모델**로 관절 좌표를 추출하고, 무릎-발끝 정렬, 각도 계산 등 기준에 따라 스쿼트 정확도를 분석 <br> - 동작 오류 발생 시 **Gemini 피드백**과 **TTS 음성 안내**를 제공 | Michael |
| 챗봇 (Fit봇)           | - 페이지별로 등록된 **키워드 기반 응답 사전**(page_responses)을 우선 활용하며, 해당 키워드가 없을 경우 **Gemini API**(gemini-1.5-flash)를 호출해 페이지 맥락에 맞는 실시간 LLM 응답을 생성 <br> - 핵심만 간결하게 설명하는 프롬프트 설계로 사용자 피로도를 줄이고 기능/결과 해석/건강 가이드를 실시간 제공 | Simon, Bradley |



---



## ■  사용자 및 데이터 흐름도 📈

> 사용자 행동경로와 데이터기반 모델흐름, URL구조를 정리한 것입니다.

<img src="사용자흐름도.png" alt="FinFit 사용자 흐름도" width="700">


## ■  아키텍처

### ▪ Directory 구조

