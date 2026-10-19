# Changes we helped make
## Zero × Youngseok Oh

**Find the failure. Make it reproducible. Help someone make a better change.**

[한국어](README.md) · [All 14 cases](CASES.ko.md) · [Public source index](evidence.json) · [Support the work](https://ko-fi.com/ysohcore)

## Fourteen selected contributions

Merged fixes, findings another developer reproduced, tests reused with credit, and reviews that changed a design. Each case connects a concrete problem to our contribution and the recipient's recorded response.

The collection includes different outcomes: a merged change, a patch adopted on an author's branch, an approved contribution awaiting merge, or explicitly credited analysis. Each is labeled where it appears.

## Start with these six

### 11 · Stop incomplete comparisons from reporting success

**CanIToolCall · Our fix merged into main**

A before-and-after comparison could report success even when its results were missing, duplicated, or otherwise incomplete. We reported the failure and supplied report validation with 54 regression and control cases. Maintainer **redd34** reported reproducing the original failures and rerunning the corrected tests, then approved and merged PR #31 on 14 October KST.

[Read the case](CASES.ko.md#11) · [Maintainer's verification](https://github.com/redd34/canitoolcall/pull/31#pullrequestreview-5508476450) · [Merged PR](https://github.com/redd34/canitoolcall/pull/31)

### 12 · Catch a regression hidden beside two improvements

**CanIToolCall · Finding reproduced by the owner; verifier approved, awaiting merge**

We built a verifier that separately builds and compares the original and proposed revisions of Ollama and llama.cpp. An actual Ollama comparison found two improvements alongside a new parser regression. **redd34** reproduced the finding with a separate build and credited our work, then approved the verifier after four requested corrections. The approved revision remains unmerged; the actual engine runs belong to the earlier revision, not a fresh engine rebuild of the approved code.

[Read the case](CASES.ko.md#12) · [Owner's separate reproduction and credit](https://github.com/redd34/canitoolcall/issues/37) · [Approval after corrections](https://github.com/redd34/canitoolcall/pull/33#pullrequestreview-5543659056)

### 10 · Make a failed deletion recoverable on retry

**Qdrant client · Our report linked to a merged external fix**

Using a real SQLite store, we reproduced a partial deletion that hid surviving records from a retry, allowing them to reappear after reopening the collection. PR #1515 explicitly linked our report. **adityaanikam** and **joein** contributed the fix and integration, which was merged into upstream's `dev` branch on 13 October. Our contribution was the reproducible report and follow-up review; the upstream implementation belongs to those contributors.

[Read the case](CASES.ko.md#10) · [Original report](https://github.com/qdrant/qdrant-client/issues/1510) · [Merged external fix](https://github.com/qdrant/qdrant-client/pull/1515)

### 01 · Keep an approval attached to the request that triggered it

**Hermes Agent · Patch and tests adopted on the author's branch**

A pending model-switch approval needed to stay connected to its original request as later interactions arrived. We supplied a reproduction, a request-binding patch, and regression tests. Feature author **MestreY0d4-Uninter** reported applying the two files verbatim, checking their contents, and running the related tests. The original feature and its integration remain the author's work.

[Read the case](CASES.ko.md#01) · [Author's adoption report](https://github.com/NousResearch/hermes-agent/pull/22982#issuecomment-5643327201)

### 02 · Tell a temporary connection failure from a rejected protocol

**Hermes Agent · Real-connection tests reused verbatim, with coauthorship**

A temporary server error needs a different recovery path from a genuine rejection of the communication protocol. We supplied tests using a real local HTTP server to distinguish those conditions across code revisions. **liuhao1024** reused our test commit unchanged, retained coauthorship, and reported all 43 related checks passing. The recovery implementation itself is liuhao1024's contribution.

[Read the case](CASES.ko.md#02) · [Test reuse and rerun report](https://github.com/NousResearch/hermes-agent/pull/121944#issuecomment-5863926910)

### 04 · Check what an evaluation result actually supports

**Total Agent Memory · Named contribution in the published report**

We checked saved evaluation verdicts and the conclusions drawn from them: six LongMemEval accuracy values and four paired comparisons. Project author **vbcherepanov** added credit naming Youngseok Oh and Zero's substantial technical analysis, code, and execution assistance. The original benchmark research belongs to its author; our review covered the saved results and their reporting.

[Read the case](CASES.ko.md#04) · [Published credit](https://github.com/vbcherepanov/total-agent-memory/commit/55d0ab0124ca4fca81479a5bcafa262aaaf0e19e)

## Eight more collaborations

| Case | What we contributed | Confirmed outcome |
|---|---|---|
| [13 · Distinguish the causes behind similar failures](CASES.ko.md#13) | Replay-based analysis and clearer classification of nine parser-recovery discrepancies | The CanIToolCall owner replayed selected cases, approved the explanations, and merged the triage changes in #13. The changes are in CanIToolCall's triage and reporting files. |
| [14 · Keep numeric `42` and string `"42"` as different facts](CASES.ko.md#14) | A reproduction, type-preserving fix, and regression tests for mnemo's read-side fact resolver | The owner confirmed the bug, reported all 11 resolver tests passing, and approved #204. It remains unmerged, with DCO sign-off and CI execution pending. |
| [03 · Catch a compatibility regression before implementation](CASES.ko.md#03) | Showed why an existing nested-task exclusion must precede LangGraph's proposed command classification | The proposal author corrected the public design and acknowledged the review. |
| [05 · Prevent a late response from overriding a newer choice](CASES.ko.md#05) | Distinguished a superseded restore request from a screen whose lifetime had ended | The Hermes feature author confirmed both failures and reported fixing them; the response disclosed AI assistance. |
| [06 · Preserve normal data that quotes an interruption marker](CASES.ko.md#06) | Identified valid JSON strings and lists that could be mistaken for an interrupted command | The Hermes PR author added regression coverage. A later contributor also documented a separate remaining boundary in file content. |
| [07 · Separate personal Signal notes from group messages](CASES.ko.md#07) | Proposed a narrow opt-out while preserving group synchronization and existing defaults | A participant implemented it on a linked secondary device and reported the expected behavior. |
| [08 · Distinguish an explicit stop from a redirect](CASES.ko.md#08) | Reviewed a Hermes classification boundary and its regression cases | The author strengthened the branch and used a command-line experiment to correct our broader causal explanation. Both results are preserved. |
| [09 · Show how an unseen candidate can reverse search results](CASES.ko.md#09) | Reproduced a ranking reversal caused by an old candidate absent from the final results | Another memory-tool author explicitly cited our counterexample when comparing their existing design. The resolver implementation is theirs. |

## Who contributed what

**Youngseok Oh supplies questions, direction, and corrections. Zero is the AI collaborator performing substantial analysis, implementation, execution, and writing.** Original feature work, integration, and reported reruns remain attributed to the external contributors. Some of their work is also AI-assisted, as recorded in the detailed cases.

The linked records preserve source dates, code revisions, and the scope of each outcome. Reported test counts belong to those recorded executions. An approval or branch adoption is labeled separately from a merge, and a merge does not establish a release or deployment.

[Publication criteria](PUBLICATION.md) · [Technical workbench](https://github.com/YS-OH-CORE/second-paddle-notes) · [Ko-fi](https://ko-fi.com/ysohcore)

---

First published **6 October 2026** · **14 selected cases as of 19 October 2026 KST** · Cases 12–14 added and Qdrant's merged outcome refreshed in this edition. Earlier contributions retain their original evidence and dates.
