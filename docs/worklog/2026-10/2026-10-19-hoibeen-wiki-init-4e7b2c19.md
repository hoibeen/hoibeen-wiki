---
id: worklog-4e7b2c19
title: hoibeen 위키 신설
scope: wiki-operations
authors: [정회석]
created_at: 2026-10-19
updated_at: 2026-10-19
topics: [wiki-init, versioning]
code_paths: []
related: []
---

# hoibeen 위키 신설

## 변경과 이유

- 개인 개발 위키의 문서 구조와 기준을 바탕으로 hoibeen 프로젝트 공용 위키를 신설했습니다.
- 저장소명·심볼릭링크·위키 실체 경로를 `hoibeen-wiki`, `~/hoibeen-wiki`로, 원격을 `https://github.com/hoibeen/hoibeen-wiki.git`으로 맞췄습니다.
- 개인 위키·개인 프로젝트 기준 문구를 hoibeen 프로젝트 기준으로 바꿨습니다.
- `.obsidian/` 설정, 이전 작업 기록, `/10_raw/` 회의록 원문을 제외하고, 각 문서의 `audit_log`·작성일을 신설일로 초기화했습니다.
- `code-review`는 code-review-graph 실행 절차를 빼고 품질 4기준·접근성·디버깅 원칙만 남겼습니다. `/00_context/`의 글쓰기·사고 기준은 AI 티 금지 항목과 예시를 보강했습니다.
- PR 템플릿 `.github/pull_request_template.md`를 `10_raw/merge_request_templates/Default.md` 양식으로 바꾸고 [[mr-pr-guide]]에 둘의 관계를 적었습니다.
- 운영 기준선을 갖춘 상태로 시작하므로 `index.version`을 `1.0.0`으로 정했습니다.

## 검증과 한계

- `[[링크]]` 대상 파일 존재 여부를 확인했습니다.
- 외부 문서 확인일(`2026-09-23 확인` 등)은 실제 조회일이라 유지했습니다. 최신 여부는 다시 확인하지 않았습니다.
