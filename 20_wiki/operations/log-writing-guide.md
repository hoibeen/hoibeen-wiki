---
id: operation-log-writing-guide
title: 로그 작성 규칙
aliases: [로그 작성 규칙]
type: operation
status: active
created_at: 2026-10-19
created_by: 정회석
updated_at: 2026-10-19
updated_by: 정회석
last_verified_at: 2026-09-23
last_verified_by: 정회석
audit_log:
  - action: created
    at: 2026-10-19
    by: 정회석
    note: "hoibeen 위키 신설"
tags: [common, operation, wiki, log]
stack: common
scope: log-authoring
source:
  - "hoibeen 위키 신설, 2026-10-19"
relations:
  - id: operation-wiki-authoring-guide
    label: related
  - id: operation-wiki-versioning
    label: related
  - id: operation-project-wiki-guide
    label: related
---
# 로그 작성 규칙

## 한 줄 요약

hoibeen-wiki의 새 기록은 `docs/worklog/YYYY-MM/YYYY-MM-DD-<주제>-<식별자>.md`에 변경 단위로 남깁니다. 메타데이터·본문·조회 순서는 [[worklog-writing-guide]]를 따릅니다.

## 이 위키에 적용

- [AGENTS.md](/AGENTS.md)가 요구하는 문서 변경·채택된 결정·새 검증 결과·후속 조치가 필요한 발견을 기록합니다. 단순 조회·설명·상태 확인은 기록하지 않습니다.
- 같은 변경의 미병합 기록을 재사용합니다. 별도 후속 결과는 날짜를 붙여 아래에 추가하며, 병합된 기록은 수정하지 않습니다.
- 루트 [README.md](/README.md)는 저장소 소개, [docs/worklog/README.md](/docs/worklog/README.md)는 작성·조회 안내입니다. 개별 기록 목록이나 누적 요약을 매번 갱신하지 않습니다.
- 지식 분류는 `/20_wiki/`와 [20_wiki/index.md](/20_wiki/index.md)로 유지합니다. 개별 worklog를 index 목차에 등록하지 않습니다.

## 남길 내용

- 변경 문서·이유·선택 근거·검증 결과와 한계를 남깁니다. 분량보다 나중에 판단을 재구성할 수 있는지가 기준입니다.
- `scope`는 `wiki-operations`처럼 주된 영역, `topics`는 검색어를 씁니다. 문서만 바꿨다면 `code_paths: []`로 두고 본문에 문서 링크를 남깁니다.
- 기록만 바꾸면 버전은 `none`입니다. 규칙·구조가 바뀌면 [[wiki-versioning]]에 따라 같은 변경에서 버전을 갱신하고 이전·새 버전과 이유를 기록합니다.
- 과거 기록은 당시 맥락입니다. 현재 정책은 최신 지침, 기술 사실은 공식 문서와 실제 코드로 확인합니다. 근거가 부족하면 연결된 원문이나 `/10_raw/`의 관련 자료만 찾습니다.

## 기록 시작점

2026-10-19 hoibeen 위키로 신설하며 기록을 새로 시작했습니다. 이전 저장소의 기록은 가져오지 않았습니다. 조회는 [docs/worklog/README.md](/docs/worklog/README.md)를 따릅니다.

일반 프로젝트의 전환·삭제는 [[project-wiki-guide]]를 따릅니다. 작업 완료 시 주간·월간 자동 압축을 요구하지 않습니다.

## 관련 문서

- [[worklog-writing-guide]]
- [[project-wiki-guide]]
- [[wiki-versioning]]
- [[wiki-authoring-guide]]

## 출처

- hoibeen 위키 신설, 2026-10-19.
