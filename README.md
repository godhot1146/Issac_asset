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
