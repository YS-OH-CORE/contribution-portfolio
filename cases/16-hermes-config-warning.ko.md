# 16 · 설정을 읽지 못했을 때, 실패를 조용히 숨기지 않도록

**Hermes Agent · 우리 수정이 관리자 통합 PR에 포함되어 main에 병합**

[전체 공개 사례](../README.md#전체-공개-사례) · [영석과 제로의 메인](https://github.com/YS-OH-CORE) · [English summary](#english-summary)

**Zero × Youngseok Oh** · 공개 근거 확인: 2026-10-27 KST

## 문제

설정 파일을 읽지 못했는데도 기존 기본값으로 조용히 진행하면, 사용자는 자신이 고른 기억·프롬프트 캐시·추론 관련 설정이 적용됐다고 오해할 수 있습니다. 나중의 설정 읽기가 성공했다고 해서 앞선 읽기 실패가 사라지는 것도 아닙니다.

## 우리가 보탠 것

YS-OH-CORE가 작성한 [PR #125960](https://github.com/NousResearch/hermes-agent/pull/125960)은 기존 대체 동작을 유지하면서 각 설정 읽기 경계의 실패를 알리고, 초기 로그 기록이 실제 파일에 도달하도록 보완했습니다. 예외의 종류와 실패한 경계는 알리되 개인 설정값, 예외 메시지, 추적 정보는 경고에 넣지 않도록 했습니다.

원래 제출과 10월 4일 보완의 실행 범위는 해당 PR에 남아 있습니다. 그 기록의 114개 통과는 당시 초기화 경로와 주변 검사의 결과이며, 이번 공개 정리에서 검사를 새로 돌린 숫자가 아닙니다. 실제 모델 대화나 전체 제품의 무결점도 뜻하지 않습니다.

## 외부에서 확인된 결과

관리자 **teknium1**의 [통합 PR #144257](https://github.com/NousResearch/hermes-agent/pull/144257)은 설명에 #125960과 YS-OH-CORE를 명시하고, 원래 작성자 표시를 유지한 커밋으로 가져왔다고 적었습니다. 통합 PR은 **2026-10-25 10:01:27 UTC, 한국시간 19:01:27에 main으로 병합**됐습니다.

- [통합 PR의 기여 표기와 병합 기록](https://github.com/NousResearch/hermes-agent/pull/144257)
- [병합 커밋 1d258cc6](https://github.com/NousResearch/hermes-agent/commit/1d258cc6c23b2d6db1ed63f551cf9267d6d471ac)
- [우리 원래 PR과 당시 검증 범위](https://github.com/NousResearch/hermes-agent/pull/125960)

**원래 #125960 자체는 미병합 종료입니다.** 따라서 이 사례를 “우리 PR 자체가 병합됐다”로 표시하지 않습니다. 확인한 결과는 **우리의 설정 실패 경고 작업을 포함한다고 명시한 관리자 통합 PR의 병합**입니다.

## 기여의 경계

우리 범위는 설정 읽기 실패의 진단과 관련 검사입니다. 통합 PR 전체의 플러그인 복구, 의존성 처리, 자동 재활성화, 다른 기여자의 수정까지 우리의 단독 작업으로 소개하지 않습니다. 통합과 다른 기능은 teknium1 및 해당 기여자들의 작업입니다.

이번에 새로 확인한 것은 공개된 기여 연결과 병합 상태입니다. 병합 결과 전체를 재검증하거나 배포판 출시·사용자 PC 적용을 확인한 것은 아닙니다. 한 협업을 원래 PR과 통합 PR로 나누어 두 건으로 세지 않습니다.

## English summary

Our authored PR #125960 made configuration-read failures visible while retaining existing fallback behavior and keeping private configuration values out of diagnostics. Maintainer teknium1 explicitly included that work, retaining original commit authorship, in integration PR #144257, merged into main on 25 October 2026.

The original PR was closed without being merged directly. This is **one contribution incorporated through a merged integration PR**, not two merges or authorship of the integration's entire plugin-recovery feature. Historical tests describe their original revision; this publication did not rerun the merged tree or verify a release.

Youngseok Oh contributes questions, direction and corrections; Zero contributes substantial AI-assisted analysis, implementation, verification and writing. External authors retain their work.
