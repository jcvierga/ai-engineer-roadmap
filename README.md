# AI Engineer Roadmap

A structured study plan to become an AI Engineer — covering Machine Learning, Deep Learning, Large Language Models, and Production AI Systems.

**Profile:** Intermediate Python, moderate math, familiar with AI tools
**Commitment:** 10-20 hours/week
**Structure:** 5 phases over ~10 months

---

## Ongoing Side-Track: Math (Throughout Entire Plan)

**Runs parallel to all phases — dedicate 2-3 hours/week separately**

| Alongside Phase | Math Focus | Resource |
|----------------|-----------|----------|
| Phase 1 | Linear Algebra (vectors, matrices, transformations) | [Math for ML Specialization — Course 1](https://www.coursera.org/specializations/mathematics-machine-learning) (Coursera) + [3Blue1Brown Essence of Linear Algebra](https://www.youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab) |
| Phase 2 | Multivariate Calculus (gradients, chain rule, optimization) | Math for ML Specialization — Course 2 + [3Blue1Brown Essence of Calculus](https://www.youtube.com/playlist?list=PLZHQObOWTQDMsr9K-rj53DwVRMYO3t5Yr) |
| Phase 3 | Probability & Statistics (distributions, Bayes, MLE) | Math for ML Specialization — Course 3 + [StatQuest YouTube](https://www.youtube.com/@statquest) |
| Phase 4-5 | Information theory, attention mechanics, loss functions | Papers + blog posts as needed ([Chris Olah's blog](https://colah.github.io/), [Lilian Weng's blog](https://lilianweng.github.io/)) |

> **Rule:** Math supports the main track, never blocks it. If you're in Phase 2 studying neural networks and the calculus hasn't fully clicked yet, keep going — they reinforce each other.

---

## Phase 1: Machine Learning Foundations (Weeks 1-8)

**Goal:** Understand core ML algorithms, evaluation, and the full ML workflow

| Week | Study (50%) | Build (50%) |
|------|------------|-------------|
| 1-2 | [Andrew Ng's ML Specialization](https://www.coursera.org/specializations/machine-learning-introduction) — Course 1: Supervised Learning (linear/logistic regression, regularization) | [Kaggle Intro to ML](https://www.kaggle.com/learn/intro-to-machine-learning) micro-course. Start [Titanic competition](https://www.kaggle.com/competitions/titanic) |
| 3-4 | ML Specialization — Course 1 continued (SVMs, decision trees, ensembles) | Kaggle micro-courses: [Intermediate ML](https://www.kaggle.com/learn/intermediate-machine-learning) + [Feature Engineering](https://www.kaggle.com/learn/feature-engineering) |
| 5-6 | ML Specialization — Course 2: Advanced Learning Algorithms (neural network intro, trees, advice for ML) | Kaggle [House Prices](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques) competition — full pipeline |
| 7-8 | ML Specialization — Course 3: Unsupervised Learning, Recommenders, Reinforcement Learning | **Project 1:** End-to-end ML pipeline — real dataset, data cleaning, feature engineering, model comparison, evaluation metrics. Scikit-learn. GitHub repo with README and tests |

**Key concepts to nail:**
- [ ] Bias/variance tradeoff
- [ ] Cross-validation
- [ ] Precision, recall, F1, AUC-ROC
- [ ] Feature engineering
- [ ] When to use which algorithm

**Reading:** [Jay Alammar's visual ML guides](https://jalammar.github.io/), Kaggle winning solution write-ups

---

## Phase 2: Deep Learning (Weeks 9-20)

**Goal:** Understand neural networks deeply, master PyTorch, grasp the transformer architecture

| Week | Study (50%) | Build (50%) |
|------|------------|-------------|
| 9-10 | [Deep Learning Specialization](https://www.coursera.org/specializations/deep-learning) — Course 1: Neural Networks & Deep Learning | Implement a 2-layer neural network from scratch in NumPy (no frameworks) |
| 11-12 | Deep Learning Specialization — Course 2: Improving Deep Neural Networks (hyperparameters, regularization, optimization) | [PyTorch official tutorials](https://pytorch.org/tutorials/) — tensors, autograd, nn.Module |
| 13-14 | Deep Learning Specialization — Course 4: Convolutional Neural Networks | Build an image classifier in PyTorch (CIFAR-10 or custom dataset) |
| 15-16 | Deep Learning Specialization — Course 5: Sequence Models (RNNs, LSTMs, attention mechanism) | [Fast.ai Practical Deep Learning](https://course.fast.ai/) — Lessons 1-7 (practical complement to Ng's theory) |
| 17-18 | [Hugging Face NLP Course](https://huggingface.co/learn/nlp-course) — Chapters 1-4 (Transformers, tokenizers, fine-tuning) | Run and modify Hugging Face examples, experiment with pre-trained models |
| 19-20 | Fast.ai continued + review | **Project 3:** Fine-tune a pre-trained transformer model (BERT or similar) on a custom task. GitHub repo |

**Key concepts to nail:**
- [ ] Backpropagation (be able to explain it clearly)
- [ ] CNNs: convolutions, pooling, architectures (ResNet, etc.)
- [ ] RNNs/LSTMs: sequence modeling, vanishing gradients
- [ ] Transformers: self-attention, multi-head attention, positional encoding
- [ ] Transfer learning and fine-tuning

**Reading:**
- ["Attention Is All You Need"](https://arxiv.org/abs/1706.03762) paper
- [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/) — Jay Alammar
- [The Illustrated BERT](https://jalammar.github.io/illustrated-bert/) — Jay Alammar

---

## Phase 3: Large Language Models & Applied AI (Weeks 21-34)

**Goal:** Deep understanding of LLMs, build real applications with RAG, agents, and tool use

### 3A: LLM Fundamentals (Weeks 21-26)

| Week | Study (50%) | Build (50%) |
|------|------------|-------------|
| 21-22 | [Generative AI with LLMs](https://www.coursera.org/learn/generative-ai-with-llms) (Coursera — AWS + DeepLearning.AI) — training, fine-tuning, RLHF, scaling laws | Set up [Anthropic API](https://docs.anthropic.com/en/api/getting-started) + [OpenAI API](https://platform.openai.com/docs). Build basic chat apps with both |
| 23-24 | Hugging Face NLP Course — Chapters 5-8 (advanced tokenization, embeddings, model internals) | Experiment with embeddings — visualize them, compare similarity, build a semantic search prototype |
| 25-26 | [Anthropic Courses](https://github.com/anthropics/courses) (GitHub) — prompt engineering, tool use, real patterns | [Anthropic Cookbook](https://github.com/anthropics/anthropic-cookbook) — implement 3-4 examples, modify them, understand the patterns |

### 3B: RAG & Vector Databases (Weeks 27-30)

| Week | Study (50%) | Build (50%) |
|------|------------|-------------|
| 27-28 | DeepLearning.AI: [LangChain for LLM Application Dev](https://www.deeplearning.ai/short-courses/langchain-for-llm-application-development/) + [LangChain Chat with Your Data](https://www.deeplearning.ai/short-courses/langchain-chat-with-your-data/) | Build a basic RAG pipeline from scratch (without frameworks) — embeddings + vector store + retrieval + generation |
| 29-30 | Study vector databases ([Chroma](https://docs.trychroma.com/), [Pinecone](https://www.pinecone.io/), [Weaviate](https://weaviate.io/) docs). Understand chunking strategies, retrieval metrics, re-ranking | **Project 4:** Document Q&A system — upload PDFs, chunk, embed, retrieve, answer using Anthropic API. GitHub repo |

### 3C: Agents & Tool Use (Weeks 31-34)

| Week | Study (50%) | Build (50%) |
|------|------------|-------------|
| 31-32 | DeepLearning.AI: [Building Agentic RAG](https://www.deeplearning.ai/short-courses/) + Functions, Tools and Agents with LangChain | Build a simple agent that uses 2-3 tools (web search, calculator, file reader) |
| 33-34 | [AI Engineering Specialization](https://www.coursera.org/specializations/ai-engineering) (Coursera) — agent architectures, orchestration, evaluation | **Project 5:** AI agent that solves a real problem — multi-step reasoning, tool use, memory, error handling. GitHub repo |

**Key concepts to nail:**
- [ ] How LLMs are trained (pre-training, fine-tuning, RLHF)
- [ ] Tokenization, context windows, temperature, sampling strategies
- [ ] Embeddings: what they are, how they're generated, similarity metrics
- [ ] RAG: chunking, retrieval, re-ranking, generation, evaluation
- [ ] Agents: ReAct pattern, tool use, planning, memory
- [ ] Prompt engineering: system prompts, few-shot, chain-of-thought
- [ ] Evaluation: how to measure LLM application quality

**Reading:**
- [Anthropic Research Blog](https://www.anthropic.com/research)
- [Anthropic Prompt Engineering Guide](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview)
- [LLM Powered Autonomous Agents](https://lilianweng.github.io/posts/2023-06-23-agent/) — Lilian Weng
- ["Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks"](https://arxiv.org/abs/2005.11401) paper

---

## Phase 4: Production AI Systems (Weeks 35-42)

**Goal:** Learn to deploy, scale, and monitor AI systems

| Week | Study (50%) | Build (50%) |
|------|------------|-------------|
| 35-36 | [Docker fundamentals](https://docs.docker.com/get-started/) + [FastAPI tutorial](https://fastapi.tiangolo.com/tutorial/) | Containerize Project 5, expose it as a REST API with FastAPI |
| 37-38 | [MLOps Specialization](https://www.coursera.org/specializations/machine-learning-engineering-for-production-mlops) (Coursera) — Courses 1-2: ML pipelines, data validation, model serving | Set up CI/CD with GitHub Actions for one of your projects |
| 39-40 | MLOps Specialization — Courses 3-4: Model monitoring, pipeline automation | Cloud basics: deploy a model to AWS (Lambda + API Gateway) or GCP (Cloud Run) |
| 41-42 | LLM-specific production concerns: rate limiting, caching, cost optimization, guardrails, observability | **Project 6:** Full production AI application — API + LLM integration + monitoring + error handling + CI/CD + cloud deployment. GitHub repo |

**Key concepts to nail:**
- [ ] Docker and containerization
- [ ] API design (REST, async)
- [ ] CI/CD for ML/AI projects
- [ ] Model monitoring and drift detection
- [ ] LLM-specific: token cost management, latency optimization, caching, guardrails
- [ ] Basic cloud deployment (pick one cloud and learn it)

---

## Phase 5: Specialization & Depth (Weeks 43-52)

**Goal:** Go deep in one area, build authority, contribute to the community

| Week | Focus |
|------|-------|
| 43-44 | **Choose your specialization** based on what excited you most. Natural options: Conversational AI, LLM Applications, AI Agents. Read 4-5 foundational papers in that area |
| 45-46 | **Advanced project** in your specialization — something novel, not a tutorial clone. Could be: a multi-agent system, a specialized RAG pipeline for a domain, a fine-tuned model for a specific task |
| 47-48 | **Open-source contribution** — contribute to [LangChain](https://github.com/langchain-ai/langchain), [Hugging Face](https://github.com/huggingface), [Anthropic Cookbook](https://github.com/anthropics/anthropic-cookbook), or another AI project. Start with docs, issues, or small features |
| 49-50 | **Build something people can use** — a demo app, a tool, a library. Deploy it, share it, get feedback |
| 51-52 | **Write about what you've learned** — blog posts, tutorials, or detailed GitHub READMEs. Teaching solidifies understanding and builds visibility |

---

## Weekly Routine (~15 hours/week)

```
Mon-Tue:     Course material — videos + notes (4 hrs)
Wed:         Hands-on exercises from courses (2 hrs)
Thu-Fri:     Project work (5 hrs)
Sat:         Math side-track (2 hrs) + 1 paper/blog (1 hr)
Sun:         Rest
```

---

## GitHub Portfolio at the End

| # | Project | Stack |
|---|---------|-------|
| 1 | ML pipeline (full workflow) | Scikit-learn, Pandas |
| 2 | Deep learning model (CNN or RNN) | PyTorch |
| 3 | Fine-tuned transformer | Hugging Face, PyTorch |
| 4 | RAG document Q&A system | Anthropic API, Vector DB |
| 5 | AI agent with tool use and memory | LangChain, Anthropic API |
| 6 | Production-deployed AI application | FastAPI, Docker, Cloud |

---

## Key Milestones

| Month | You should be able to... |
|-------|--------------------------|
| 2 | Train, evaluate, and compare ML models on real data |
| 5 | Build neural networks in PyTorch, explain transformers |
| 7 | Build LLM apps with RAG, embeddings, and basic agents |
| 9 | Deploy an AI application to production |
| 10 | Have a specialization, 6 projects on GitHub, and open-source contributions |

---

## Resources Index

### Courses (Coursera)
- [Machine Learning Specialization](https://www.coursera.org/specializations/machine-learning-introduction) — Andrew Ng
- [Deep Learning Specialization](https://www.coursera.org/specializations/deep-learning) — DeepLearning.AI
- [Math for Machine Learning Specialization](https://www.coursera.org/specializations/mathematics-machine-learning) — Imperial College London
- [Generative AI with LLMs](https://www.coursera.org/learn/generative-ai-with-llms) — AWS + DeepLearning.AI
- [AI Engineering Specialization](https://www.coursera.org/specializations/ai-engineering) — Coursera
- [MLOps Specialization](https://www.coursera.org/specializations/machine-learning-engineering-for-production-mlops) — DeepLearning.AI

### Free Courses & Tutorials
- [Fast.ai — Practical Deep Learning for Coders](https://course.fast.ai/)
- [Hugging Face NLP Course](https://huggingface.co/learn/nlp-course)
- [Anthropic Courses](https://github.com/anthropics/courses)
- [Anthropic Cookbook](https://github.com/anthropics/anthropic-cookbook)
- [DeepLearning.AI Short Courses](https://www.deeplearning.ai/short-courses/)
- [Kaggle Learn](https://www.kaggle.com/learn)
- [PyTorch Tutorials](https://pytorch.org/tutorials/)
- [FastAPI Tutorial](https://fastapi.tiangolo.com/tutorial/)
- [Docker Getting Started](https://docs.docker.com/get-started/)

### Documentation
- [Anthropic API Docs](https://docs.anthropic.com/en/api/getting-started)
- [Anthropic Prompt Engineering Guide](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview)
- [LangChain Documentation](https://python.langchain.com/docs/get_started/introduction)

### Blogs & Visual Guides
- [Jay Alammar](https://jalammar.github.io/) — visual explanations of ML/DL concepts
- [Lilian Weng](https://lilianweng.github.io/) — in-depth AI research summaries
- [Chris Olah](https://colah.github.io/) — neural network visualizations
- [StatQuest](https://www.youtube.com/@statquest) — statistics made simple
- [3Blue1Brown](https://www.youtube.com/@3blue1brown) — math visualizations

### Key Papers
- ["Attention Is All You Need"](https://arxiv.org/abs/1706.03762) — Vaswani et al.
- ["Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks"](https://arxiv.org/abs/2005.11401) — Lewis et al.

---

> **Note:** This plan is aggressive for 10-20 hours/week. Some phases may take longer than estimated, and that's fine. The phases matter more than the timeline — don't rush through a phase just to stay "on schedule." Understanding compounds.
