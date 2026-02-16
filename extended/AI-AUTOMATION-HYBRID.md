# AI Engineer + Automation Hybrid Roadmap (5-6 Months)

> **This is a compressed hybrid version** for developers with programming fundamentals who want to combine AI Engineering with process automation (n8n, Make, etc.). Designed for AI-assisted learning with tools like Claude.

**Profile:** Developer with Python fundamentals, SQL, APIs, Git basics
**Commitment:** 15-20 hours/week
**Duration:** 5-6 months
**Philosophy:** LLM-first, automation-focused, learn by building with AI assistance

---

## Why This Hybrid Path?

| Traditional Learning | AI-Assisted Learning |
|---------------------|----------------------|
| Read docs for 2 hours | Ask Claude, get working example in 5 min |
| Debug solo for 1 hour | "Why does this fail?" → immediate solution |
| Search tutorials | "Teach me X with working code" |
| Design architecture alone | "Design system for Y, give me pros/cons" |

**The combination of AI Engineering + Automation is highly demanded:**
- Companies need intelligent workflows, not just rule-based automation
- LLMs transform simple automations into smart systems
- This hybrid profile is rare and valuable

---

## Priority Stack

```
Tier 1 — Must-Have (Foundational):
  ├── Automation platforms (n8n, Make)
  ├── LLM APIs (Anthropic, OpenAI — tool use, structured outputs)
  ├── RAG (embeddings, chunking, retrieval, vector DBs)
  ├── Backend skills (Python, APIs, async, error handling)
  └── Prompt engineering (versioning, testing, guardrails)

Tier 2 — Differentiators:
  ├── Advanced RAG (re-ranking, evaluation)
  ├── Agentic systems (planning, tool use, memory)
  ├── Cost optimization (caching, batching, model selection)
  ├── LLM security (prompt injection, PII, output filtering)
  └── Production ops (monitoring, deployment, CI/CD)

Tier 3 — Senior/Lead Level:
  ├── Product judgment (when NOT to use LLMs)
  ├── Multi-agent orchestration
  ├── System design for AI at scale
  └── Fine-tuning techniques (LoRA)
```

---

## Timeline Overview

```
Month 1        →  Automation + AI Basics (parallel)
Month 2-3      →  AI Applied (RAG, Agents, APIs)
Month 4-5      →  Production + Specialization
Month 6        →  Portfolio + Real Projects
```

---

## Month 1: Automation + AI Basics (Parallel Track)

### Week 1-2: Foundations

| Day | Morning (2h) | Afternoon (2h) |
|-----|--------------|----------------|
| Mon-Tue | n8n: installation, nodes, first workflow | Claude API: first call, structured outputs |
| Wed-Thu | n8n: webhooks, HTTP requests | Prompting: few-shot, chain-of-thought |
| Fri | **Project**: n8n workflow using Claude API |

**n8n Core Concepts:**
- [ ] Installation (Docker or cloud)
- [ ] Basic nodes: HTTP Request, Webhook, IF, Set
- [ ] Triggers: Schedule, Webhook, Email
- [ ] Error handling and retries
- [ ] Credentials management

**Claude API Basics:**
- [ ] API authentication and setup
- [ ] Message roles (system, user, assistant)
- [ ] Structured outputs (JSON mode)
- [ ] Basic tool use

### Week 3-4: Integration

| Focus | Topics | Deliverable |
|-------|--------|-------------|
| n8n + Claude | Classification, extraction, summarization | Automated email classifier |
| Data pipelines | Sheets ↔ DB sync, API integrations | Data sync workflow |
| **Project** | Complete system: input → AI processing → action | Intelligent automation |

**Key concepts to nail:**
- [ ] n8n expressions and data transformation
- [ ] Connecting multiple services
- [ ] Error handling in workflows
- [ ] Claude API integration in n8n

---

## Month 2-3: AI Core

### Week 5-6: Embeddings & Semantic Search

| Week | Study (40%) | Build (60%) |
|------|-------------|-------------|
| 5 | What embeddings are, how they encode meaning. [Jay Alammar's illustrated guides](https://jalammar.github.io/illustrated-word2vec/) | Experiment with sentence-transformers |
| 6 | Similarity metrics (cosine, dot product). Embedding model comparison | **Project 1:** Semantic search application with t-SNE/UMAP visualization |

**Key concepts:**
- [ ] Vector representations of text
- [ ] Cosine similarity and distance metrics
- [ ] Embedding model selection (OpenAI, Cohere, open-source)
- [ ] Visualization techniques

### Week 7-8: RAG Fundamentals

| Week | Study (40%) | Build (60%) |
|------|-------------|-------------|
| 7 | RAG architecture end-to-end. Chunking strategies (fixed vs semantic) | Build RAG from scratch (no frameworks) |
| 8 | Vector databases ([Chroma](https://docs.trychroma.com/), [Pinecone](https://www.pinecone.io/)). Re-ranking basics | **Project 2:** RAG with PDF ingestion and citations |

**Key concepts:**
- [ ] Document ingestion and preprocessing
- [ ] Chunking: size, overlap, semantic boundaries
- [ ] Vector database operations (upsert, query, filter)
- [ ] Retrieval quality metrics

### Week 9-10: Advanced RAG & Evaluation

| Week | Study (40%) | Build (60%) |
|------|-------------|-------------|
| 9 | RAG evaluation: faithfulness, relevance, context precision. [RAGAS](https://docs.ragas.io/) | Build evaluation pipeline |
| 10 | Hybrid search, re-ranking, citation management | **Project 3:** Production RAG with evaluation dashboard |

**Key concepts:**
- [ ] Evaluation without ground truth
- [ ] Golden datasets creation
- [ ] A/B testing retrieval strategies
- [ ] Re-ranking and hybrid search

### Week 11-12: Agents & Tool Use

| Week | Study (40%) | Build (60%) |
|------|-------------|-------------|
| 11 | Agent patterns: ReAct, planning, memory. [Lilian Weng's agent guide](https://lilianweng.github.io/posts/2023-06-23-agent/) | Build simple agent with tools |
| 12 | [MCP (Model Context Protocol)](https://modelcontextprotocol.io/). Multi-step reasoning | **Project 4:** AI agent with reasoning, multiple tools, memory |

**Key concepts:**
- [ ] ReAct pattern (Reasoning + Acting)
- [ ] Tool use and function calling
- [ ] Agent memory (conversation and long-term)
- [ ] Error handling and recovery
- [ ] MCP for system integration

---

## Month 4-5: Production Systems

### Week 13-14: Backend & Deployment

| Week | Study (40%) | Build (60%) |
|------|-------------|-------------|
| 13 | [FastAPI](https://fastapi.tiangolo.com/) for AI apps. Async patterns, streaming | API wrapper for RAG project |
| 14 | Docker fundamentals. Cloud deployment (Railway, Render) | Containerize and deploy |

**Key concepts:**
- [ ] Async Python (asyncio)
- [ ] Streaming LLM responses
- [ ] Docker containerization
- [ ] Cloud deployment options

### Week 15-16: Cost, Performance, Security

| Week | Study (40%) | Build (60%) |
|------|-------------|-------------|
| 15 | Token counting, caching (Redis), model routing | Implement caching layer |
| 16 | LLM security: prompt injection, PII handling, output filtering | Add security layers |

**Key concepts:**
- [ ] Token cost calculation
- [ ] Aggressive caching strategies
- [ ] Model routing (cheap → expensive fallback)
- [ ] Prompt injection defense
- [ ] PII detection and handling

### Week 17-18: Observability & CI/CD

| Week | Study (40%) | Build (60%) |
|------|-------------|-------------|
| 17 | LLM observability ([LangSmith](https://smith.langchain.com/), [Helicone](https://helicone.ai/)) | Add monitoring to projects |
| 18 | CI/CD for AI applications. Rollback strategies | **Project 5:** Full production deployment with monitoring |

**Key concepts:**
- [ ] Logging and tracing LLM calls
- [ ] Cost and latency monitoring
- [ ] Prompt versioning in production
- [ ] Automated testing for AI

---

## Month 6: Specialization & Portfolio

### Week 19-20: Advanced Integration

| Focus | Topics | Deliverable |
|-------|--------|-------------|
| n8n + RAG | RAG as n8n service, webhook integrations | Knowledge base automation |
| Multi-system | Connect multiple services with AI processing | Enterprise workflow |

### Week 21-22: Specialization Track

Choose one focus area:

| Track | Focus | Final Project |
|-------|-------|---------------|
| **Intelligent Automation** | n8n + AI for business processes | No-code AI platform |
| **RAG Systems** | Advanced retrieval, evaluation | Enterprise knowledge base |
| **AI Agents** | Multi-agent, complex orchestration | Autonomous task executor |
| **AI Infrastructure** | Scaling, optimization, gateways | LLM gateway with routing |

### Week 23-24: Portfolio Polish

- Clean GitHub repos with detailed READMEs
- Architecture diagrams and demo videos
- Write about your learning journey
- Contribute to open source (LangChain, Anthropic Cookbook, n8n)

---

## Effective Claude Usage Patterns

**Learning new concepts:**
```
"Explain [topic] like I'm a backend dev who knows Python but is new to ML.
Give me concrete code examples."
```

**Building systems:**
```
"I want to build [system]. Walk me through the architecture first,
then let's implement step by step."
```

**Understanding gaps:**
```
"I don't understand why [concept] works. What's the intuition?
Skip the math, give me the mental model."
```

**Code review:**
```
"Review this [implementation]. What would a senior AI engineer change?
Be specific."
```

**Debugging:**
```
"I'm getting [error]. Here's my code. What's wrong and why?"
```

---

## Six-Project Portfolio

| # | Project | Demonstrates |
|---|---------|--------------|
| 1 | n8n + Claude integration | Automation, API integration, workflows |
| 2 | Semantic search with embeddings | Embeddings, similarity, evaluation |
| 3 | Production RAG system | Chunking, retrieval, vector DBs, metrics |
| 4 | AI agent with memory | Multi-step reasoning, planning, tools |
| 5 | Full production deployment | Docker, API, caching, security, monitoring |
| 6 | Specialization project | Deep expertise in chosen area |

---

## Tools to Master

| Category | Tool | Priority |
|----------|------|----------|
| Automation | n8n | High |
| Automation | Make (backup) | Medium |
| AI APIs | Anthropic Claude | High |
| AI APIs | OpenAI | Medium |
| Vector DB | Chroma (local) | High |
| Vector DB | Pinecone (cloud) | Medium |
| Backend | FastAPI | High |
| Caching | Redis | Medium |
| Deploy | Railway / Docker | High |
| Observability | LangSmith / Helicone | Medium |

---

## Weekly Schedule (~18 hours)

```
Monday:      Study (docs, courses) — 3 hours
Tuesday:     Study + hands-on exercises — 3 hours
Wednesday:   Build with AI assistance — 4 hours
Thursday:    Build with AI assistance — 4 hours
Friday:      Complete weekly milestone — 2 hours
Saturday:    Review and exploration — 2 hours
Sunday:      Rest
```

---

## Core Skills Checklist

### Tier 1: Foundations (Months 1-3)
- [ ] n8n workflows and integrations
- [ ] LLM API usage (structured outputs, tool use)
- [ ] Embeddings and similarity search
- [ ] RAG complete pipeline
- [ ] Prompt engineering (few-shot, CoT, versioning)
- [ ] Basic evaluation

### Tier 2: Production (Months 4-5)
- [ ] Advanced evaluation (RAGAS, golden datasets)
- [ ] Agentic patterns and memory
- [ ] Cost optimization and model routing
- [ ] LLM security and PII handling
- [ ] Production deployment and monitoring

### Tier 3: Specialization (Month 6+)
- [ ] Advanced automation patterns
- [ ] Multi-agent systems
- [ ] System design for AI at scale
- [ ] Fine-tuning techniques
- [ ] Open source contributions

---

## Resources Index

### Automation
- [n8n Documentation](https://docs.n8n.io/)
- [n8n YouTube Channel](https://www.youtube.com/@n8n-io)
- [Make (Integromat) Academy](https://www.make.com/en/academy)

### AI Documentation
- [Anthropic API Docs](https://docs.anthropic.com/en/api/getting-started)
- [Anthropic Prompt Engineering Guide](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview)
- [Anthropic Cookbook](https://github.com/anthropics/anthropic-cookbook)
- [Model Context Protocol (MCP)](https://modelcontextprotocol.io/)
- [OpenAI API Docs](https://platform.openai.com/docs)

### Courses
- [Hugging Face NLP Course](https://huggingface.co/learn/nlp-course) — free, essential
- [DeepLearning.AI Short Courses](https://www.deeplearning.ai/short-courses/) — LangChain, RAG, Agents

### Evaluation & Observability
- [RAGAS](https://docs.ragas.io/) — RAG evaluation
- [LangSmith](https://smith.langchain.com/) — observability
- [Helicone](https://helicone.ai/) — LLM observability

### Visual Guides & Blogs
- [Jay Alammar](https://jalammar.github.io/) — essential visual explanations
- [Lilian Weng](https://lilianweng.github.io/) — in-depth AI research
- [Simon Willison](https://simonwillison.net/) — LLM ecosystem tracking

---

## Comparison with Other Versions

| Aspect | This (Hybrid) | Extended (6-7mo) | Accelerated (3mo) |
|--------|---------------|------------------|-------------------|
| Duration | 5-6 months | 6-7 months | 3 months |
| Hours/week | 15-20 hours | 10-15 hours | 15-25 hours |
| Focus | AI + Automation | Pure AI Engineering | Pure AI Engineering |
| Automation | Core skill | Not covered | Not covered |
| Best for | Hybrid profile | Part-time learners | Full commitment |

---

> **Note:** This roadmap assumes AI-assisted learning with tools like Claude. The timeline is compressed compared to traditional learning because you have instant access to explanations, debugging help, and code review. Use this advantage strategically.
