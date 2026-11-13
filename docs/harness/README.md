# 하네스 문서

AI 코딩 에이전트와 함께 작업할 때 따르는 작업 규칙입니다. 원본은 다른 프로젝트에서 사용하던 일반화된 하네스 문서(2026-10-06 기준)이며, 그중 진행 기록과 이슈·PR 작성에 필요한 세 문서만 가져왔습니다. 핸드오프와 작업 범위 규칙은 원문 그대로이고, 이슈·PR 규칙은 협업 규칙이 정해지지 않아 절 구성만 남긴 초안으로 바꿨습니다. Tiggle에서는 아래 "Tiggle 적용 사항"이 원문보다 우선합니다.

> 이 규칙을 팀원 전체에 적용할지는 팀 합의 전입니다. 합의 전까지는 원하는 팀원이 자기 폴더에서 적용해 주세요.

## 구성

- [personal_convention/handoff_convention.md](personal_convention/handoff_convention.md): 이슈별 핸드오프 작성과 갱신, 작업 단위 설계 기준, 계획 승인 절차
- [personal_convention/work_scope_convention.md](personal_convention/work_scope_convention.md): 한 채팅에서 작업 단위 하나를 진행하는 방식, 검증, 작업 후 보고 방식
- [project_code_convention/issue_pr_convention.md](project_code_convention/issue_pr_convention.md): 이슈와 PR 본문의 섹션 구성(내용은 협업 규칙이 정해지면 채움)

## Tiggle 적용 사항

### 경로

원문의 경로는 저장소 하나를 한 사람이 구현하는 구조를 전제로 합니다. Tiggle은 4명이 각자 폴더에서 같은 작업을 구현하므로 아래처럼 바꿔 읽어 주세요.

- 이슈별 핸드오프: `docs/handoff/issue-{번호}-handoff.md` → `<자기 폴더>/docs/handoff/issue-{번호}-handoff.md`
  - 예: `jeonggyu/docs/handoff/issue-12-handoff.md`
  - 같은 이슈를 여러 명이 구현하면 각자 폴더에 같은 번호의 파일이 생깁니다.
- future plan: `docs/handoff/plan/future-plan.md` → [docs/milestones/](../milestones/README.md). 단계 순서와 완료 기준은 이 폴더를 링크하고 따로 만들지 않습니다.
- 제품 맥락 문서: `docs/project-overview.md` → 저장소 [README](../../README.md)와 노션 "온보딩" 페이지
- `legacy/`: 각자 `<자기 폴더>/docs/handoff/legacy/`를 사용합니다.
- 핸드오프는 저장소에 추적합니다. 회고에서 각자의 선택과 이유를 비교하는 근거로 사용하기 때문입니다. 원문 README의 "개인 규칙은 `.gitignore`에 추가한다"는 Tiggle에 적용하지 않습니다.

### 팀 현황판과의 관계

- 팀 전체에서 누가 어느 단계에 있는지는 [docs/progress.md](../progress.md)에서 관리합니다. 핸드오프는 이슈 하나의 세부 진행만 담습니다.
- 단계를 시작하거나 마치면 progress.md의 자기 칸을 고치고, 그 단계의 핸드오프 링크를 함께 남겨 주세요.

### 아직 없는 참조 대상

원문이 가리키는 아래 문서와 파일은 Tiggle에 아직 없습니다. 생길 때까지 해당 문장은 건너뛰어 주세요.

- `AGENTS.md`(handoff_convention.md의 판단 순서, 0절 참조 문서)
- `project_code_convention/testing_convention.md`, `personal_convention/comment-style.md`(work_scope_convention.md의 링크)
- `.github/ISSUE_TEMPLATE/`(issue_pr_convention.md의 이슈 템플릿). PR 템플릿은 [`.github/pull_request_template.md`](../../.github/pull_request_template.md)이며, 섹션 이름이 원문과 다르면 Tiggle 템플릿을 따릅니다.
- 원격 저장소와 GitHub Issue. 이슈 번호가 생긴 뒤부터 핸드오프를 만들 수 있습니다.
