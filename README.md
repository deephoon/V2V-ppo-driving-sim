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

. ├── data/ │ ├── us101.nod.xml # 노드 정의 파일 │ ├── us101.edg.xml # 도로(엣지) 정의 │ ├── us101.netccfg # 네트워크 생성용 설정 │ ├── us101.sumocfg # SUMO 시뮬레이션 설정 파일 │ ├── vehicle_scenario.rou.xml # 차량 경로 및 정지 이벤트 정의 │ ├── vehicle_info.csv # 차량 정보 요약 │ └── veh_*.csv # 개별 차량 궤적 데이터 │ ├── V2V_avoid_dataprocessing.ipynb # 전처리 및 XML 생성 ├── ttc_analysis.py # TTC 계산 및 시각화 ├── rl_env/ # PPO 학습 환경 (gym.Env) └── README.md

markdown
복사
편집

---

## ⚙️ 설치 및 실행 환경

- Python ≥ 3.8  
- [SUMO](https://www.eclipse.org/sumo/) 설치 필요  
- `traci`, `pandas`, `numpy`, `matplotlib`, `stable-baselines3`

```bash
pip install pandas numpy matplotlib stable-baselines3
🚀 실행 방법
NGSIM 데이터 전처리 및 SUMO 시나리오 생성
V2V_avoid_dataprocessing.ipynb 실행 → .rou.xml, .nod.xml, .edg.xml 등 생성

SUMO 네트워크 파일 생성

bash
복사
편집
netconvert -c ./data/us101.netccfg
TTC 기반 위험도 분석 실행

bash
복사
편집
python ttc_analysis.py
PPO 학습 실행 (추후 추가 예정)

bash
복사
편집
# train_ppo.py (coming soon)
📊 결과 시각화 예시

평균 TTC와 위험 구간(붉은 음영) 표시


TTC < 3 이벤트 밀도 분포 시각화

📝 논문 정보
본 프로젝트는 KCC 2025 학부생 논문 출품용 연구로 개발되었습니다.
시뮬레이션 환경, 분석 지표, 학습 프레임워크 등을 포함합니다.

📬 문의
정재훈 (Jaehoon Jung)
[이메일 또는 GitHub 프로필 링크]
