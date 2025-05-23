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

## 📄 참고
  PPO: Stable-Baselines3 라이브러리 기반
  
  TTC 계산: traci.vehicle.getLeader() 기반 실시간 추출
  
  시뮬레이션은 SUMO GUI 또는 headless 모드 모두 지원

---

### 📘 논문 관련
본 프로젝트는 KCC 2025 학부생 논문 제출을 위한 실험 기반 연구로 수행되었으며,
강화학습 기반 사고 회피 전략의 실효성과 안전성 분석을 목적으로 합니다.

---

📬 문의
정재훈 (Jaehoon Jung)
[이메일 또는 GitHub 프로필 링크]

---
