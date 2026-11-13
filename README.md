# Tiggle (Ticketing-Bench)

티켓 예매 백엔드입니다. 같은 조건에서 동시성 제어 방식 다섯 가지(비관적 락, 낙관적 락, Redisson 분산 락, Redis Lua, 대기열+Lua+Outbox+Kafka)를 비교하고, 장애를 주입해서 결과를 검증합니다.

팀원 4명이 도메인을 나누지 않고 각자 프로젝트 전체를 구현합니다. 마일스톤마다 "다음 마일스톤의 기술 스터디 → 각자 구현 → 회고"를 반복합니다.

## 저장소 구조

루트에는 팀이 함께 관리하는 공용 영역과 팀원별 폴더가 있습니다.

- **공용 영역**: 각자의 구현을 같은 기준으로 비교하기 위한 명세와 도구입니다.
  - [`docs/`](docs/)
    - [`milestones/`](docs/milestones/): 마일스톤별 작업 단위와 완료 조건
    - [`feature-spec.md`](docs/feature-spec.md): 기능 목록과 기능 ID
    - [`progress.md`](docs/progress.md): 팀원별 진행 현황판
    - [`harness/`](docs/harness/): 이슈별 핸드오프 작성 규칙과 이슈·PR 작성 규칙(형식만 있는 초안)
    - [`templates/`](docs/templates/): ADR, 런북, 실험 기록 템플릿
  - [`specs/`](specs/): API 명세(OpenAPI), 이벤트 스키마, 예약 상태 전이도
  - [`loadtest/`](loadtest/): 공용 k6 시나리오와 불변식 검사기
  - `.github/`: PR 템플릿과 CODEOWNERS
- **팀원별 폴더**: 각자의 구현이 들어갑니다. 폴더 안의 구성은 [`docs/milestones/m0.md`](docs/milestones/m0.md)의 작업으로 각자 만듭니다.
  - [`jeonggyu/`](jeonggyu/)
  - [`junhyeok/`](junhyeok/)
  - [`yonghwan/`](yonghwan/)
  - [`yuseong/`](yuseong/)

## 처음 읽을 문서

1. [`docs/milestones/`](docs/milestones/README.md): 마일스톤별 작업 단위와 완료 조건
2. [`docs/feature-spec.md`](docs/feature-spec.md): 기능 목록과 기능 ID
3. [`docs/progress.md`](docs/progress.md): 팀원별 진행 현황과 갱신 방법
4. 노션 "온보딩" 페이지: 기술 스택과 도입 이유

## 협업 규칙

아직 정하지 않았습니다. 팀 논의로 정하면 이 절에 정리할 예정입니다. 논의할 항목은 다음과 같습니다.

- 브랜치 전략(GitHub Flow / `develop` 브랜치)
- 리뷰 승인 기준과 리뷰어를 정하는 방법
- 공용 영역 변경의 확인 범위
- 이슈·PR·커밋 제목 규칙(기능 ID 표기 등)
- 진행 기록(하네스) 적용 범위

정해지기 전까지 PR은 [PR 템플릿](.github/pull_request_template.md)의 절을 따라 작성해 주세요.
