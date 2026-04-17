# CHANGELOG — project-updater

## v1.1.0 (2026-04-17)

### 구조 개편 (skill-doctor 진단 후 처방)

**건강점수 변화:** 🟠 67.7 → 목표 🟢 ≥80

- **[비대 해소]** SKILL.md 10.3KB → ~5KB 목표. 상세 절차를 references/로 분리
  - `references/claude-md-generation.md` 신설 (CLAUDE.md 생성 프로토콜·체크리스트)
  - `references/graph-md-generation.md` 신설 (GRAPH.md 생성·갱신·체크리스트)
  - `references/batch-update.md` 신설 (볼트 전체 순회 절차)
- **[INVARIANT 보호]** 절대 규칙 5개 섹션 신설 (볼트 마운트·덮어쓰기 금지·형 승인·인젝션 방어·파일명 고정)
- **[회귀 검증]** `evals/cases.json` 6 케이스 추가 (풀초기화·GRAPH 갱신·배치·독립생성·인젝션·볼트미마운트)
- **[버전관리]** frontmatter `version: 1.1.0` + CHANGELOG.md 추가
- **[Self-Check]** self-check 프로토콜 명시 (validate.py + evals 드라이런)
- **[Gotchas 보강]** 빈폴더·심볼릭링크·볼트미마운트 항목 추가 → 9개 → 11개
- **[예시 추가]** "새 프로젝트 초기세팅" 실행 예시 1개
- **[피드백 채널]** thumbs-down 안내 추가
- **[P1 키워드 본문 등장]** "프로젝트초기화·초기세팅·지식그래프·그래프갱신·md생성" 등 본문 문단 보강

### 하위호환

- 모든 모드 판정 키(CLAUDE.md 생성·GRAPH.md 생성·풀초기화·갱신·전체갱신) 보존
- 파일명 `CLAUDE.md`/`GRAPH.md` 고정 유지
- 기존 references/ 3개(interview·templates·graph-template) 유지

## v1.0.0 (2026-04-16)

- 초기 버전 (프로젝트 CLAUDE.md + GRAPH.md 통합 엔진)
