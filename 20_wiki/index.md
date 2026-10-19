---
id: index-index
title: 목차
aliases: [목차]
type: index
status: active
version: "1.0.0"
created_at: 2026-10-19
created_by: 정회석
updated_at: 2026-10-19
updated_by: 정회석
audit_log:
  - action: created
    at: 2026-10-19
    by: 정회석
    note: "hoibeen 위키 신설"
tags: [wiki, index]
stack: common
scope: wiki-index
source:
  - "hoibeen 위키 신설, 2026-10-19"
relations: []
---
# hoibeen-wiki

hoibeen 개발 지식과 판단 기준의 진입점입니다. 실제 프로젝트의 지침을 우선합니다.

## 시작 전 필수

1. **원격 상태 확인**: [[wiki-sync]]에 따라 GitHub Release·`origin/main`·현재 버전을 비교합니다. 작업 중 미발행 버전과 동기화 누락을 구분합니다.
2. **Context7 연결 확인**: [[context7-instruction-guide]]에 따라 연결을 확인합니다. 라이브러리 문서는 대상 버전에 맞춰 조회합니다.
3. **Conventions·Operations 선행 학습**: 아래 문서를 직접 읽습니다. hoibeen 프로젝트에 적용할 때는 그 프로젝트의 지침·도구·지원 범위를 먼저 확인합니다.

저장소 운영 규칙은 [AGENTS.md](/AGENTS.md)가 기준입니다.

## 구조

```text
00_context/          글쓰기·사고방식 기준
10_raw/              원본 보관소
20_wiki/
  ├ principles/      원칙·기술 선택 기준
  ├ conventions/     개발 전용 규칙
  ├ operations/      작성·Git·에이전트 운영
  └ index.md         이 목차
docs/worklog/
  ├ README.md        작성·조회 안내
  └ YYYY-MM/
      └ YYYY-MM-DD-<주제>-<식별자>.md
README.md            저장소 소개
```

분류는 아래 목차가 기준입니다. 지식 폴더는 세 개를 유지합니다. 라이브러리·프레임워크의 버전별 사용법은 저장하지 않고 Context7으로 조회하며, 선택 기준과 이유만 남깁니다.

## Principles

- [[expo-sdk-version]]: hoibeen 앱의 안정 SDK 선택·development build 판단 기준. `[앱]`

## Conventions

개발에 적용하는 공통 기준입니다. 도구 설정 예시는 대상 프로젝트의 호환성을 확인해 적용합니다.

- [[naming-convention]]: 파일·식별자 네이밍.
- [[lint-format]]: ESLint·Prettier 역할 분리와 hoibeen 프로젝트 기본 설정.
- [[git-hooks]]: Husky·nano-staged·typecheck, 코드 프로젝트의 커밋·push 검증.
- [[package-manager]]: hoibeen JS/TS 프로젝트 pnpm 기본값과 기존 매니저 존중.
- [[node-version]]: Node LTS 선택·프로젝트 버전 고정.
- [[code-review]]: 코드 품질 4기준·접근성·디버깅 판단.

## Operations

개발 외에도 사용하는 작성·운영 기준입니다.

- [[commit-convention]]: 한국어 `type(scope): subject` 커밋 메시지.
- [[mr-pr-guide]]: GitHub PR·GitLab MR 작성과 hoibeen 위키 PR 템플릿.
- [[branch-strategy]]: 이 위키의 `main` 운영과 hoibeen 프로젝트의 `main`·`dev` 구분.
- [[context7-instruction-guide]]: 라이브러리 문서 조회와 위키의 역할 분리.
- [[wiki-authoring-guide]]: 파일명·frontmatter·출처·링크 표준.
- [[log-writing-guide]]: hoibeen 위키 worklog 적용과 기록 시작점.
- [[worklog-writing-guide]]: 변경 단위 기록·경량 메타데이터·선택적 조회.
- [[wiki-versioning]]: 기록 전용 변경 제외·같은 변경에서 버전 확정·요청된 tag와 Release 발행.
- [[wiki-sync]]: 로컬·`origin/main`·GitHub Release 비교.
- [[project-wiki-guide]]: hoibeen 프로젝트의 기록 도입·전환·원문 보존.
- [[agent-instruction-guide]]: 프로젝트 지침·위키 연동·도구 활용.

## 기록 조회

모든 기록은 `/docs/worklog/`에서 조회합니다. 작성·검색은 [docs/worklog/README.md](/docs/worklog/README.md)를 따르며, 개별 기록은 이 목차에 추가하지 않습니다.
