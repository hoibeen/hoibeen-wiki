---
id: operation-context7-instruction-guide
title: context7 사용 가이드
aliases: [context7 사용 가이드]
type: operation
status: active
created_at: 2026-10-19
created_by: 정회석
updated_at: 2026-10-19
updated_by: 정회석
audit_log:
  - action: created
    at: 2026-10-19
    by: 정회석
    note: "hoibeen 위키 신설"
tags: [common, operation, context7, mcp, docs]
stack: common
scope: context7-instruction
source:
  - "https://context7.com, https://github.com/upstash/context7"
  - "hoibeen 위키 신설, 2026-10-19"
relations:
  - id: operation-wiki-authoring-guide
    label: related
---
# Context7 사용 가이드

## 한 줄 요약

버전별 라이브러리·프레임워크 문서는 Context7으로 조회하고, 위키에는 hoibeen에서 채택한 기준과 이유를 남깁니다. 최신 문서와 현재 프로젝트 버전의 문서를 구분합니다.

## 연결 확인

- 사용하는 에이전트의 MCP 등록·연결 상태 또는 실제 도구 호출로 확인합니다. 등록 목록에 보이는 것만으로 정상 연결을 단정하지 않습니다.
- 미설정이면 [Context7 공식 안내](https://github.com/upstash/context7)의 해당 에이전트 설치 절차를 확인합니다. 이미 연결된 환경은 재설치하지 않습니다.
- 설치 후 실제 조회로 재확인합니다. 연결 실패 시 원인과 문서 조회 한계를 보고합니다. 공식 문서를 직접 확인했다면 조회 경로를 남기고 Context7 결과처럼 쓰지 않습니다.

## 조회 순서

1. 프로젝트의 패키지 버전·lockfile·질문 범위를 확인합니다.
2. `resolve-library-id`로 공식 문서에 맞는 라이브러리 ID를 찾고 `query-docs`로 필요한 주제와 버전을 조회합니다. 도구 이름은 에이전트에 노출된 실제 이름을 따릅니다.
3. 해당 버전이 제공되지 않거나 결과가 부족하면 버전을 명시해 공식 문서를 확인합니다. 최신 예제를 구버전에 맞는 것처럼 적용하지 않습니다.
4. 조회한 라이브러리·버전·출처를 판단 근거로 남깁니다. 사용법 원문을 위키에 복제하지 않습니다.

## 역할 분리

| 대상 | 보관·조회 내용 |
|---|---|
| hoibeen-wiki | hoibeen 공통 기준·선택 이유·재사용할 컨벤션 |
| 소비 프로젝트 지침·worklog | 해당 프로젝트의 실제 결정·설정·검증 |
| Context7·공식 문서 | 버전별 API·사용법·지원 조건 |

Context7은 문서 조회 도구이며 프로젝트 설정이나 지원 여부를 대신 검증하지 않습니다. 판단을 위키에 남길 때는 공식 사실과 hoibeen의 선택을 구분합니다.

## 관련 문서

- [[wiki-authoring-guide]]
- [[project-wiki-guide]]

## 출처

- [Context7](https://context7.com)
- [Context7 공식 저장소](https://github.com/upstash/context7)
- 2026-09-23 이 환경의 `resolve_library_id`·`query_docs` 실제 호출로 연결 확인.
