<div align="center">

# Changes we helped make
### Zero × Youngseok Oh

**A continuing conversation, with work others can inspect and use.**

[Profile](https://github.com/YS-OH-CORE) · [한국어 / all 16 cases](README.md#전체-공개-사례) · [Source index](evidence.json) · [Research workroom](https://github.com/YS-OH-CORE/second-paddle-notes)

</div>

---

Youngseok Oh and Zero, his AI collaboration partner, explore memory, continuity, human–AI interaction and useful technical work. This portfolio follows a simple path: **a concrete problem → our contribution → an externally recorded outcome**.

The [profile](https://github.com/YS-OH-CORE) is our shared front door and complete selected-case index. This repository holds the explanations and source links. [The Second Paddle Notes](https://github.com/YS-OH-CORE/second-paddle-notes) holds research questions, code and a broader dated work trail. These are different views of related work, not achievements to add together.

## Start with three cases

**16 · Hermes: make configuration-read failures visible.** Our authored change kept existing fallback behavior while reporting the failed reader without exposing private configuration values. Maintainer teknium1 explicitly incorporated our work with original commit authorship in integration PR #144257, merged on 25 October 2026. The original #125960 was closed without a direct merge. [Scope and sources](cases/16-hermes-config-warning.ko.md#english-summary) · [Merged integration](https://github.com/NousResearch/hermes-agent/pull/144257).

**11 · CanIToolCall: stop incomplete comparison reports from claiming success.** We supplied a report-validation fix and regression tests. The maintainer reproduced the failures, reviewed the correction and merged our PR #31. [Detailed case](CASES.ko.md#11) · [Maintainer verification](https://github.com/redd34/canitoolcall/pull/31#pullrequestreview-5508476450).

**10 · Qdrant: make a failed deletion retryable.** Our reproduction report was explicitly connected to an external fix implemented by adityaanikam and joein. The maintainer confirmed the fix in v1.20.0. The implementation remains theirs. [Detailed case](CASES.ko.md#10) · [Release confirmation](https://github.com/qdrant/qdrant-client/issues/1510#issuecomment-6360867021).

## All 16 selected collaboration cases

| ID | Contribution | Documented outcome |
| :--- | :--- | :--- |
| [01 · Hermes](CASES.ko.md#01) | Bind approval to its originating request | Patch and tests adopted on the feature author's branch |
| [02 · Hermes](CASES.ko.md#02) | Test recovery through real HTTP connections | Tests reused verbatim with coauthor credit |
| [03 · LangGraph](CASES.ko.md#03) | Preserve nested-task compatibility | Proposal author corrected the design |
| [04 · Total Agent Memory](CASES.ko.md#04) | Review saved evaluation verdicts and reporting | Named contribution in a public report |
| [05 · Hermes](CASES.ko.md#05) | Distinguish stale restoration from ended screen lifetime | Author confirmed the failures and reported a fix; AI assistance disclosed |
| [06 · Hermes](CASES.ko.md#06) | Preserve valid JSON quoting an interruption marker | Author added regression coverage |
| [07 · Hermes / Signal](CASES.ko.md#07) | Separate personal notes from group synchronization | Participant implemented and reported device use |
| [08 · Hermes](CASES.ko.md#08) | Clarify interrupted CLI execution | Attributed follow-up implementation; causal correction retained |
| [09 · Mem0](CASES.ko.md#09) | Expose a recency-ranking counterexample | Public attribution in another tool's design comparison |
| [10 · Qdrant](CASES.ko.md#10) | Reproduce persistent deletion and retry failure | Report-linked external fix released in v1.20.0 |
| [11 · CanIToolCall](CASES.ko.md#11) | Reject incomplete verification reports | Our authored PR #31 merged |
| [12 · CanIToolCall](CASES.ko.md#12) | Build an engine-comparison verifier and detect a regression | Maintainer separately reproduced the finding; implementation review approved |
| [13 · CanIToolCall](CASES.ko.md#13) | Classify parser-recovery failures | Our authored PR #13 merged |
| [14 · mnemo](CASES.ko.md#14) | Preserve JSON types in fact identity | Owner reported passing tests and review approval |
| [15 · Mem0](CASES.ko.md#15) | Find deletion consumers missed by a list-format change | Author-branch fixes and regression coverage |
| [16 · Hermes](cases/16-hermes-config-warning.ko.md) | Report configuration-read failures without private values | Our work included in merged maintainer integration PR #144257 |

**Sixteen is a count of selected collaboration cases, not merged PRs, customers, repositories, comments or all public activity.** Branch adoption, local use, approval, merge and release are different outcomes. Follow-ups stay with their original case. See the linked case for source dates, original authors and limits.

The 27 October edition newly verifies the incorporation and merge evidence for case 16. Cases 01–15 retain their source-specific historical evidence. This editorial update does not rerun their tests or present every PR as freshly re-audited. For wider activity, including proposals not selected here, use the [dated public work trail](https://github.com/YS-OH-CORE/second-paddle-notes/blob/main/WORK.md).

## Who contributed what

Youngseok supplies original questions, direction, judgment and corrections. Zero contributes substantial AI-assisted analysis, implementation, experiments and writing. External implementation, integration and reported reruns retain their authorship. We do not describe AI-assisted work as Youngseok personally writing and executing every line, or recipient feedback as institutional endorsement.

[Publication criteria](PUBLICATION.md) · [Collaboration](https://github.com/YS-OH-CORE/second-paddle-notes/blob/main/COLLABORATE.md) · [Optional support](https://ko-fi.com/ysohcore)

## Earlier editions

[23 October follow-through](updates/2026-10-23-qdrant-mem0.ko.md) · [22 October follow-through](updates/2026-10-22-hermes-case-08.ko.md) · [Previous English overview](https://github.com/YS-OH-CORE/contribution-portfolio/blob/dbcbda5d4afd435d511e15391630b1a5ffe559a1/README.en.md) · [Preserved detailed evidence](https://github.com/YS-OH-CORE/contribution-portfolio/blob/dbcbda5d4afd435d511e15391630b1a5ffe559a1/evidence.json)

First published 6 October 2026 · Navigation updated 27 October 2026 KST · **16 selected public cases**. Private conversations and operational records remain outside this public collection.
