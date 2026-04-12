# project-updater

> 🇺🇸 [English README](./README.md)

**프로젝트 CLAUDE.md + GRAPH.md 통합 엔진 — 작업지침 생성과 Obsidian 위키링크 기반 지식그래프를 한 번에.**

## 사전 요구

- **Claude Cowork 또는 Claude Code** 환경
- **Obsidian Vault** (위키링크 기반 노트 구조)

## 목표

새 프로젝트 폴더마다 두 가지가 필요하다. AI에게 작업 규칙을 알려주는 CLAUDE.md, 문서 관계를 매핑해서 매 세션 전체 파일을 다시 읽지 않아도 되는 GRAPH.md. 이 스킬은 한 번의 호출로 둘 다 생성한다 — 인터뷰 기반 템플릿으로 CLAUDE.md, 내용 분석 기반으로 GRAPH.md.

## 사용 시점 & 방법

새 프로젝트를 시작할 때, CLAUDE.md나 GRAPH.md가 없는 폴더를 발견했을 때, 문서가 변경되어 지식그래프 갱신이 필요할 때 발동. "프로젝트 업데이터", "프로젝트 업데이트 실행해줘"로 트리거. 볼트 전체 대상은 "전체 프로젝트 업데이트".

## 사용 사례

| 상황 | 프롬프트 | 동작 |
|---|---|---|
| 새 프로젝트 폴더 | `"새 프로젝트 세팅해줘"` | 인터뷰 → 유형 판별 → CLAUDE.md + GRAPH.md 생성 |
| 문서 추가/변경 | `"GRAPH.md 갱신해줘"` | 폴더 재스캔 → 변경분만 외과적 diff 반영 |
| 볼트 전체 점검 | `"전체 프로젝트 업데이트"` | 전체 프로젝트 폴더 병렬 스캔 → 리포트 테이블 |

## 주요 기능

- **3유형 CLAUDE.md 템플릿** — 풀스펙(A), 표준형(B), 최소형(C)을 프로젝트 복잡도에 맞춤
- **Obsidian 위키링크 지식그래프** — `[[위키링크]]` 기반 GRAPH.md로 그래프뷰 네이티브 연동
- **인터뷰 프로토콜** — 최소 왕복으로 필수 맥락을 수집하는 구조화된 질문
- **외과적 그래프 갱신** — 변경된 문서만 반영, 기존 요약은 보존
- **볼트 전체 배치 모드** — Agent tool로 3~5개 프로젝트 동시 처리

## 연동 스킬

- **[skill-builder](https://github.com/jasonnamii/skill-builder)** — 스킬 생성·수정 담당. project-updater는 스킬 생성에 관여하지 않음
- **[up-manager](https://github.com/jasonnamii/up-manager)** — CLAUDE.md 초기 생성 후 갱신은 UP §H 규칙으로 처리

## 설치

```bash
git clone https://github.com/jasonnamii/project-updater.git ~/.claude/skills/project-updater
```

## 업데이트

```bash
cd ~/.claude/skills/project-updater && git pull
```

`~/.claude/skills/`에 배치된 스킬은 Claude Code 및 Cowork 세션에서 자동으로 사용 가능합니다.

## Cowork Skills

25개 이상의 커스텀 스킬 중 하나입니다. 전체 카탈로그: [github.com/jasonnamii/cowork-skills](https://github.com/jasonnamii/cowork-skills)

## 라이선스

MIT License — 자유롭게 사용, 수정, 공유 가능합니다.
