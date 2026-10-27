<div align="center">

# 함께 만든 변화
### Zero × Youngseok Oh

**질문을 주고받다가, 다른 사람에게도 쓸모 있는 변화가 남았습니다.**

[영석과 제로의 메인](https://github.com/YS-OH-CORE) · [English](README.en.md) · [전체 16개 사례](#전체-공개-사례) · [공개 근거 색인](evidence.json)

</div>

---

이곳은 영석과 AI 협업 파트너 제로가 **문제를 찾고, 재현하고, 다른 사람의 작업에 보탠 기록**입니다. 단순한 제출이나 우리끼리의 평가는 성과로 세지 않습니다. 작성자의 반영, 실제 사용 보고, 검토 승인, 병합, 기여 표기처럼 공개 원문에서 확인할 수 있는 결과를 연결합니다.

**처음 오셨다면:** 아래 세 사례를 먼저 읽고, 궁금한 항목의 상세 설명과 원문으로 이어가세요. 우리 소개와 전체 목차는 [GitHub 프로필 메인](https://github.com/YS-OH-CORE)에, 실험 코드와 연구 원자료는 [The Second Paddle Notes](https://github.com/YS-OH-CORE/second-paddle-notes)에 있습니다. 서로 다른 업적을 중복해서 세는 세 개의 목록이 아닙니다.

## 먼저 볼 세 가지

### 16 · 실패했는데 조용히 넘어가지 않도록

**Hermes · 우리 수정이 관리자 통합 PR에 포함되어 병합**

설정 읽기가 실패하면 사용자가 고른 기억·추론 설정이 적용되지 않을 수 있습니다. 기존 대체 동작은 유지하되, 개인 설정값을 노출하지 않고 실패한 지점을 알리는 수정과 검사를 제공했습니다. 관리자는 우리 PR을 원래 작성자 표시와 함께 가져왔다고 명시했고, 통합 PR은 main에 병합됐습니다. 원래 우리 PR 자체의 직접 병합과는 구별합니다.

[사례와 정확한 기여 범위](cases/16-hermes-config-warning.ko.md) · [관리자 통합·병합 기록](https://github.com/NousResearch/hermes-agent/pull/144257)

### 11 · 검사 결과가 빠졌는데도 ‘정상’이 되는 오류

**CanIToolCall · 운영자 재현·승인, 우리 수정 병합**

수정 전후 비교 보고서에 결과가 빠지거나 중복돼도 성공으로 처리되던 문제를 고쳤습니다. 운영자가 원래 실패와 수정 결과를 다시 확인하고 변경을 병합했습니다.

[사례 자세히](CASES.ko.md#11) · [운영자의 전후 대조](https://github.com/redd34/canitoolcall/pull/31#pullrequestreview-5508476450) · [병합된 PR](https://github.com/redd34/canitoolcall/pull/31)

### 10 · 실패한 삭제를 다시 시도할 수 있도록

**Qdrant · 우리 신고에 연결된 외부 수정, v1.20.0 배포**

삭제 중 실패한 데이터가 조회에서만 사라져 재시도하기 어려워지는 조건을 재현했습니다. adityaanikam과 joein이 수정·통합했고, 관리자가 배포판의 해결을 확인했습니다. 최종 구현은 해당 개발자들의 기여입니다.

[사례 자세히](CASES.ko.md#10) · [관리자 배포 확인](https://github.com/qdrant/qdrant-client/issues/1510#issuecomment-6360867021)

## 전체 공개 사례

**16개는 선별한 협업 사례 수입니다.** 병합 PR 16개, 독립 결함 16개, 고객 16명이라는 뜻이 아닙니다. 같은 작업의 댓글·후속 검사·통합 PR을 따로 더하지 않습니다. 사례 번호는 기존 기록과 연결되도록 유지합니다.

| 사례 | 우리가 보탠 것 | 공개 원문으로 확인되는 결과 |
| :--- | :--- | :--- |
| [01 · Hermes](CASES.ko.md#01) | 승인과 원래 요청의 연결을 보존하는 패치·검사 | [작성자 브랜치에 그대로 반영](https://github.com/NousResearch/hermes-agent/pull/22982#issuecomment-5643327201) |
| [02 · Hermes](CASES.ko.md#02) | 실제 HTTP 연결로 복구 조건을 구별한 검사 | [검사 재사용·공동 저작 표기](https://github.com/NousResearch/hermes-agent/pull/121944#issuecomment-5863926910) |
| [03 · LangGraph](CASES.ko.md#03) | 중첩 작업의 기존 호환성 규칙 검토 | [제안 작성자가 설계 교정](https://github.com/langchain-ai/langgraph/issues/9072#issuecomment-5980134186) |
| [04 · Total Agent Memory](CASES.ko.md#04) | 저장된 평가 판정과 보고 표현 검토 | [공개 보고서에 영석·제로 기여 명시](https://github.com/vbcherepanov/total-agent-memory/commit/55d0ab0124ca4fca81479a5bcafa262aaaf0e19e) |
| [05 · Hermes](CASES.ko.md#05) | 늦게 온 복원 응답이 새 선택을 덮는 조건 검토 | [작성자가 실패 확인·수정 보고](https://github.com/NousResearch/hermes-agent/pull/130126#issuecomment-5932499656) |
| [06 · Hermes](CASES.ko.md#06) | 중단 표시를 인용한 정상 JSON의 경계 제시 | [작성자가 회귀검사 추가](https://github.com/NousResearch/hermes-agent/pull/107809#issuecomment-5931462372) |
| [07 · Hermes / Signal](CASES.ko.md#07) | 개인 메모와 그룹 동기화를 분리하는 설정 제안 | [참여자가 구현·기기 실사용 확인](https://github.com/NousResearch/hermes-agent/issues/121970#issuecomment-5823143850) |
| [08 · Hermes](CASES.ko.md#08) | 명령줄 중단 안내의 조건·위치·문구 검토 | [후속 구현에서 기여 표기](https://github.com/NousResearch/hermes-agent/pull/133858) · [정정·후속 이력](updates/2026-10-22-hermes-case-08.ko.md) |
| [09 · Mem0](CASES.ko.md#09) | 검색 순위가 뒤집히는 반례 제시 | [다른 도구 작성자가 설계 비교에 인용](https://github.com/mem0ai/mem0/issues/7535#issuecomment-5992249148) |
| [10 · Qdrant](CASES.ko.md#10) | 실패한 영구 삭제의 재시도 문제 재현·신고 | [연결된 외부 수정이 v1.20.0에 배포](https://github.com/qdrant/qdrant-client/issues/1510#issuecomment-6360867021) |
| [11 · CanIToolCall](CASES.ko.md#11) | 불완전한 검증 보고서의 거짓 성공 수정 | [우리 PR #31 병합](https://github.com/redd34/canitoolcall/pull/31) |
| [12 · CanIToolCall](CASES.ko.md#12) | 실제 엔진 비교 검증기와 회귀 발견 | [운영자 별도 재현·기여 표기](https://github.com/redd34/canitoolcall/issues/37), 구현 승인 기록 |
| [13 · CanIToolCall](CASES.ko.md#13) | 비슷해 보이는 파서 복구 실패의 원인 분류 | [우리 PR #13 병합](https://github.com/redd34/canitoolcall/pull/13) |
| [14 · mnemo](CASES.ko.md#14) | 숫자와 문자열의 기억 식별 충돌 수정 | [소유자 검사 통과 보고·승인](https://github.com/sattyamjjain/mnemo/pull/204#issuecomment-6096480334) |
| [15 · Mem0](CASES.ko.md#15) | 목록 형식 변경이 놓친 동기·비동기 삭제 경로 검토 | [작성자 브랜치의 두 경로·검사 수정](https://github.com/mem0ai/mem0/pull/7647#issuecomment-6347118756) |
| [16 · Hermes](cases/16-hermes-config-warning.ko.md) | 개인 설정을 노출하지 않는 설정 읽기 실패 경고 | [우리 작업을 포함한 관리자 통합 PR #144257 병합](https://github.com/NousResearch/hermes-agent/pull/144257) |

**읽는 기준:** 브랜치 반영·사용 보고·승인은 병합과 다르고, 병합은 배포와 다릅니다. 표는 입증된 사건을 요약하며 모든 PR의 실시간 상태판은 아닙니다. 각 상세 글의 작성일·확인 판본·남은 범위를 함께 봅니다. 2026-10-27 정리에서는 사례 16의 연결·병합을 새로 확인했고, 01~15의 과거 검사를 다시 실행한 것으로 세지 않았습니다.

## 우리와 원자료

영석은 질문과 방향, 판단과 교정을 보탭니다. 제로는 AI 협업 파트너로서 상당한 분석·구현·실험·집필을 수행합니다. 둘의 역할을 지우지 않고, 다른 개발자의 구현·통합·재실행은 그 작성자의 공로로 남깁니다.

[우리 이야기와 연구 작업실](https://github.com/YS-OH-CORE/second-paddle-notes) · [더 넓은 공개 작업 이력](https://github.com/YS-OH-CORE/second-paddle-notes/blob/main/WORK.md) · [공개·갱신 기준](PUBLICATION.md) · [활동 후원](https://ko-fi.com/ysohcore)

모든 공개 활동이 이 선별집의 사례 수에 포함되지는 않습니다. 진행 중인 제안과 더 넓은 검토 기록은 공개 작업 이력에서 날짜와 함께 읽을 수 있습니다. 사적인 대화·계정 정보·비공개 운영 자료는 공개하지 않습니다.

## 이전 판본과 후속

[23일 Qdrant·Mem0 후속](updates/2026-10-23-qdrant-mem0.ko.md) · [22일 Hermes 후속](updates/2026-10-22-hermes-case-08.ko.md) · [정리 전 첫 화면](https://github.com/YS-OH-CORE/contribution-portfolio/blob/dbcbda5d4afd435d511e15391630b1a5ffe559a1/README.md) · [이전 상세 근거 색인 원문](https://github.com/YS-OH-CORE/contribution-portfolio/blob/dbcbda5d4afd435d511e15391630b1a5ffe559a1/evidence.json)

첫 공개 2026-10-06 · 공개 목차 정리 2026-10-27 · **16개 선별 사례**. 원자료와 기존 사례 번호는 이어집니다.
