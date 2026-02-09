# AI Engineer Roadmap (2025)

A structured, market-aligned study plan to become an AI Engineer — focused on what companies actually hire for today: LLM integration, RAG, evaluation, production systems, and cost optimization.

**Profile:** Intermediate Python, moderate math, familiar with AI tools
**Commitment:** 10-20 hours/week
**Structure:** 5 phases over ~6-7 months
**Philosophy:** LLM-first, production-focused, build real projects

---

## What This Plan Is Based On

This roadmap reflects the 2025 reality of AI engineering hiring:

| What Companies Want | What's Now Secondary |
|---------------------|---------------------|
| Ship LLMs to production | Training models from scratch |
| RAG pipelines that work | Custom deep learning architectures |
| LLM evaluation skills | Heavy classical ML focus |
| Cost & latency optimization | Research-only profiles |
| Strong backend engineering | Kaggle as primary signal |
| Product judgment | Feature engineering depth |

> **The question is no longer "Which model should I train?"**
> **It's "How do I integrate LLMs safely, efficiently, and at scale?"**

---

## Priority Stack

```
Tier 1 — Get hired (must-have):
  ├── RAG (embeddings, chunking, retrieval, vector DBs)
  ├── LLM APIs (Anthropic, OpenAI — tool use, structured outputs)
  ├── Backend skills (Python, APIs, async, error handling)
  ├── Prompt engineering (versioning, testing, guardrails)
  └── Basic evaluation (how do you know it works?)

Tier 2 — Stand out (differentiators):
  ├── Advanced evaluation (golden datasets, A/B testing)
  ├── Cost optimization (caching, batching, model selection)
  ├── Agentic systems (planning, tool use, memory)
  ├── LLM security (prompt injection, PII, output filtering)
  └── Production ops (monitoring, rollback, CI/CD for AI)

Tier 3 — Level up (senior/lead):
  ├── Product judgment (when NOT to use LLMs)
  ├── Fine-tuning (LoRA, when and why)
  ├── Multi-modal (vision, audio)
  ├── System design for AI (architecture decisions at scale)
  └── Deep transformer understanding (for debugging, optimization)
```

---

## Ongoing Side-Track: Math (As Needed)

**Runs parallel — 2 hours/week, never blocks progress**

| When | What | Resource |
|------|------|----------|
| Phase 1 | Linear algebra basics (vectors, matrices, dot products) | [3Blue1Brown Essence of Linear Algebra](https://www.youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab) |
| Phase 2 | Calculus intuition (gradients, chain rule) | [3Blue1Brown Essence of Calculus](https://www.youtube.com/playlist?list=PLZHQObOWTQDMsr9K-rj53DwVRMYO3t5Yr) |
| Phase 3+ | Probability, statistics (as needed for evaluation) | [StatQuest YouTube](https://www.youtube.com/@statquest) |

> **Rule:** Learn math when you hit a concept that requires it, not upfront. Embeddings → learn dot products. Backpropagation → learn chain rule. Just-in-time, not just-in-case.

---

## Phase 1: Compressed ML Foundations (Weeks 1-4)

**Goal:** Understand enough ML to evaluate models, understand embeddings, and know why things work — not to become an ML researcher.

| Week | Study (40%) | Build (60%) |
|------|------------|-------------|
| 1 | [Andrew Ng's ML Specialization](https://www.coursera.org/specializations/machine-learning-introduction) — Course 1 only: Supervised Learning (regression, classification, evaluation) | [Kaggle Intro to ML](https://www.kaggle.com/learn/intro-to-machine-learning) micro-course |
| 2 | Focus on: evaluation metrics, train/test splits, overfitting, cross-validation | Build a simple classifier with scikit-learn on a real dataset |
| 3 | Embeddings deep-dive: what they are, how they represent meaning, similarity metrics | Visualize embeddings using a pre-trained model (sentence-transformers) |
| 4 | Review + consolidate | **Project 1:** Simple ML pipeline — data → features → model → evaluation. Focus on metrics and understanding *why* the model works or fails. GitHub repo |

**Key concepts to nail:**
- [ ] Train/validation/test splits — why they matter
- [ ] Evaluation metrics: accuracy, precision, recall, F1, AUC-ROC
- [ ] Overfitting and how to detect it
- [ ] What embeddings are and how similarity works
- [ ] When ML is the right tool (vs. rules, vs. LLMs)

**Reading:**
- [Jay Alammar's visual ML guides](https://jalammar.github.io/)
- [What Are Word Embeddings?](https://jalammar.github.io/illustrated-word2vec/) — Jay Alammar

---

## Phase 2: Transformers Deep-Dive (Weeks 5-7)

**Goal:** Understand how LLMs actually work — attention, tokenization, context windows — so you can debug and optimize, not just call APIs.

| Week | Study (50%) | Build (50%) |
|------|------------|-------------|
| 5 | [Hugging Face NLP Course](https://huggingface.co/learn/nlp-course) — Chapters 1-2 (Transformers, pipeline API) + ["Attention Is All You Need"](https://arxiv.org/abs/1706.03762) with [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/) | Run Hugging Face pipelines, experiment with different models |
| 6 | Hugging Face NLP Course — Chapters 3-4 (Tokenizers, fine-tuning basics) | Tokenize text with different tokenizers, understand token counts, context limits |
| 7 | How LLMs are trained: pre-training, instruction tuning, RLHF. Inference vs training. | **Project 2:** Fine-tune a small model (DistilBERT or similar) on a classification task. Understand the training loop. GitHub repo |

**Key concepts to nail:**
- [ ] Self-attention mechanism (intuition, not math derivation)
- [ ] Multi-head attention and why it matters
- [ ] Tokenization: BPE, token counts, context windows
- [ ] Positional encoding
- [ ] Pre-training vs fine-tuning vs RLHF
- [ ] Inference: temperature, top-p, sampling strategies

**Reading:**
- ["Attention Is All You Need"](https://arxiv.org/abs/1706.03762) — the original transformer paper
- [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/) — Jay Alammar
- [The Illustrated GPT-2](https://jalammar.github.io/illustrated-gpt2/) — Jay Alammar
- [What Is ChatGPT Doing?](https://writings.stephenwolfram.com/2023/02/what-is-chatgpt-doing-and-why-does-it-work/) — Stephen Wolfram

---

## Phase 3: Applied LLM Engineering (Weeks 8-17)

**Goal:** This is the core of modern AI engineering. RAG, agents, evaluation, prompt engineering, structured outputs, MCP.

### 3A: LLM APIs & Prompt Engineering (Weeks 8-10)

| Week | Study (40%) | Build (60%) |
|------|------------|-------------|
| 8 | [Anthropic Prompt Engineering Guide](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview) + [Anthropic Courses](https://github.com/anthropics/courses) | Set up [Anthropic API](https://docs.anthropic.com/en/api/getting-started) and [OpenAI API](https://platform.openai.com/docs). Build chat applications with both |
| 9 | Prompt patterns: system prompts, few-shot, chain-of-thought, structured outputs | Build a prompt versioning system. Test prompts systematically |
| 10 | Tool use / function calling with Claude and OpenAI | **Project 3:** LLM app with structured outputs and tool use — e.g., an assistant that can search, calculate, and return JSON. GitHub repo |

**Key concepts to nail:**
- [ ] System / user / assistant message roles
- [ ] Few-shot prompting
- [ ] Chain-of-thought reasoning
- [ ] Structured outputs (JSON mode, tool use)
- [ ] Prompt versioning and regression testing
- [ ] Guardrails and output validation

### 3B: RAG — The Non-Negotiable Skill (Weeks 11-14)

| Week | Study (40%) | Build (60%) |
|------|------------|-------------|
| 11 | DeepLearning.AI: [LangChain for LLM Application Dev](https://www.deeplearning.ai/short-courses/langchain-for-llm-application-development/) | Build RAG from scratch (no frameworks): embed documents → store in vector DB → retrieve → generate |
| 12 | Chunking strategies, embedding models comparison, retrieval metrics | Experiment with different chunk sizes, overlap, embedding models |
| 13 | Vector databases deep-dive: [Chroma](https://docs.trychroma.com/), [Pinecone](https://www.pinecone.io/), [Weaviate](https://weaviate.io/). Re-ranking, hybrid search | Implement re-ranking, compare retrieval quality |
| 14 | DeepLearning.AI: [LangChain Chat with Your Data](https://www.deeplearning.ai/short-courses/langchain-chat-with-your-data/) | **Project 4:** Production-quality RAG system — PDF ingestion, chunking, retrieval, answer generation with citations. Measure retrieval quality. GitHub repo |

**Key concepts to nail:**
- [ ] Embeddings: models, dimensions, similarity metrics
- [ ] Chunking: size, overlap, semantic vs fixed
- [ ] Vector databases: indexing, querying, filtering
- [ ] Retrieval quality: precision, recall, MRR
- [ ] Re-ranking and hybrid search
- [ ] Caching strategies for embeddings

### 3C: Evaluation — Where Seniors Stand Out (Weeks 15-16)

| Week | Study (40%) | Build (60%) |
|------|------------|-------------|
| 15 | LLM evaluation approaches: [RAGAS](https://docs.ragas.io/), [DeepEval](https://docs.confident-ai.com/). Human-in-the-loop workflows | Build an evaluation pipeline for your RAG project |
| 16 | Golden datasets, A/B testing prompts, offline vs online evaluation | **Add to Project 4:** Comprehensive evaluation suite — automated metrics + golden dataset + regression tests |

**Key concepts to nail:**
- [ ] Evaluation without ground truth
- [ ] RAG metrics: faithfulness, relevance, context precision
- [ ] Golden datasets and how to build them
- [ ] A/B testing prompts and models
- [ ] Human evaluation workflows
- [ ] Regression testing for prompts

### 3D: Agents & Tool Use (Weeks 17)

| Week | Study (40%) | Build (60%) |
|------|------------|-------------|
| 17 | DeepLearning.AI: [Building Agentic RAG](https://www.deeplearning.ai/short-courses/). ReAct pattern, planning, memory. [MCP (Model Context Protocol)](https://modelcontextprotocol.io/) | **Project 5:** AI agent — multi-step reasoning, multiple tools, memory, error handling. GitHub repo |

**Key concepts to nail:**
- [ ] ReAct pattern (Reasoning + Acting)
- [ ] Tool use and function calling
- [ ] Agent memory (short-term and long-term)
- [ ] Planning and task decomposition
- [ ] MCP for connecting LLMs to external systems
- [ ] When agents are overkill vs necessary

**Reading for Phase 3:**
- [Anthropic Cookbook](https://github.com/anthropics/anthropic-cookbook) — real code patterns
- [LLM Powered Autonomous Agents](https://lilianweng.github.io/posts/2023-06-23-agent/) — Lilian Weng
- [RAG paper](https://arxiv.org/abs/2005.11401) — "Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks"
- [Anthropic Research Blog](https://www.anthropic.com/research)

---

## Phase 4: Production AI Systems (Weeks 18-23)

**Goal:** Ship reliable, cost-effective, secure AI applications. This is what separates demos from products.

### 4A: Backend Engineering for AI (Weeks 18-19)

| Week | Study (40%) | Build (60%) |
|------|------------|-------------|
| 18 | [FastAPI tutorial](https://fastapi.tiangolo.com/tutorial/) — async, dependencies, error handling | Build an API wrapper around your RAG project |
| 19 | [Docker fundamentals](https://docs.docker.com/get-started/). Async patterns, streaming responses | Containerize your application. Implement streaming for LLM responses |

**Key concepts to nail:**
- [ ] Async Python (asyncio, aiohttp)
- [ ] Error handling and timeouts for LLM calls
- [ ] Streaming responses
- [ ] Docker containerization
- [ ] API design (REST, request validation)

### 4B: Cost & Performance (Weeks 20-21)

| Week | Study (40%) | Build (60%) |
|------|------------|-------------|
| 20 | Token cost management, context window optimization, caching strategies | Implement caching (Redis or similar) for embeddings and LLM responses |
| 21 | Model selection tradeoffs (Claude Haiku vs Sonnet vs Opus, GPT-4 vs GPT-4-mini), batch vs real-time | Add cost tracking and optimization to your project. Implement model routing |

**Key concepts to nail:**
- [ ] Token counting and cost calculation
- [ ] Aggressive caching strategies
- [ ] Context window optimization
- [ ] Model routing (cheap model first, expensive if needed)
- [ ] Batch vs real-time tradeoffs
- [ ] Latency optimization

### 4C: LLM Security (Week 22)

| Week | Study (40%) | Build (60%) |
|------|------------|-------------|
| 22 | Prompt injection attacks, data leakage, PII handling, output filtering | Add security layers to your project: input validation, output filtering, PII detection |

**Key concepts to nail:**
- [ ] Prompt injection (direct and indirect)
- [ ] Data leakage prevention
- [ ] PII detection and handling
- [ ] Output filtering and validation
- [ ] Tool misuse prevention

### 4D: Deployment & Observability (Week 23)

| Week | Study (40%) | Build (60%) |
|------|------------|-------------|
| 23 | Cloud deployment (AWS Lambda, GCP Cloud Run, or similar). LLM observability ([LangSmith](https://smith.langchain.com/), [Helicone](https://helicone.ai/)). CI/CD for AI | **Project 6:** Deploy your full stack — API + RAG + caching + monitoring + CI/CD. GitHub repo with deployment instructions |

**Key concepts to nail:**
- [ ] Cloud deployment options
- [ ] CI/CD pipelines for AI applications
- [ ] Monitoring: latency, cost, error rates
- [ ] Logging and tracing LLM calls
- [ ] Rollback strategies
- [ ] Model and prompt versioning in production

---

## Phase 5: Specialization & Depth (Weeks 24-28+)

**Goal:** Go deep in one area. Build authority. Contribute to the ecosystem.

| Week | Focus |
|------|-------|
| 24-25 | **Choose your specialization:** Conversational AI, RAG Systems, AI Agents, LLM Security, AI Infrastructure. Read 4-5 key papers/posts in that area |
| 26-27 | **Advanced project** — something novel, not a tutorial clone. Multi-agent system, domain-specific RAG, fine-tuned model, security toolkit |
| 28+ | **Contribute to open source** ([LangChain](https://github.com/langchain-ai/langchain), [Anthropic Cookbook](https://github.com/anthropics/anthropic-cookbook), [Hugging Face](https://github.com/huggingface)). Write about what you learned |

**Specialization options:**

| Track | Focus Areas |
|-------|-------------|
| Conversational AI | Multi-turn memory, personality, safety, dialogue management |
| RAG Systems | Advanced retrieval, re-ranking, evaluation, domain adaptation |
| AI Agents | Planning, tool use, multi-agent coordination, reliability |
| LLM Security | Red teaming, prompt injection defense, guardrails, compliance |
| AI Infrastructure | Scaling, cost optimization, observability, platform building |
| Fine-tuning | LoRA/QLoRA, dataset curation, evaluation, deployment |

---

## Weekly Routine (~15 hours/week)

```
Mon-Tue:     Course material — videos + reading (4 hrs)
Wed:         Hands-on exercises, API experimentation (2 hrs)
Thu-Fri:     Project work (6 hrs)
Sat:         Math (as needed) + 1 paper/blog (2 hrs)
Sun:         Rest or light review
```

---

## GitHub Portfolio at the End

| # | Project | What It Demonstrates |
|---|---------|---------------------|
| 1 | ML pipeline with evaluation | Understand metrics, train/test, model selection |
| 2 | Fine-tuned transformer | How LLMs work, training loop, Hugging Face |
| 3 | LLM app with tools + structured output | API integration, prompt engineering, tool use |
| 4 | RAG system with evaluation suite | Embeddings, retrieval, chunking, quality measurement |
| 5 | AI agent with memory | Multi-step reasoning, planning, error handling |
| 6 | Production-deployed full stack | Docker, API, caching, monitoring, CI/CD, cloud |

---

## Key Milestones

| Week | You should be able to... |
|------|--------------------------|
| 4 | Understand ML evaluation, embeddings, when to use what |
| 7 | Explain how transformers work, fine-tune a model |
| 14 | Build production-quality RAG systems, measure retrieval quality |
| 17 | Build agents with tools and memory |
| 23 | Deploy, monitor, and optimize LLM applications in production |
| 28 | Have a specialization and contribute to open source |

---

## Core Skills Checklist

### Tier 1: Get Hired
- [ ] RAG: embeddings, chunking, retrieval, vector databases
- [ ] LLM APIs: Anthropic, OpenAI — structured outputs, tool use
- [ ] Prompt engineering: versioning, testing, guardrails
- [ ] Backend: Python, async, APIs, error handling
- [ ] Basic evaluation: know if your system works

### Tier 2: Stand Out
- [ ] Advanced evaluation: golden datasets, A/B testing, RAGAS
- [ ] Cost optimization: caching, batching, model routing
- [ ] Agents: planning, tool use, memory, MCP
- [ ] LLM security: prompt injection, PII, output filtering
- [ ] Production: monitoring, CI/CD, rollback

### Tier 3: Senior/Lead
- [ ] Product judgment: when NOT to use LLMs
- [ ] Fine-tuning: LoRA, dataset curation
- [ ] Multi-modal: vision, audio integration
- [ ] System design: architecture at scale
- [ ] Deep transformer knowledge: debugging, optimization

---

## Resources Index

### Core Documentation
- [Anthropic API Docs](https://docs.anthropic.com/en/api/getting-started)
- [Anthropic Prompt Engineering Guide](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview)
- [Anthropic Courses](https://github.com/anthropics/courses)
- [Anthropic Cookbook](https://github.com/anthropics/anthropic-cookbook)
- [Model Context Protocol (MCP)](https://modelcontextprotocol.io/)
- [OpenAI API Docs](https://platform.openai.com/docs)
- [LangChain Documentation](https://python.langchain.com/docs/get_started/introduction)

### Courses
- [Andrew Ng's ML Specialization](https://www.coursera.org/specializations/machine-learning-introduction) — Course 1 only for foundations
- [Hugging Face NLP Course](https://huggingface.co/learn/nlp-course) — free, essential
- [DeepLearning.AI Short Courses](https://www.deeplearning.ai/short-courses/) — LangChain, RAG, Agents
- [Generative AI with LLMs](https://www.coursera.org/learn/generative-ai-with-llms) — AWS + DeepLearning.AI

### Evaluation Tools
- [RAGAS](https://docs.ragas.io/) — RAG evaluation
- [DeepEval](https://docs.confident-ai.com/) — LLM testing framework
- [Braintrust](https://www.braintrust.dev/) — LLM evaluation platform

### Observability
- [LangSmith](https://smith.langchain.com/) — LangChain's observability
- [Helicone](https://helicone.ai/) — LLM observability
- [Portkey](https://portkey.ai/) — LLM gateway

### Blogs & Visual Guides
- [Jay Alammar](https://jalammar.github.io/) — essential visual explanations
- [Lilian Weng](https://lilianweng.github.io/) — in-depth AI research
- [Simon Willison](https://simonwillison.net/) — LLM ecosystem tracking
- [Latent Space](https://www.latent.space/) — AI engineering podcast/blog

### Key Papers
- ["Attention Is All You Need"](https://arxiv.org/abs/1706.03762) — Transformers
- ["Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks"](https://arxiv.org/abs/2005.11401) — RAG

---

## What's Different About This Plan

Compared to traditional ML/AI curricula:

| Traditional (2020-2023) | This Plan (2025) |
|------------------------|------------------|
| 8+ weeks on classical ML | 4 weeks compressed |
| 12 weeks on deep learning | 3 weeks on transformers only |
| LLMs as final topic | LLMs as the core focus |
| Training models | Using models well |
| Kaggle competitions | Production projects |
| 10-12 months | 6-7 months |
| First LLM project at week 21 | First LLM project at week 8 |

---

> **Note:** The industry moves fast. This plan reflects 2025 hiring reality. Review and adjust every 6 months. The fundamentals (how transformers work, evaluation thinking, production skills) will remain valuable. The specific tools may change.
