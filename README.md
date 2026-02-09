# AI Engineer Roadmap (2025)

A structured, market-aligned study plan to become an AI Engineer — focused on what companies actually hire for today: LLM integration, RAG, evaluation, production systems, and cost optimization.

**Profile:** Intermediate Python, moderate math, familiar with AI tools (Claude Code, etc.)
**Commitment:** 15-25 hours/week
**Structure:** 5 phases over 12 weeks (3 months)
**Philosophy:** LLM-first, production-focused, learn by building with AI assistance

---

## Why 3 Months Is Possible

This accelerated timeline works because:

| Traditional Learning | Learning with Claude |
|---------------------|---------------------|
| Watch 4-hour course → take notes → get stuck → search forums | Ask Claude → get tailored explanation → build immediately |
| Debug alone for hours | Explain error → get fix + understanding in seconds |
| Read docs hoping to understand | "Explain this like I'm a backend dev" → instant clarity |
| Build alone, hope it's right | Real-time pair programming and code review |
| Wait for course to cover your question | Ask exactly what you need, when you need it |

**You skip hours of friction per concept.**

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

## 12-Week Accelerated Timeline

```
┌─────────────────────────────────────────────────────────────────┐
│  MONTH 1: FOUNDATIONS + TRANSFORMERS                            │
│  ┌─────────────┐  ┌─────────────┐                               │
│  │ Week 1-2    │  │ Week 3-4    │                               │
│  │ ML Core +   │  │ Transformers│                               │
│  │ Embeddings  │  │ Deep-Dive   │                               │
│  │ Project 1   │  │ Project 2   │                               │
│  └─────────────┘  └─────────────┘                               │
├─────────────────────────────────────────────────────────────────┤
│  MONTH 2: LLM ENGINEERING (THE CORE)                            │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐              │
│  │ Week 5-6    │  │ Week 7-8    │  │ Week 9      │              │
│  │ LLM APIs +  │  │ RAG         │  │ Evaluation  │              │
│  │ Prompting   │  │ Systems     │  │ + Agents    │              │
│  │ Project 3   │  │ Project 4   │  │ Project 5   │              │
│  └─────────────┘  └─────────────┘  └─────────────┘              │
├─────────────────────────────────────────────────────────────────┤
│  MONTH 3: PRODUCTION + SPECIALIZATION                           │
│  ┌─────────────┐  ┌─────────────┐                               │
│  │ Week 10-11  │  │ Week 12     │                               │
│  │ Production  │  │ Specialize  │                               │
│  │ + Security  │  │ + Portfolio │                               │
│  │ Project 6   │  │ Polish      │                               │
│  └─────────────┘  └─────────────┘                               │
└─────────────────────────────────────────────────────────────────┘
```

---

## Ongoing: Math (Just-in-Time)

**Learn math when you hit a concept that requires it, not upfront.**

| When You Encounter | Learn | Resource |
|-------------------|-------|----------|
| Embeddings, similarity | Dot products, cosine similarity | [3Blue1Brown Linear Algebra](https://www.youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab) Ch 1-4 |
| Backpropagation | Chain rule, gradients | [3Blue1Brown Calculus](https://www.youtube.com/playlist?list=PLZHQObOWTQDMsr9K-rj53DwVRMYO3t5Yr) Ch 1-4 |
| Evaluation metrics | Probability basics | [StatQuest](https://www.youtube.com/@statquest) as needed |

> **Rule:** Embeddings → learn dot products. Backprop → learn chain rule. Just-in-time, not just-in-case.

---

## Phase 1: Foundations + Embeddings (Weeks 1-2)

**Goal:** Understand ML evaluation, embeddings, and why things work — in 2 weeks, not 8.

### Week 1: ML Core Concepts

| Focus | How to Learn |
|-------|--------------|
| Evaluation metrics (precision, recall, F1, AUC) | Ask Claude to explain with examples from your domain |
| Train/test splits, overfitting | [Kaggle Intro to ML](https://www.kaggle.com/learn/intro-to-machine-learning) micro-course (3-4 hours) |
| When to use ML vs rules vs LLMs | Discuss tradeoffs with Claude |

**Build:** Simple classifier with scikit-learn. Focus on evaluation, not the model.

### Week 2: Embeddings Deep-Dive

| Focus | How to Learn |
|-------|--------------|
| What embeddings are, how they encode meaning | [What Are Word Embeddings?](https://jalammar.github.io/illustrated-word2vec/) — Jay Alammar |
| Similarity metrics (cosine, dot product, euclidean) | Ask Claude to explain + show code |
| Embedding models comparison | Experiment with sentence-transformers |

**Project 1:** Build an embedding-based semantic search. Given a query, find similar documents. Visualize embeddings with t-SNE or UMAP. GitHub repo.

**Key concepts checklist:**
- [ ] Evaluation metrics: when to use which
- [ ] Overfitting and how to detect it
- [ ] What embeddings represent
- [ ] Similarity search basics

---

## Phase 2: Transformers Deep-Dive (Weeks 3-4)

**Goal:** Understand how LLMs actually work — attention, tokenization, context windows — so you can debug and optimize.

### Week 3: Transformer Architecture

| Focus | How to Learn |
|-------|--------------|
| Self-attention mechanism | [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/) + ask Claude to clarify |
| Multi-head attention, positional encoding | [Hugging Face NLP Course](https://huggingface.co/learn/nlp-course) — Chapters 1-2 |
| Tokenization (BPE, token counts) | Experiment with different tokenizers in code |

**Build:** Tokenize various texts, count tokens, understand context limits hands-on.

### Week 4: How LLMs Are Trained

| Focus | How to Learn |
|-------|--------------|
| Pre-training vs fine-tuning vs RLHF | [What Is ChatGPT Doing?](https://writings.stephenwolfram.com/2023/02/what-is-chatgpt-doing-and-why-does-it-work/) — Wolfram |
| Inference parameters (temperature, top-p) | Experiment with Anthropic/OpenAI APIs |
| Fine-tuning basics | [Hugging Face NLP Course](https://huggingface.co/learn/nlp-course) — Chapters 3-4 |

**Project 2:** Fine-tune a small model (DistilBERT) on a classification task. Understand the training loop. GitHub repo.

**Key concepts checklist:**
- [ ] Self-attention intuition
- [ ] Tokenization and context windows
- [ ] Pre-training vs fine-tuning vs RLHF
- [ ] Temperature, top-p, sampling

**Reading:**
- ["Attention Is All You Need"](https://arxiv.org/abs/1706.03762) — skim for concepts, not math
- [The Illustrated GPT-2](https://jalammar.github.io/illustrated-gpt2/)

---

## Phase 3: Applied LLM Engineering (Weeks 5-9)

**Goal:** This is the core. RAG, agents, evaluation, prompt engineering. Where you'll spend 50% of your time.

### Week 5-6: LLM APIs + Prompt Engineering

| Focus | How to Learn |
|-------|--------------|
| Anthropic API (messages, system prompts, tool use) | [Anthropic API Docs](https://docs.anthropic.com/en/api/getting-started) + [Anthropic Courses](https://github.com/anthropics/courses) |
| Prompt patterns (few-shot, chain-of-thought, structured outputs) | [Anthropic Prompt Engineering Guide](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview) |
| Tool use / function calling | [Anthropic Cookbook](https://github.com/anthropics/anthropic-cookbook) examples |

**Project 3:** LLM app with structured outputs and tool use — an assistant that can search, calculate, call APIs, and return typed JSON. GitHub repo.

**Key concepts checklist:**
- [ ] System / user / assistant roles
- [ ] Few-shot prompting
- [ ] Chain-of-thought
- [ ] Structured outputs (JSON mode, tool use)
- [ ] Prompt versioning

### Week 7-8: RAG — The Non-Negotiable Skill

| Focus | How to Learn |
|-------|--------------|
| RAG architecture end-to-end | DeepLearning.AI: [LangChain for LLM Application Dev](https://www.deeplearning.ai/short-courses/langchain-for-llm-application-development/) |
| Chunking strategies | Experiment: fixed vs semantic, different sizes, overlap |
| Vector databases | [Chroma](https://docs.trychroma.com/) (start here), [Pinecone](https://www.pinecone.io/), [Weaviate](https://weaviate.io/) |
| Re-ranking, hybrid search | Implement and compare retrieval quality |

**Project 4:** Production-quality RAG system — PDF ingestion, smart chunking, retrieval with citations, answer generation. Measure retrieval quality. GitHub repo.

**Key concepts checklist:**
- [ ] Chunking: size, overlap, semantic vs fixed
- [ ] Vector DB: indexing, querying, filtering, metadata
- [ ] Retrieval metrics: precision, recall, MRR
- [ ] Re-ranking strategies
- [ ] Caching for embeddings

### Week 9: Evaluation + Agents

| Focus | How to Learn |
|-------|--------------|
| LLM evaluation without ground truth | [RAGAS](https://docs.ragas.io/), [DeepEval](https://docs.confident-ai.com/) |
| RAG metrics (faithfulness, relevance) | Build evaluation pipeline for Project 4 |
| Agent patterns (ReAct, tool use, memory) | DeepLearning.AI: [Building Agentic RAG](https://www.deeplearning.ai/short-courses/) |
| MCP (Model Context Protocol) | [MCP Docs](https://modelcontextprotocol.io/) |

**Project 5:** AI agent with multi-step reasoning, multiple tools, memory, and error handling. Add evaluation suite to Project 4. GitHub repo.

**Key concepts checklist:**
- [ ] Evaluation without ground truth
- [ ] RAG metrics: faithfulness, context precision
- [ ] Golden datasets
- [ ] ReAct pattern
- [ ] Agent memory (short-term, long-term)
- [ ] MCP basics

**Reading:**
- [LLM Powered Autonomous Agents](https://lilianweng.github.io/posts/2023-06-23-agent/) — Lilian Weng
- [RAG paper](https://arxiv.org/abs/2005.11401)

---

## Phase 4: Production AI Systems (Weeks 10-11)

**Goal:** Ship reliable, cost-effective, secure AI applications. This separates demos from products.

### Week 10: Backend + Deployment

| Focus | How to Learn |
|-------|--------------|
| FastAPI for AI apps | [FastAPI Tutorial](https://fastapi.tiangolo.com/tutorial/) — async, streaming |
| Docker | [Docker Get Started](https://docs.docker.com/get-started/) |
| Streaming LLM responses | Implement in your API |
| Cloud deployment | AWS Lambda / GCP Cloud Run / Railway |

**Build:** Containerize and deploy Project 4 or 5 as an API with streaming.

### Week 11: Cost, Performance, Security

| Focus | How to Learn |
|-------|--------------|
| Token cost management | Build cost tracking into your app |
| Caching strategies (Redis) | Cache embeddings and repeated queries |
| Model routing (cheap → expensive) | Implement Haiku-first, Sonnet-fallback |
| LLM security | Prompt injection, PII handling, output filtering |
| Observability | [LangSmith](https://smith.langchain.com/) or [Helicone](https://helicone.ai/) |

**Project 6:** Production-deployed full stack — API + RAG + caching + cost tracking + security layers + monitoring + CI/CD. GitHub repo with deployment instructions.

**Key concepts checklist:**
- [ ] Async Python, streaming
- [ ] Docker containerization
- [ ] Token counting and cost calculation
- [ ] Caching strategies
- [ ] Model routing
- [ ] Prompt injection defense
- [ ] PII detection
- [ ] CI/CD for AI apps
- [ ] Monitoring and observability

---

## Phase 5: Specialization + Portfolio (Week 12)

**Goal:** Pick a direction, polish your portfolio, prepare for opportunities.

### Week 12: Specialize and Ship

| Focus | Action |
|-------|--------|
| Choose specialization | RAG Systems, AI Agents, LLM Security, AI Infrastructure, or Fine-tuning |
| Portfolio polish | Clean READMEs, add diagrams, record demo videos |
| Write about your learning | Blog post or detailed GitHub docs |
| Open source | One PR to LangChain, Anthropic Cookbook, or similar |

**Specialization options:**

| Track | What to Build |
|-------|---------------|
| RAG Systems | Advanced retrieval with re-ranking, evaluation dashboard |
| AI Agents | Multi-agent system, complex tool orchestration |
| LLM Security | Red team toolkit, guardrail library |
| AI Infrastructure | LLM gateway with routing, caching, observability |
| Fine-tuning | LoRA fine-tune for specific domain, evaluation suite |

---

## Weekly Schedule (~20 hours/week)

```
Monday:      Study — docs, courses, papers (3 hrs)
Tuesday:     Study + hands-on exercises (3 hrs)
Wednesday:   Build — project work with Claude (4 hrs)
Thursday:    Build — project work with Claude (4 hrs)
Friday:      Build — finish weekly milestone (3 hrs)
Saturday:    Review + math if needed + reading (2 hrs)
Sunday:      Rest or light exploration
```

---

## How to Use Claude Effectively

```python
# Learning a concept
"Explain [embeddings] like I'm a backend dev who knows Python
 but is new to ML. Give me a concrete code example."

# Building
"I want to build [RAG system]. Walk me through the architecture
 first, then let's implement step by step."

# Debugging understanding
"I don't understand why [attention] works. What's the intuition?
 Skip the math, give me the mental model."

# Code review
"Review this [RAG implementation]. What would a senior AI engineer
 at Anthropic change? Be specific."

# Unstuck
"I'm getting [error]. Here's my code. What's wrong and why?"
```

---

## GitHub Portfolio at Week 12

| # | Project | What It Demonstrates |
|---|---------|---------------------|
| 1 | Semantic search with embeddings | Embeddings, similarity, evaluation basics |
| 2 | Fine-tuned classifier | Transformers, training loop, Hugging Face |
| 3 | LLM app with tools | API integration, structured outputs, tool use |
| 4 | RAG system + evaluation | Chunking, retrieval, vector DB, metrics |
| 5 | AI agent with memory | Multi-step reasoning, planning, error handling |
| 6 | Production full stack | Docker, API, caching, security, monitoring, cloud |

---

## Weekly Milestones

| Week | Milestone | Proof |
|------|-----------|-------|
| 2 | Understand embeddings, built semantic search | Project 1 on GitHub |
| 4 | Explain transformers, fine-tuned a model | Project 2 on GitHub |
| 6 | Build LLM apps with tools and structured outputs | Project 3 on GitHub |
| 8 | Build production-quality RAG | Project 4 on GitHub |
| 9 | Build agents, evaluate LLM systems | Project 5 on GitHub |
| 11 | Deploy secure, cost-optimized AI app | Project 6 on GitHub |
| 12 | Specialization chosen, portfolio polished | All projects documented |

---

## Core Skills Checklist

### Tier 1: Get Hired (Weeks 1-9)
- [ ] Embeddings and similarity search
- [ ] RAG: chunking, retrieval, vector databases
- [ ] LLM APIs: Anthropic, OpenAI — structured outputs, tool use
- [ ] Prompt engineering: few-shot, CoT, versioning
- [ ] Basic evaluation: know if your system works

### Tier 2: Stand Out (Weeks 9-11)
- [ ] Advanced evaluation: RAGAS, golden datasets
- [ ] Cost optimization: caching, model routing
- [ ] Agents: ReAct, tool use, memory, MCP
- [ ] LLM security: prompt injection, PII
- [ ] Production: Docker, CI/CD, monitoring

### Tier 3: Keep Growing (Week 12+)
- [ ] Product judgment: when NOT to use LLMs
- [ ] Fine-tuning: LoRA, dataset curation
- [ ] System design at scale
- [ ] Open source contributions

---

## Resources Index

### Core Documentation
- [Anthropic API Docs](https://docs.anthropic.com/en/api/getting-started)
- [Anthropic Prompt Engineering Guide](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview)
- [Anthropic Courses](https://github.com/anthropics/courses)
- [Anthropic Cookbook](https://github.com/anthropics/anthropic-cookbook)
- [Model Context Protocol (MCP)](https://modelcontextprotocol.io/)
- [LangChain Documentation](https://python.langchain.com/docs/get_started/introduction)

### Short Courses (Do These)
- [Hugging Face NLP Course](https://huggingface.co/learn/nlp-course) — Chapters 1-4 only
- [DeepLearning.AI Short Courses](https://www.deeplearning.ai/short-courses/) — LangChain, RAG, Agents
- [Kaggle Intro to ML](https://www.kaggle.com/learn/intro-to-machine-learning) — 3-4 hours

### Evaluation & Observability
- [RAGAS](https://docs.ragas.io/) — RAG evaluation
- [DeepEval](https://docs.confident-ai.com/) — LLM testing
- [LangSmith](https://smith.langchain.com/) — observability
- [Helicone](https://helicone.ai/) — LLM monitoring

### Visual Guides (Essential)
- [Jay Alammar](https://jalammar.github.io/) — Illustrated Transformer, GPT-2, BERT, Word2Vec
- [Lilian Weng](https://lilianweng.github.io/) — LLM Agents, RAG
- [3Blue1Brown](https://www.youtube.com/@3blue1brown) — Math when needed

### Key Papers (Skim, Don't Study)
- ["Attention Is All You Need"](https://arxiv.org/abs/1706.03762) — understand the concepts
- ["RAG for Knowledge-Intensive NLP"](https://arxiv.org/abs/2005.11401) — understand the pattern

---

## What's Different About This Plan

| Traditional (2020-2023) | This Plan (2025, 3 months) |
|------------------------|---------------------------|
| 8+ weeks on classical ML | 2 weeks, focused on evaluation + embeddings |
| 12 weeks on deep learning | 2 weeks, transformers only |
| First LLM project at week 21 | First LLM project at week 5 |
| Learn alone, get stuck | Learn with Claude, build faster |
| 10-12 months | 12 weeks |
| Courses then projects | Projects from day 1 |

---

## The 3-Month Commitment

```
Week 1-2:   Foundations + Embeddings     → Project 1
Week 3-4:   Transformers                 → Project 2
Week 5-6:   LLM APIs + Prompting         → Project 3
Week 7-8:   RAG Systems                  → Project 4
Week 9:     Evaluation + Agents          → Project 5
Week 10-11: Production + Security        → Project 6
Week 12:    Specialize + Polish          → Portfolio ready
```

**By week 12:** 6 projects on GitHub, production deployment experience, evaluation skills, and a specialization direction.

---

> **Note:** This is aggressive but achievable with focused effort and AI-assisted learning. The key is building every week, not just consuming content. You learn by doing, and Claude accelerates the doing.
