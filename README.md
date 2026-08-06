# Issac_asset

Isaac Gym 시뮬레이션용 에셋 저장소. [Issac_project](https://github.com/godhot1146/Issac_project)에서 사용한다.

## 구성

| 폴더 | 내용 |
|---|---|
| `isaac_assets/urdf/` | 로봇·물체 URDF 및 메쉬 (핵심 — carter, franka, indy7, forklift, conveyor, low_amr 등) |
| `isaac_assets/mjcf/` | MuJoCo 포맷 모델 (Isaac Gym 기본 샘플) |
| `isaac_assets/textures/` | 배경/재질 텍스처 이미지 |
| `isaac_assets/warehouse/` | 창고 랙 등 |

## 사용법

프로젝트 코드는 환경변수 `ISAAC_ASSETS`로 이 에셋의 루트를 참조한다.

```bash
git clone https://github.com/godhot1146/Issac_asset.git
export ISAAC_ASSETS=/절대경로/Issac_asset/isaac_assets
```

자세한 실행 방법은 [Issac_project README](https://github.com/godhot1146/Issac_project) 참고.

## 에셋 목록 (`isaac_assets/urdf/`)

### 🤖 로봇 (팔 / 이동로봇)
| 에셋 | 설명 |
|---|---|
| `doosan_a0509` | 두산 A0509 협동로봇팔 6축 — 프로젝트 주력 |
| `indy_description` | 뉴로메카 Indy7 로봇팔 (창고 버전 팔) |
| `franka_description` | Franka Emika Panda 7축 (Isaac Gym 표준 샘플) |
| `kinova_description` | Kinova 로봇팔 |
| `kuka_allegro_description` | KUKA 팔 + Allegro 다지 핸드 |
| `anymal_b_simple_description` | ANYmal 4족 보행로봇 |
| `carter` | NVIDIA Carter 자율주행 AMR |
| `low` | 저상형 AMR (low_amr) |
| `forklift` | 포크리프트 AMR |
| `lifting_amr` | 리프팅 AMR |

### 🛠 커스텀 에셋 (두산 셀 구성)
| 에셋 | 설명 |
|---|---|
| `robot_stand` | 로봇 스탠드/선반 60×60×80cm, Ø30 기둥 4개(개방 프레임) |
| `a0509_on_stand` | 두산 A0509 + 선반을 fixed joint로 결합한 통합 에셋 |
| `air_compressor` | 에어 컴프레셔 (STEP/STL→URDF 변환, 단일 바디) |

### 🏭 창고 설비 / 구조물
| 에셋 | 설명 |
|---|---|
| `conveyor` | 컨베이어 벨트 |
| `cargo_shelf` | 화물 선반(랙) |
| `pallet` | 팔레트 |
| `fixed_caser` | 고정 케이서(포장 설비) |
| `taping` | 테이핑 설비 |
| `fold_up` | 박스 접이 설비 |
| `warehouse` | 창고 구조물(랙·벽·박스 등 모음) |
| `sektion_cabinet_model` | 수납 캐비닛 (Franka 샘플) |
| `door` | 문 |
| `guest_space` | 사무/휴게 공간 소품(싱크·의자·찬장) |
| `square_table.urdf` | 사각 테이블 |

### 📦 물체 / 소품
| 에셋 | 설명 |
|---|---|
| `cardboard_box` | 접이식 카드보드 박스 |
| `tray` | 트레이 |
| `nut_bolt` | 너트·볼트 (조립 예제) |
| `ycb` | YCB 표준 물체 데이터셋(벤치마크용 일상 물체) |
| `objects` | 기타 물체 모음 |
| `ball.urdf` / `small_ball.urdf` | 공 |
| `cube.urdf` | 큐브 |

### 🧪 테스트 / 예제용 (Isaac Gym 기본)
| 에셋 | 설명 |
|---|---|
| `cartpole.urdf` | 카트폴 (강화학습 고전 예제) |
| `spherical_joint.urdf` | 구관절 테스트 |
| `icosphere.urdf` / `.tet` | 정이십면체 (연질체/변형 예제) |
