# siyeong (시영)

시영의 Tiggle 구현입니다. 기능 범위와 완료 조건은 [`docs/milestones/`](../docs/milestones/README.md)와 [`docs/feature-spec.md`](../docs/feature-spec.md)를 따릅니다.

## 권장 구성

회고에서 서로의 구현을 비교하기 쉽도록 아래 구성과 모듈 이름을 맞추는 것을 권합니다. M0에서 직접 만들어 주세요.

- `ticketing-core/`: 모듈형 모놀리스(`auth`, `organizer`, `reservation`, `payment`, `coupon`, `audit`)
- `mock-pg/`: 결제 대행사를 흉내 내는 서버(M3)
- `notification-service/`: M7에서 분리
- `search-indexer/`: M8
- `settlement-batch/`: M10
- `infra/`: Docker Compose, k3s 매니페스트, Terraform
- `docs/`: 자기 구현의 `adr/`, `runbook/`, `experiments/`

## CI

GitHub Actions 워크플로는 저장소 루트의 `.github/workflows/`에만 배치할 수 있습니다. 자기 폴더만 빌드하도록 `paths: ['siyeong/**']` 필터를 지정한 `siyeong.yml`을 만들어 주세요.

## 진행 현황

이슈마다 `docs/handoff/issue-{번호}-handoff.md`를 이 폴더 안에 만들어 진행, 설계 결정, 검증 결과를 기록합니다. 작성 규칙은 [`docs/harness/README.md`](../docs/harness/README.md)를 따르고, 단계를 시작하거나 마치면 [`docs/progress.md`](../docs/progress.md)의 자기 칸도 고쳐 주세요.
