# 🚗 V2V 회피 전략 시뮬레이터

본 프로젝트는 **SUMO(Simulation of Urban MObility)** 시뮬레이터 기반에서 **V2V(Vehicle-to-Vehicle)** 차량 간 협력 주행 상황을 구성하고, **PPO(Proximal Policy Optimization)** 알고리즘을 활용하여 사고 회피 전략을 학습하는 시뮬레이션 프레임워크입니다.  
또한 **TTC(Time-to-Collision)** 기반의 위험도 분석 및 시각화 기능을 포함합니다.

---

## 📌 주요 기능

- ✅ NGSIM 기반 궤적 데이터 전처리
- 🚗 혼잡 + 급정지 차량 포함 시나리오 자동 생성
- 🛣️ SUMO 환경 구성 자동화 (.xml 생성)
- 🧠 PPO 기반 강화학습 환경 제공
- 📊 시뮬레이션 중 TTC 계산 및 평균/표준편차 분석
- ⚠️ TTC < 3 구간 하이라이트 및 이벤트 밀도 시각화

---

## 🧱 프로젝트 구조

V2V/ ├── data/ # SUMO 환경 구성용 .xml 및 차량 궤적 CSV │ └── ... │ ├── logs/ # PPO 학습 로그 저장 디렉토리 │ ├── models/ │ ├── ppo_sumo_agent.zip # 학습된 PPO 모델 파일 │ ├── sumo_env.py # PPO 학습용 gym 환경 정의 │ ├── init.py │ └── scripts/ │ ├── ppo_train_agent.py # PPO 에이전트 학습 코드 │ ├── ppo_test_agent.py # 학습된 모델 테스트 시뮬레이션 │ └── analyze_ttc_plot.py # TTC 시각화 스크립트 │ ├── V2V_avoid_dataprocessing.ipynb # 데이터 전처리 및 SUMO XML 자동 생성 ├── README.md


📬 문의
정재훈 (Jaehoon Jung)
[이메일 또는 GitHub 프로필 링크]
