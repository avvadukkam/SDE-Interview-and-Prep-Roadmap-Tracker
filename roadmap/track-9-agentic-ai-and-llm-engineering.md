# Optional Specialization: Agentic AI, LLM Engineering & AI System Design

**Difficulty:** Advanced | **Estimated Duration:** 3–4 Weeks (Optional) | **Topics:** 2

> **Overview:** Preserves 100% of the original repository's Section 1 ('Agentic AI, LLM Engineering, and AI System Design') plus the LLM Security (Section 11) and LLM Evaluation (Section 14) checklists, repositioned from Section 1 to an advanced post-core specialization track so beginners are never overwhelmed early.

## Why This Phase Is Ordered Here
Building production RAG pipelines and multi-agent architectures requires solid foundations in APIs, databases/vector indexes, distributed caching, queues, security, and observability from Phases 1–7.

## Topics in This Phase

### 9.1 LLM Fundamentals, Prompt Engineering & RAG Architectures
- **Tier:** `Optional / Advanced (P2)` | **Difficulty:** `Advanced` | **Est. Study Time:** `14 hrs`
- **What It Covers:** Covers Transformer/token fundamentals, model selection, structured JSON schema outputs, function/tool calling, embeddings, vector indexes (HNSW, IVF), chunking, hybrid BM25 + dense retrieval, reranking, and RAG evaluation.
- **Why It Is Important:** Essential for AI Engineer, Applied LLM, and modern backend SDE roles building AI-powered features.
- **Completion Criteria:** Can architect, evaluate, and optimize an ACL-aware production RAG pipeline.

- [ ] LLM Fundamentals: Transformers, attention, tokens/context windows, temperature/top-p, closed vs. open-weight, Prompting vs. RAG vs. Fine-tuning — `P0`
- [ ] Prompt Engineering & Structured Outputs: system/user/tool priority, JSON Schema validation, function/tool calling, handling refusals & long context — `P1`
- [ ] RAG Pipelines: chunking (fixed/semantic/hierarchical), embeddings, Vector DBs (HNSW, IVF), hybrid search (BM25 + dense), reranking, multi-tenant ACL filtering — `P0`
- [ ] RAG Evaluation: recall@k, precision@k, MRR, nDCG, faithfulness, groundedness, and citations — `P0`

### 9.2 Agentic Workflows, Multi-Agent Systems, Safety & AI System Design
- **Tier:** `Optional / Advanced (P2)` | **Difficulty:** `Advanced` | **Est. Study Time:** `16 hrs`
- **What It Covers:** Covers core agent loops (ReAct), workflows vs. autonomous agents, LangGraph/checkpointing, MCP & tool contracts, memory management, multi-agent coordination, LLM-as-judge evaluation, prompt injection defense, and agentic system design case studies.
- **Why It Is Important:** Prepares engineers for cutting-edge Agentic AI system design interviews, covering reliability, cost/latency budgets, and safety guardrails.
- **Completion Criteria:** Can whiteboard an end-to-end agentic architecture with token/latency math, evaluation rubrics, and security boundaries.

- [ ] Agent Fundamentals: observe-decide-act loop, ReAct, deterministic workflows vs. autonomous agents, human-in-the-loop approvals, turn budgets — `P0`
- [ ] Orchestration & State: LangGraph state graphs, checkpointing, durable execution, short-term vs. episodic/semantic memory, context compaction — `P1`
- [ ] Tool Use & Multi-Agent Systems: MCP protocol, idempotent tools, parallel tool execution, supervisor/worker vs. single-agent trade-offs — `P1`
- [ ] Evaluation, Reliability & Security: trajectory tests, LLM-as-judge calibration, prompt/response caching, token cost/p95 latency budgets, prompt injection & sandboxing — `P0`
- [ ] Agentic System Design Practice: code-review agent, customer-support agent with handoff, document research agent, incident-response assistant — `P0`
