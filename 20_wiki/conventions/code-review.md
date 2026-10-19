---
id: convention-code-review
title: 코드 리뷰
aliases: [코드 리뷰]
type: convention
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
tags: [frontend, code-review, code-quality, readability, predictability, cohesion, coupling, a11y]
stack: common
scope: code-review
source:
  - "Toss Frontend Fundamentals"
  - "hoibeen 위키"
relations:
  - id: convention-naming-convention
    label: depends-on
  - id: operation-commit-convention
    label: depends-on
  - id: operation-mr-pr-guide
    label: depends-on
---

# 코드 리뷰

코드를 짜거나 리뷰할 때 지키는 기준. 좋은 코드는 결국 **변경하기 쉬운 코드**를 뜻한다.

## 1. 코드 품질 4기준과 트레이드오프

4가지를 동시에 완벽하게 채울 수는 없다. **"장기적으로 수정하기 쉬운가"**를 기준으로 판단한다.

- **가독성**: 한 번에 고려할 맥락이 적고, 위에서 아래로 자연스럽게 읽히는가.
  - 같이 실행되지 않는 코드는 분기별로 쪼개고, 복잡한 조건이나 매직 넘버는 이름을 붙인다 (`canPurchase`, `PAGE_SIZE`).
  - 단, 위험이 낮다면 과한 추상화보다 중복을 허용해 가독성을 챙긴다.
- **예측 가능성**: 이름, 파라미터, 반환값만 보고 동작을 알 수 있는가.
  - 라이브러리 이름과 겹치는 래퍼를 만들지 않고(`http` 대신 `httpService`), 숨은 부수효과(side effect)를 함수 안에 숨기지 않는다.
- **응집도**: 함께 수정되어야 할 코드가 같은 곳에 모여 있는가.
  - 함께 바뀌는 파일은 같은 디렉토리에 두고, 두 기능이 다르게 발전할 가능성이 높다면 억지로 공통화하지 않고 중복을 둔다.
- **결합도**: 코드를 고쳤을 때 영향 범위가 좁은가.
  - 책임이 큰 훅은 쪼개고, 깊은 Prop Drilling은 Composition(`children`)이나 Context로 푼다. Context는 테마·로케일·인증 같은 진짜 전역 관심사에만 쓴다.

## 2. 접근성 (a11y)

프론트엔드가 만드는 HTML 구조와 인터랙션의 기본값이다.

- **스크린리더 순서**: 역할(Role) → 레이블(Label) → 상태(State) 순으로 읽히는지 확인한다.
- **핵심 원칙**:
  - 버튼 안에 버튼을 넣지 않는다.
  - 클릭 가능한 요소는 가짜 버튼(`<div onclick>`) 대신 진짜 `<button>`이나 `<a>`를 쓴다.
  - 시각 정보에만 의존하지 않고 `alt`나 텍스트를 보완한다.
- 테스트는 `getByRole`을 우선 사용한다.

## 3. 디버깅 원칙

감으로 고치지 않고 체계적으로 접근한다.

1. **진단**: 에러 메시지만 보고 추측하지 말고 호출·의존 관계를 좁혀 원인을 특정한다.
2. **수정**: 증상만 막는 임시방편을 피하고 근본 원인을 고친다. 비즈니스 로직은 순수 함수로 분리해 독립 테스트가 가능하게 만든다.
3. **예방**: 버그의 원인, 재현 조건, 수정 근거를 작업 기록에 남겨 재발을 막는다.
