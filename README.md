<div align="center">

# 🧠 AI Engineering Interview Prep Guide

**A structured, hands-on roadmap for landing AI/ML Engineer, Applied Scientist, and LLM Engineer roles.**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Stars](https://img.shields.io/github/stars/your-username/ai-engineering-interview-guide?style=social)](https://github.com/your-username/ai-engineering-interview-guide)
[![Last Commit](https://img.shields.io/github/last-commit/your-username/ai-engineering-interview-guide)](https://github.com/your-username/ai-engineering-interview-guide/commits/main)

[Study Plan](#-study-plan) • [Topics](#-core-topics) • [Question Bank](#-question-bank) • [Coding](#-coding-challenges) • [System Design](#-ml--llm-system-design) • [Papers](#-must-read-papers) • [Contributing](#-contributing)

</div>

---

## 📖 About

AI engineering interviews are unusual: they blend **software engineering**, **ML theory**, **applied LLM work**, and **system design** in a single loop. Most resources cover only one of these.

This repo is a single place to prepare for all of them. It contains curated notes, worked solutions, from-scratch implementations, mock interview questions, and reading lists, built around what interviewers actually ask.

**This guide is for you if you are:**

- Preparing for ML Engineer, AI Engineer, Applied Scientist, Research Engineer, or LLM/GenAI Engineer interviews
- Transitioning from software engineering, data science, or academia into applied AI
- A researcher who wants to sharpen production, systems, and coding skills
- An engineer who wants to go deeper than "call the API and prompt it"

> **Note:** Every topic is written to be *explainable out loud*. Knowing something and articulating it clearly under pressure are different skills, and this repo trains both.

---

## 🗺 Table of Contents

- [Interview Landscape](#-interview-landscape)
- [Study Plan](#-study-plan)
- [Repository Structure](#-repository-structure)
- [Core Topics](#-core-topics)
- [Question Bank](#-question-bank)
- [Coding Challenges](#-coding-challenges)
- [ML & LLM System Design](#-ml--llm-system-design)
- [Must-Read Papers](#-must-read-papers)
- [Books, Courses & Resources](#-books-courses--resources)
- [Behavioral & Communication](#-behavioral--communication)
- [Progress Tracker](#-progress-tracker)
- [Getting Started](#-getting-started)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🎯 Interview Landscape

A typical AI engineering loop has 4–6 rounds. Emphasis varies by company and role.

| Round | What's Tested | Where to Prepare |
|---|---|---|
| **Coding** | Data structures, algorithms, Python fluency | [`/coding`](./coding) |
| **ML Fundamentals** | Optimization, bias/variance, metrics, probability | [`/topics/01-ml-fundamentals`](./topics/01-ml-fundamentals) |
| **Deep Learning / LLM Depth** | Transformers, training dynamics, fine-tuning, alignment | [`/topics/02-deep-learning`](./topics/02-deep-learning), [`/topics/03-llms`](./topics/03-llms) |
| **Applied / Take-Home** | RAG, agents, evals, data pipelines | [`/topics/05-rag-and-agents`](./topics/05-rag-and-agents) |
| **ML System Design** | End-to-end architecture, scaling, trade-offs | [`/system-design`](./system-design) |
| **Research Discussion** | Paper deep-dives, experimental design, critique | [`/papers`](./papers) |
| **Behavioral** | Ownership, ambiguity, collaboration, impact | [`/behavioral`](./behavioral) |

---

## 📅 Study Plan

Pick the track that matches your timeline. Each week links to the relevant folders.

### 🚀 8-Week Standard Plan

| Week | Focus | Deliverables |
|---|---|---|
| **1** | Math & ML fundamentals refresh | Derive gradient descent, logistic regression, and bias–variance by hand |
| **2** | Classical ML + evaluation | Implement k-means, decision tree, and a metrics suite from scratch |
| **3** | Deep learning foundations | Build an MLP + backprop in NumPy; implement a training loop in PyTorch |
| **4** | Transformers & LLM internals | Implement multi-head attention, a small GPT, and KV-caching |
| **5** | Fine-tuning & alignment | LoRA fine-tune a small model; compare SFT vs. DPO |
| **6** | RAG, agents & evals | Build a RAG pipeline with a proper eval harness |
| **7** | Inference, serving & MLOps | Profile latency/throughput; explore quantization and batching |
| **8** | System design + mock interviews | Complete 4+ system design mocks and 3+ full mock loops |

### ⚡ 2-Week Sprint (Already Experienced)

1. **Days 1–3:** Skim [ML fundamentals](./topics/01-ml-fundamentals) and [LLM internals](./topics/03-llms); drill the [Question Bank](#-question-bank)
2. **Days 4–6:** Coding practice (Medium-level) + implement attention and a training loop from scratch
3. **Days 7–10:** RAG/agents/evals + inference optimization
4. **Days 11–13:** System design mocks (2 per day)
5. **Day 14:** Behavioral stories + rest

### 🔬 Research → Industry Track

If you come from academia, prioritize what's typically *under*-practiced:

- Production concerns: latency, cost, monitoring, data drift, rollout strategies
- Software engineering hygiene: testing, code review norms, API design
- Communicating research impact in business terms
- Timed coding under interview conditions

---

## 📁 Repository Structure

```
ai-engineering-interview-guide/
│
├── README.md
├── CONTRIBUTING.md
├── LICENSE
│
├── topics/                        # Concept notes (theory + interview angles)
│   ├── 01-ml-fundamentals/
│   ├── 02-deep-learning/
│   ├── 03-llms/
│   ├── 04-fine-tuning-and-alignment/
│   ├── 05-rag-and-agents/
│   ├── 06-evaluation/
│   ├── 07-inference-and-serving/
│   ├── 08-mlops-and-data/
│   └── 09-math-and-stats/
│
├── questions/                     # Question bank with model answers
│   ├── ml-fundamentals.md
│   ├── deep-learning.md
│   ├── llms.md
│   ├── rag-and-agents.md
│   └── system-design.md
│
├── coding/                        # Coding challenges & from-scratch implementations
│   ├── algorithms/
│   ├── ml-from-scratch/
│   ├── pytorch/
│   └── llm-from-scratch/
│
├── system-design/                 # Case studies + a reusable framework
│   ├── framework.md
│   └── case-studies/
│
├── papers/                        # Annotated reading list + summaries
├── behavioral/                    # STAR stories, templates, leadership principles
├── cheatsheets/                   # One-page references (formulas, shapes, complexity)
├── mock-interviews/               # Scripts, rubrics, self-evaluation forms
└── assets/                        # Diagrams and images
```

---

## 📚 Core Topics

Each topic folder contains: **concept summary → common interview questions → pitfalls → follow-up probes → references.**

### 1. ML Fundamentals
- Supervised vs. unsupervised vs. self-supervised learning
- Bias–variance tradeoff, regularization (L1/L2, dropout, early stopping)
- Loss functions and their probabilistic interpretations (MLE/MAP)
- Optimization: SGD, momentum, Adam/AdamW, learning-rate schedules, warmup
- Evaluation metrics: precision/recall/F1, ROC-AUC vs. PR-AUC, calibration, ranking metrics (NDCG, MRR)
- Data leakage, distribution shift, class imbalance, cross-validation strategies
- Tree-based models, gradient boosting, and when they beat deep learning

### 2. Deep Learning
- Backpropagation and the computational graph
- Initialization (Xavier/He), normalization (BatchNorm, LayerNorm, RMSNorm)
- Activation functions (ReLU, GELU, SwiGLU) and vanishing/exploding gradients
- CNNs, RNNs/LSTMs, and why attention displaced them for many tasks
- Mixed precision (FP16/BF16/FP8), gradient accumulation, gradient checkpointing
- Distributed training: data / tensor / pipeline parallelism, ZeRO, FSDP

### 3. Large Language Models
- Tokenization (BPE, WordPiece, SentencePiece) and its downstream effects
- Transformer architecture: self-attention, multi-head/grouped-query/multi-query attention
- Positional encodings: sinusoidal, learned, RoPE, ALiBi; long-context extension
- Decoder-only vs. encoder-decoder; pretraining objectives
- Scaling laws and compute-optimal training
- Mixture-of-Experts: routing, load balancing, trade-offs
- Decoding: greedy, beam, top-k/top-p, temperature, speculative decoding
- Emergent behavior, in-context learning, chain-of-thought and reasoning models

### 4. Fine-Tuning & Alignment
- Full fine-tuning vs. parameter-efficient methods (LoRA, QLoRA, adapters, prefix/prompt tuning)
- Supervised fine-tuning: data curation, formatting, loss masking
- Preference optimization: RLHF (PPO), DPO and variants, RLAIF, GRPO
- Reward modeling, reward hacking, and over-optimization
- Catastrophic forgetting and mitigation
- Distillation and synthetic data generation

### 5. RAG & Agents
- Chunking strategies, embeddings, vector indexes (HNSW, IVF, PQ)
- Hybrid search (BM25 + dense), re-ranking, query rewriting
- Failure modes: retrieval misses, context stuffing, lost-in-the-middle, hallucination
- Tool use and function calling; planning, memory, and reflection patterns
- Multi-agent orchestration, reliability, guardrails, and prompt-injection defense
- When *not* to use RAG or agents

### 6. Evaluation
- Offline vs. online evaluation; golden sets and regression suites
- LLM-as-judge: biases, calibration, agreement with human raters
- Benchmarks and their limits (contamination, saturation, Goodhart's law)
- RAG-specific metrics: context precision/recall, faithfulness, answer relevance
- A/B testing, guardrail metrics, and statistical significance for ML systems
- Red-teaming and safety evaluation

### 7. Inference & Serving
- Prefill vs. decode; memory-bound vs. compute-bound regimes
- KV cache, PagedAttention, continuous batching, prefix caching
- Quantization (INT8/INT4, GPTQ, AWQ), pruning, distillation
- FlashAttention and kernel-level optimizations
- Latency/throughput/cost trade-offs; autoscaling and GPU utilization
- Model routing, caching, and fallback strategies

### 8. MLOps & Data
- Feature stores, data versioning, and lineage
- Experiment tracking and reproducibility
- CI/CD for ML, canary/shadow deployments, rollback
- Monitoring: drift detection, quality regressions, cost tracking
- Data quality, labeling pipelines, and privacy/compliance basics

### 9. Math & Statistics
- Linear algebra: SVD, eigendecomposition, matrix calculus
- Probability: Bayes, common distributions, expectation/variance, KL divergence, entropy
- Statistics: hypothesis testing, confidence intervals, bootstrap, multiple comparisons
- Information theory and its role in loss functions and compression

---

## ❓ Question Bank

Questions are tagged by **difficulty** (🟢 Easy · 🟡 Medium · 🔴 Hard) and **type** (Concept, Derivation, Debugging, Design).

<details>
<summary><b>Example: ML Fundamentals</b></summary>

- 🟢 Explain the bias–variance tradeoff. How does it change as model capacity grows?
- 🟡 Why does L1 regularization induce sparsity while L2 does not?
- 🟡 Your model has 99% accuracy on a fraud dataset. Is that good? What would you check?
- 🔴 Derive the gradient of the cross-entropy loss with respect to the logits under softmax.

</details>

<details>
<summary><b>Example: Transformers & LLMs</b></summary>

- 🟢 Why do we scale dot-product attention by √d<sub>k</sub>?
- 🟡 Explain the KV cache. What does it save, and what does it cost in memory?
- 🟡 Compare multi-head, multi-query, and grouped-query attention.
- 🔴 A model's loss spikes midway through pretraining. How do you diagnose and respond?
- 🔴 Why does RoPE generalize better to longer contexts than learned absolute embeddings, and where does it still break down?

</details>

<details>
<summary><b>Example: Fine-Tuning & Alignment</b></summary>

- 🟡 When would you choose LoRA over full fine-tuning? What are the limits of LoRA?
- 🟡 Explain the DPO objective. What does it remove compared to RLHF with PPO?
- 🔴 Your reward model scores keep rising but human preference ratings drop. What's happening?

</details>

<details>
<summary><b>Example: RAG & Agents</b></summary>

- 🟢 What are the trade-offs between small and large chunk sizes?
- 🟡 Your RAG system answers confidently but incorrectly. Walk through how you'd debug it.
- 🔴 Design an evaluation strategy for an agent that takes multi-step actions with side effects.

</details>

<details>
<summary><b>Example: Inference & Systems</b></summary>

- 🟡 Why is decoding memory-bandwidth-bound while prefill is compute-bound?
- 🟡 How does continuous batching improve GPU utilization over static batching?
- 🔴 You need to cut serving cost by 50% without hurting quality. What levers do you pull, and in what order?

</details>

👉 Full question sets with model answers live in [`/questions`](./questions).

### Answer Format

Model answers follow a consistent structure so you can practice delivering them:

1. **One-line answer** (the headline)
2. **Intuition** (why it's true)
3. **Details / math** (when relevant)
4. **Trade-offs and edge cases**
5. **Likely follow-ups**

---

## 💻 Coding Challenges

### Algorithms & Data Structures
Standard interview fare, curated for relevance to ML roles: arrays/strings, hash maps, heaps, graphs, DP, sliding window, and binary search. Solutions are in Python with complexity analysis.

### ML From Scratch (NumPy)
- [ ] Linear & logistic regression (with gradient descent)
- [ ] k-means and k-NN
- [ ] Decision tree and random forest
- [ ] Naive Bayes
- [ ] PCA via SVD
- [ ] MLP with manual backpropagation
- [ ] Evaluation metrics (precision, recall, AUC, NDCG)

### PyTorch
- [ ] Custom `Dataset`, `DataLoader`, and training loop with checkpointing
- [ ] Custom `autograd.Function` and a hand-written layer
- [ ] Mixed-precision training and gradient accumulation
- [ ] Debugging a broken training run (exploding loss, shape bugs, silent NaNs)

### LLMs From Scratch
- [ ] Scaled dot-product and multi-head attention
- [ ] Causal masking and a minimal GPT
- [ ] BPE tokenizer
- [ ] KV cache for autoregressive decoding
- [ ] Sampling: top-k, top-p, temperature
- [ ] LoRA layer from scratch
- [ ] Simple RAG pipeline with a retriever, re-ranker, and eval harness

> 💡 **Tip:** Practice writing these on a blank editor without autocomplete or documentation. Interviewers often ask you to implement attention or a metric live.

---

## 🏗 ML & LLM System Design

A repeatable framework for open-ended design questions:

```
1. Clarify        →  Goals, users, scale, latency, budget, constraints
2. Metrics        →  Business metric, ML metric, guardrails
3. Data           →  Sources, labeling, quality, privacy, freshness
4. Baseline       →  Simplest thing that could work
5. Modeling       →  Architecture choices, training, fine-tuning vs. prompting
6. Serving        →  Batch vs. real-time, caching, routing, scaling
7. Evaluation     →  Offline, online, human review, regression tests
8. Monitoring     →  Drift, quality, cost, safety, feedback loops
9. Iteration      →  Failure analysis, next experiments, trade-offs
```

### Case Studies

| Case Study | Key Concepts |
|---|---|
| Enterprise document Q&A (RAG at scale) | Chunking, hybrid retrieval, access control, evals |
| Customer-support copilot | Latency, guardrails, human-in-the-loop, escalation |
| Code-completion assistant | Low-latency serving, context construction, acceptance-rate metrics |
| Recommendation / ranking system | Two-tower retrieval, re-ranking, cold start, feedback loops |
| Multi-step research agent | Planning, tool reliability, cost control, eval of trajectories |
| Content-moderation pipeline | Precision/recall trade-offs, adversarial inputs, human review |
| LLM gateway / routing layer | Model selection, caching, fallbacks, rate limiting |
| Fraud / anomaly detection | Imbalance, drift, delayed labels, explainability |

Each case study includes a **reference architecture diagram**, **trade-off table**, **failure modes**, and **follow-up questions**.

---

## 📄 Must-Read Papers

Annotated summaries live in [`/papers`](./papers), each with: *problem → key idea → why it mattered → common interview angles.*

| Area | Paper |
|---|---|
| **Foundations** | *Attention Is All You Need* (Vaswani et al., 2017) |
| | *BERT* (Devlin et al., 2018) |
| | *Language Models are Few-Shot Learners* (GPT-3, Brown et al., 2020) |
| **Scaling** | *Scaling Laws for Neural Language Models* (Kaplan et al., 2020) |
| | *Training Compute-Optimal LLMs* (Chinchilla, Hoffmann et al., 2022) |
| **Architecture** | *RoFormer / RoPE* (Su et al., 2021) |
| | *Switch Transformers* (Fedus et al., 2021) |
| | *GQA: Grouped-Query Attention* (Ainslie et al., 2023) |
| **Efficiency** | *FlashAttention* (Dao et al., 2022) |
| | *Efficient Memory Management for LLM Serving with PagedAttention* (Kwon et al., 2023) |
| | *Fast Inference via Speculative Decoding* (Leviathan et al., 2022) |
| **Fine-Tuning** | *LoRA* (Hu et al., 2021) |
| | *QLoRA* (Dettmers et al., 2023) |
| **Alignment** | *InstructGPT* (Ouyang et al., 2022) |
| | *Direct Preference Optimization* (Rafailov et al., 2023) |
| | *Constitutional AI* (Bai et al., 2022) |
| **Reasoning** | *Chain-of-Thought Prompting* (Wei et al., 2022) |
| | *Self-Consistency* (Wang et al., 2022) |
| | *DeepSeekMath* (GRPO) and *DeepSeek-R1* |
| **RAG & Agents** | *Retrieval-Augmented Generation* (Lewis et al., 2020) |
| | *ReAct* (Yao et al., 2022) |
| | *Toolformer* (Schick et al., 2023) |
| | *Reflexion* (Shinn et al., 2023) |

**How to read a paper for interviews:** be able to state the problem, the core idea, the main result, one limitation, and one follow-up experiment, all in under two minutes.

---

## 🎓 Books, Courses & Resources

### Books
- *AI Engineering*: Chip Huyen
- *Designing Machine Learning Systems*: Chip Huyen
- *Deep Learning*: Goodfellow, Bengio, Courville
- *Deep Learning: Foundations and Concepts*: Bishop & Bishop
- *Probabilistic Machine Learning*: Kevin Murphy
- *Speech and Language Processing*: Jurafsky & Martin

### Courses & Lectures
- Stanford **CS224N** (NLP with Deep Learning), **CS229** (ML), **CS336** (Language Modeling from Scratch)
- Andrej Karpathy: *Neural Networks: Zero to Hero*
- Hugging Face **LLM / NLP Course**
- fast.ai **Practical Deep Learning**

### Blogs & Explainers
- Jay Alammar: *The Illustrated Transformer*
- Lilian Weng's blog
- Sebastian Raschka's *Ahead of AI*
- Eugene Yan's writing on applied ML systems

### Practice Platforms
- LeetCode / NeetCode (algorithms)
- Kaggle (applied ML)
- Hugging Face Hub (models, datasets, Spaces)

> Contributions to this list are welcome. Please prefer resources that are free, high quality, and regularly maintained.

---

## 🗣 Behavioral & Communication

Technical strength gets you to the final round; communication often decides it.

- **STAR+ framework:** Situation → Task → Action → Result → *what you'd do differently*
- Prepare **6–8 stories** covering: technical conflict, ambiguity, failure, mentoring, cross-functional influence, tight deadline, and a project you're proud of
- Practice explaining a complex ML concept to (a) an executive, (b) a junior engineer, and (c) a peer researcher
- Prepare crisp answers to: *Why this role? Why this company? What's your biggest technical bias?*
- Templates and worked examples live in [`/behavioral`](./behavioral)

---

## ✅ Progress Tracker

Fork the repo and check things off as you go.

- [ ] Completed ML fundamentals notes and question set
- [ ] Implemented attention and a mini-GPT from scratch
- [ ] Fine-tuned a model with LoRA and evaluated it
- [ ] Built a RAG pipeline with an eval harness
- [ ] Completed 20+ coding problems (Medium or above)
- [ ] Completed 6+ system design mocks
- [ ] Read and summarized 15+ papers
- [ ] Wrote 6+ behavioral stories
- [ ] Did 3+ full mock interviews with a peer

---

## ⚙️ Getting Started

```bash
# Clone the repository
git clone https://github.com/your-username/ai-engineering-interview-guide.git
cd ai-engineering-interview-guide

# Create an environment
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate

# Install dependencies for the coding notebooks
pip install -r requirements.txt

# Run the tests for the from-scratch implementations
pytest coding/
```

**Suggested workflow**

1. Read a topic note, then close it and explain the concept aloud
2. Attempt the matching questions *before* reading the model answers
3. Implement the related code from scratch, then compare with the reference
4. Log gaps in a personal "weak spots" file and revisit weekly

---

## 🤝 Contributing

Contributions are what make this guide better. You can help by:

- 🐛 Fixing errors or outdated information
- ➕ Adding questions, model answers, or new case studies
- 🧪 Adding tested from-scratch implementations
- 📝 Sharing interview experiences (anonymized, no confidential or company-proprietary material)
- 🌍 Translating content

Please read [CONTRIBUTING.md](CONTRIBUTING.md) before opening a pull request.

**Ground rules**

- Cite sources for factual claims and paper summaries
- Keep answers concise and interview-oriented
- Do **not** submit leaked or proprietary interview questions or NDA-covered material

---

## 🙏 Acknowledgements

Thanks to the ML community, open courseware authors, and everyone who has contributed questions, fixes, and feedback.

---

## 📜 License

Distributed under the MIT License. See [`LICENSE`](LICENSE) for details.

---

<div align="center">

**If this guide helped you, consider giving it a ⭐ and sharing it with someone preparing for their next interview.**

Good luck, you've got this. 🚀

</div>
