# Ahmed Gamal (Snow)

**Applied AI Engineer**

I build citation-grounded RAG and agent systems: cited answers or safe refusal, never a confident guess.

**Open to Applied AI Engineer roles, remote or on-site.**

[Website](https://0xsnow-1.github.io) · [LinkedIn](https://www.linkedin.com/in/ahmed-gamal-363b47307) · [GitHub](https://github.com/0xSnow-1) · [Email](mailto:0xahmed.gamal@gmail.com)

---

**Start here:** [Occlusion](https://github.com/0xSnow-1/Occlusion) for measured safety, [Sibyl](https://github.com/0xSnow-1/sibyl) as the newest build.

## Selected work

### [Occlusion](https://github.com/0xSnow-1/Occlusion) - citation-grounded dental patient FAQ

- **Problem:** Dental patients mix routine questions with dosage and diagnosis asks, and a confident guess is worse than no answer.
- **Built:** A deterministic pre-LLM guardrail, hybrid retrieval (Qdrant dense + SPLADE, server-side RRF), Pydantic `Answer` vs `Refusal` contracts, and fail-closed citation gates. Refusals never call the model.
- **Result:** Ragas faithfulness 0.9304 on the committed [78-item baseline](https://github.com/0xSnow-1/Occlusion/blob/main/src/eval/ragas/results/ragas_baseline_v1.json), Harbor safety [204/204 oracle criteria](https://github.com/0xSnow-1/Occlusion/tree/main/evals/jobs) in committed job records, 193 offline tests green in CI, live-model pass 192/202.
- **Limit:** 10 live boundary questions still over-refuse. The calibration backlog stays open in the repo instead of hidden.
- **Proof:** [live demo](https://occlusion-4kywlwripebvhgmhg6evmx.streamlit.app/) · [eval section](https://github.com/0xSnow-1/Occlusion#evaluation-measured-not-claimed) · [write-up](https://0xsnow-1.github.io/posts/Occlusion/)

### [Sibyl](https://github.com/0xSnow-1/sibyl) - autonomous Gmail support desk

- **Problem:** A seller's inbox mixes routine questions with refunds and safety cases, and a model that promises a refund or sends a cut-off email is a business risk.
- **Built:** A small classifier routes each email, a larger model drafts the reply, deterministic Python rules own refunds, exchanges, and escalations, and validators reject truncated, unsigned, or AI-mentioning replies. Every decision lands in a React admin dashboard.
- **Result:** An 18-case golden set, now checked four ways per case. The committed [run history](https://github.com/0xSnow-1/sibyl/blob/main/evals/RESULTS.md) went 97.2% to 100% on the earlier two-check suite, and that 100% run still recorded cut-off customer replies - which is why the sign-off and plain-text checks exist. CI builds the Docker image and typechecks and lints the dashboard.
- **Limit:** The latest saved run predates the escaped-newline fix, and the suite runs manually because it calls paid model APIs.
- **Proof:** [run artifacts](https://github.com/0xSnow-1/sibyl/tree/main/evals/runs) · [failure write-up](https://github.com/0xSnow-1/sibyl/blob/main/failures.md)

### [agentic-support-triage](https://github.com/0xSnow-1/agentic-support-triage) - supervisor-routed support triage

- **Problem:** Support requests need deterministic routing, and an agent with open file access is a liability.
- **Built:** A LangGraph supervisor routes to billing, technical, FAQ, and escalation specialists with typed Pydantic outputs, served through a FastAPI boundary (`GET /health`, `POST /triage`), with reads limited to approved docs and writes clamped to `tickets/`.
- **Result:** A deterministic grader baseline of 18/20 (90%) recorded in the [repo eval section](https://github.com/0xSnow-1/agentic-support-triage#eval-baseline). The same suite grades routes, forbidden claims, escalation behavior, hop limits, and answer quality with an LLM judge.
- **Limit:** The recorded run predates the LLM-judge grader, so it is a deterministic baseline, not a final quality score, and the repo has no CI yet.
- **Proof:** [eval section](https://github.com/0xSnow-1/agentic-support-triage#eval-baseline) · [FastAPI service](https://github.com/0xSnow-1/agentic-support-triage/blob/main/api/main.py)

## More work

[NutriMind](https://github.com/0xSnow-1/NutriMind) · [doc-pipe](https://github.com/0xSnow-1/doc-pipe) · [Shippy](https://github.com/0xSnow-1/Shippy) · [shipment-exception-triage-agent](https://github.com/0xSnow-1/shipment-exception-triage-agent)

## Stack

Python, LangGraph and LangChain, Qdrant hybrid retrieval, Pydantic v2, FastAPI, Docker, Streamlit and React; Ragas, Harbor, LLM-as-judge, LangSmith; Claude on AWS Bedrock with Cerebras and NVIDIA endpoints.

## How I build

1. **Evals before claims.** Every project ships a versioned golden set and recorded runs, with misses published next to wins. Occlusion keeps its over-refusal backlog in the repo; Sibyl keeps its failure log.
2. **Deterministic boundaries around models.** Guardrails run before the LLM, outputs are typed contracts, validators fail closed, and tools are sandboxed. Python decides; models propose.
3. **Safety habits from smart-contract auditing.** 2025-2026 competitive audits for reentrancy and access-control bugs trained the habit of finding the specific way a system breaks, which is how trap sets and near-miss evals are built.

---

The longest write-up is the [Occlusion post](https://0xsnow-1.github.io/posts/Occlusion/).

Contact: [0xahmed.gamal@gmail.com](mailto:0xahmed.gamal@gmail.com) · [LinkedIn](https://www.linkedin.com/in/ahmed-gamal-363b47307) · [Website](https://0xsnow-1.github.io)
