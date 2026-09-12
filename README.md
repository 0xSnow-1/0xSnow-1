<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&pause=1000&color=8ED1FC&center=true&vCenter=true&width=650&lines=Building+grounded+RAG+%26+agent+systems;Eval-driven.+Source-grounded.+No+hallucinated+claims.;Ex+smart-contract+security+researcher)](https://git.io/typing-svg)

![Animated ASCII terminal boot sequence](./assets/snow-boot.svg)

❄ ⋅ ❅ ⋅ ⋅ ❆ ⋅ ❄ ⋅ ❅ ⋅ ⋅ ❆ ⋅ ❄ ⋅ ❅ ⋅ ⋅ ❆ ⋅ ❄

</div>

> **30-second scan:** I'm Ahmed Gamal (Snow) — an AI engineer building
> **grounded RAG and agent systems** where every claim is verified against
> retrieved sources, not promised by a system prompt.
> Proof first: [`evals/` in Grounded Clinical Agent](https://github.com/0xSnow-1/Grounded-Clinical-Agent)
> — 40-case benchmark, versioned ledger, failure-mode report, plus an
> 8-category adversarial safety suite. Open to AI Engineer roles, remote or on-site.

<details>
<summary><b>Static ASCII fallback (neofetch)</b> — same intro, no animation</summary>

```
               \   |   /
            *   \  |  /   *
              .  \ | /  .
           ----.--❄--.----
              .  / | \  .
            *   /  |  \   *
               /   |   \

            .  * SNOW *  .
```

```
ahmed@snow ~ % whoami
-----------------------------------
Name       : Ahmed Gamal
Role       : AI Engineer
Focus      : Agentic RAG · Evaluation · Guardrails
Stack      : LangGraph · Qdrant · Docling · Python
Languages  : English, Arabic (native)
Prior life : Smart-contract security researcher
Contact    : 0xahmed.gamal@gmail.com
```

</details>

---

### ❄ Currently building

**[Grounded Clinical Agent](https://github.com/0xSnow-1/Grounded-Clinical-Agent)**
— a self-correcting RAG agent answering dental clinical questions strictly
from CDC, WHO, and USPSTF guidelines. Unverifiable claims trigger a
feedback loop back to the generator (up to 3 retries), then escalate to
human review.

`92.5% Hit@3` · `0.872 MRR` · `95.0% faithfulness` · `85.4% answer relevance` · `80.0% safety defense`
— 40-case benchmark, baseline B0. Dual-LLM setup (Haiku 4.5 generates,
Sonnet 4.6 judges) avoids self-preference bias; MedEmbed-small-v0.1 +
Qdrant retrieval with Docling parsing; Postgres-checkpointed LangGraph flow;
FastAPI + AG-UI serving with a React/TypeScript client.

Currently going deeper: BM25 hybrid retrieval + Reciprocal Rank Fusion (RRF),
and better eval harnesses across health and law domains.

---

### ❆ Selected work — start here

| Project | Problem → mechanism | Proof |
|---|---|---|
| [**Grounded Clinical Agent**](https://github.com/0xSnow-1/Grounded-Clinical-Agent) | Clinical answers must not hallucinate → cyclic LangGraph workflow routes, retrieves, checks claim-groundedness, retries, then escalates | 40-case eval ledger: 92.5% Hit@3, 95.0% faithfulness; per-question failure analysis in `evals/` |
| [**NutriMind**](https://github.com/0xSnow-1/NutriMind) | Meal plans drift off-goal and miss safety flags → 6-agent supervisor graph with LLM-as-judge gate and caloric-safety interrupt | Plans scoring below 7/10 auto-regenerate; 3+ days under 1200 kcal pauses for human review; LangSmith-traced |
| [**agentic-support-triage**](https://github.com/0xSnow-1/agentic-support-triage) | Support requests need deterministic routing → supervisor-routed agents with typed outputs and secured tools | Deterministic evals + LangSmith tracing |
| [**shipment-exception-triage-agent**](https://github.com/0xSnow-1/shipment-exception-triage-agent) | Entry for Single Grain Career's "Beat Claude" agentic challenge | Python |

---

### ❅ Stack

| Area | Core — shipped with | Also used |
|---|---|---|
| Orchestration | LangGraph, LangChain | — |
| Retrieval | Qdrant, FAISS | — |
| Parsing | Docling | — |
| Serving | FastAPI, AG-UI | Streamlit, Docker |
| Data | PostgreSQL | SQLite, Supabase |
| Models | Claude (AWS Bedrock) | OpenAI, Groq, Gemini, local models |
| Eval & observability | LLM-as-judge, Hit@3 / MRR / faithfulness, LangSmith | — |
| Security | Slither, Foundry (smart-contract auditing) | — |

---

### ❄ How I work

1. **Eval before claims.** Every system ships with a benchmark and a ledger —
   scores are versioned, failures are documented, targets are explicit.
2. **Verification loops, not vibes.** Grounding is enforced by graph
   structure (checker nodes, retry limits, escalation), not by prompting.
3. **Security mindset, transferred.** 2025–2026 auditing Solidity contracts
   for reentrancy and access-control bugs in competitive audits —
   "find the specific way this breaks" maps directly to LLM eval design.
4. **Built to be understood.** A year in retail sales taught me to translate
   technical complexity into terms a non-technical person can act on.

---

<div align="center">

## 🌐 Socials

[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ahmed-gamal-363b47307) [![X](https://img.shields.io/badge/X-black.svg?logo=X&logoColor=white)](https://x.com/0xSnowEth) [![Instagram](https://img.shields.io/badge/Instagram-%23E4405F.svg?logo=Instagram&logoColor=white)](https://instagram.com/hamido_1x) [![email](https://img.shields.io/badge/Email-D14836?logo=gmail&logoColor=white)](mailto:0xahmed.gamal@gmail.com)

📫 Best next step: open the [Grounded Clinical Agent evals](https://github.com/0xSnow-1/Grounded-Clinical-Agent)
— or reach me at `0xahmed.gamal@gmail.com`.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/0xSnow-1/0xSnow-1/output/github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/0xSnow-1/0xSnow-1/output/github-snake.svg" />
  <img alt="contribution snake" src="https://raw.githubusercontent.com/0xSnow-1/0xSnow-1/output/github-snake.svg" />
</picture>

</div>
