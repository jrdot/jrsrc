# jrsrc

에이전트 플랫폼용 프롬프트(스킬, 규정)를 개발하는 공간.
이 폴더의 파일은 **소스**이며, 에이전트가 로드하는 활성 스킬이 아니다.

## 폴더
- `dev/` 개발: 작성·수정 중인 스킬과 규정
- `deliverable/` 배포: 완성되어 배포하는 스킬과 규정

### 구성

```
~/jrsrc
├── README.md
├── dev/           # 개발
│   ├── skills/
│   │   └── end-user-interview/
│   │       ├── SKILL.md
│   │       ├── references/
│   │       └── evals/
│   └── rules/
│       └── agent-operating-rules.md   # 에이전트 운영 규칙
└── deliverable/   # 배포
    ├── skills/
    └── rules/
```

## 규칙
- 수정은 `dev/`에서만 한다. `deliverable/`은 직접 수정하지 않는다.
- 완성되면 `dev/`에서 `deliverable/`로 수동 복사한다(`evals/`는 제외).
- 배포는 `deliverable/`에서 플랫폼의 스킬 경로로 수동 복사한다.
- 규정 파일명은 영문 kebab-case `.md` 단일 파일로 한다(예: `rules/agent-operating-rules.md`). 버전은 파일명에 넣지 않고 git 이력으로 관리한다.
- 이 프로젝트 안에 `.claude/`, `CLAUDE.md`, `AGENTS.md`를 두지 않는다(자동 로드 방지).

