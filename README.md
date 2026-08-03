# Дмитрий Пром · AI Engineer / LLM Engineer

I build production LLM systems that take manual work off revenue teams — and I do the
analysis on top of the data they produce. Business rules, prompts, retrieval, model
orchestration, Python/TypeScript services, evaluation, CRM/BI delivery, unit economics —
and then the report a decision is actually made on.

[Portfolio](https://94spec.github.io/) · [Lead Chat](https://leadchat.online/) · [Email](mailto:xpromx94@yandex.ru)

Five years in engineering, two in AI. Open to Senior / Lead Applied AI roles with end-to-end ownership. Remote, UTC+3, open to teams abroad.

## Production impact

| System | Scale | Business result |
|---|---|---|
| **AI quality control across customer communications** (major RU edtech platform) | 90 production pipelines; 55 checklists; 32 summary configurations; 464 checklist criteria and 246 summary fields/detectors | A previously manual QA workflow fully automated: **100%** of eligible conversations evaluated, against **≤20%** under manual sampling |
| **Voice AI** | **45–50%** of eligible routine consultations handled without an operator | **≥ 1M ₽ / month** saved on contact-centre cost; **×1.2** qualified leads in month one |
| **Enterprise RAG** | 100+ daily internal users | Answers with a source link in **under 10 seconds** instead of ≈5 minutes of manual search |
| **Model economics** | Same output contract moved from an expensive model to a compact one | **−88%** cost of the key LLM scenario per 1,000 deals, with schema, benchmark and quality gates unchanged |
| **Lead Chat — independent AI SaaS** | Multi-tenant RAG, tool calling, web + Telegram, CRM, booking, billing, analytics | Pay-per-result pricing: **50 ₽ per created lead**, not per message |

Denominators for every number above: [94spec.github.io/#measure](https://94spec.github.io/#measure).

Quality is controlled with four task-specific golden sets, human calibration, schema
validation, a typed error taxonomy, confidence intervals and regression gates. A frozen,
manually adjudicated **500-deal golden set** recorded **98% model-vs-expert decision
agreement**; critical-violation recall is gated separately, because an average score hides
exactly the misses that matter.

For Lead Chat I own the product concept, AI logic and core architecture. A development
partner works with me on the technical side: selected components and code testing.

## Analytics that drives decisions

The pipeline gives me structured data for every conversation. The second half of the job is
turning that into answers the business acts on — studies of up to 3,000 deals, horizons up to
six months, covering every employee who talks to customers:

- **Why conversion dropped over a quarter** — every substantive conversation for a product
  line across three months (empty calls excluded from the base explicitly, before any
  percentages), dozens of features per deal, month over month. Observations kept separate
  from hypotheses.
- **"Too expensive" is not always about price** — a two-level reason taxonomy, with records
  that failed processing excluded explicitly, the loss stated plainly in the report. The top
  level says "cost"; the second level says the customer cannot get instalment financing.
  Different problem, different decision.
- **Part of the sales team's load is not sales** — inbound requests classified by type and by
  owner (sales, refunds, support), surfacing deals closed under the wrong reason and a
  conversion denominator that was measuring the wrong thing.

Rules I keep: sample control before any percentage, a denominator for every share, hypotheses
labelled as hypotheses, every category backed by a customer quote, and an explicit limitations
section stating what the data cannot show.

## What I own

`Business process → AI behaviour spec → architecture → implementation → evaluation → production integration → cost/quality optimisation → the report behind the decision`

- Conversation intelligence and rubric-based AI quality control
- LLM evaluation: golden sets, LLM-as-a-Judge, error taxonomies, regression gates
- RAG: chunking, hybrid retrieval, grounding, source-aware answers
- AI agents: structured outputs, tool calling, memory, guardrails
- Voice AI and dialogue-state design
- Sales, marketing, product and pricing analytics on conversation data
- CRM/BI/API integration and multi-provider cost optimisation

## Engineering repositories

- [llm-evaluation-harness](https://github.com/94spec/llm-evaluation-harness) — dependency-free
  evaluation framework for four task families, with
  [methodology](https://github.com/94spec/llm-evaluation-harness/blob/main/METHODOLOGY.md),
  [error taxonomy](https://github.com/94spec/llm-evaluation-harness/blob/main/ERROR_TAXONOMY.md)
  and a [sample report](https://github.com/94spec/llm-evaluation-harness/blob/main/reports/DEMO_REPORT.md).
- [prompt-contracts](https://github.com/94spec/prompt-contracts) — prompts as versioned
  contracts: strict output schema, a linter where every rule names the production failure it
  prevents, and a release-impact diff that says whether a change forces the golden set to be
  re-run.
- [golden-set-builder](https://github.com/94spec/golden-set-builder) — building the reference
  set itself: stratified sampling that reports what the pool could not give, annotator
  agreement before any model metric, adjudication that refuses majority vote, tamper-evident
  freezing and drift detection.
- [voice-agent-runtime](https://github.com/94spec/voice-agent-runtime) — the parts of a voice
  agent that are not the model: dialogue policy as a transition table, barge-in that never
  resumes, a per-stage latency budget judged at p95, line capacity, and guardrails that decide
  whether a reply can be spoken at all.
- [rag-grounding-lab](https://github.com/94spec/rag-grounding-lab) — what chunking costs and
  where each retrieval strategy loses: BM25 against Russian morphology, character n-grams
  against near-identical codes, rank fusion carrying a wrong result. Plus sentence-level
  grounding that separates an unsupported claim from a correct refusal.
- [conversation-intelligence-lab](https://github.com/94spec/conversation-intelligence-lab) —
  the analytics methodology above on synthetic data: strict output contract, traceable
  aggregates, [architecture notes](https://github.com/94spec/conversation-intelligence-lab/blob/main/docs/architecture.md).
- [94spec.github.io](https://github.com/94spec/94spec.github.io) — the portfolio itself:
  static, no build step, with CI that checks metadata, anchors and assets.

All six code repositories above run offline, with no API key and no third-party runtime dependencies.

## Stack

**In production, under my responsibility:**
`Python` `TypeScript` `FastAPI` `Node.js` `PostgreSQL` `pgvector` `SQL` `Docker` `OpenAI API`
`Anthropic API` `GigaChat` `YandexGPT` `Dify` `RAG` `AI Agents` `Structured Outputs`
`Tool Calling` `LLM-as-a-Judge` `Voice AI` `CRM / BI` `Git`

**Worked with outside that loop:**
`LangChain` `LangGraph` `Qdrant` `vLLM` `Hugging Face` `Fine-tuning / LoRA` `RAGAS`
`A/B Testing` `Guardrails` `Prompt Injection` `NLP`

---

**RU:** Строю production LLM-системы для коммерческих процессов и делаю на их данных
аналитику, по которой принимают решения — по продажам, маркетингу, продукту и тарифам.
Открыт к Senior / Lead Applied AI ролям, удалённо, UTC+3.
