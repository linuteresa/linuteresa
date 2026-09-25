<h1 align="center">Hi, I am Linu 👋</h1>
<h3 align="center">I build ML systems and the evals that keep them honest</h3>

<p align="center">
  <a href="https://linuteresa.github.io/portfolio/">Portfolio</a> ·
  <a href="mailto:lteresa@umd.edu">lteresa@umd.edu</a> ·
  <a href="https://www.linkedin.com/in/linuteresa/">LinkedIn</a>
</p>

---

Retrieval, agents, and distributed data, with a habit of building the measurement before trusting the
system. Most of what I learn ends up here as something runnable.

> ** Hot take - Data cleaning is 80% of the job and 100% of what nobody puts in the job description.**

### Currently experimenting with

**[Reinforcement learing and agent reward modeling](https://github.com/linuteresa/llm-alignment-lab)** · PyTorch, HuggingFace, SmolLM2
Working through the post-training stack by implementing it from scratch rather than calling
`trainer.train()`: supervised fine-tuning, reward modeling, PPO, DPO and GRPO on a 135M model, plus a
small GPT-2 and a BPE tokenizer. The part I find most interesting is the reward-hacking probe, which
optimizes against a learned proxy reward while scoring on a held-out gold metric and watches the two come
apart: gold quality collapses to 0.03 under a weak KL penalty, against 0.98 under DPO.

### Selected work

**[biomed-rag](https://github.com/linuteresa/biomed-rag)** · Python, Pinecone, LlamaIndex, HuggingFace
Retrieval over biomedical literature with cited sources. Hybrid dense and BM25 retrieval, reranking, and a
hand-labeled 56-query benchmark split easy and hard, because a single average would have hidden that
Recall@10 falls from 1.00 to 0.50 on the queries that actually matter. Grounding and citation checks run
offline in CI, so a regression blocks a merge instead of reaching a user.

**[bayes-execution-engine](https://github.com/linuteresa/bayes-execution-engine)** · Python, LangGraph, MCP, pgmpy
Multi-agent orchestration on a deterministic plan-and-execute schedule, agents calling tools over MCP.
Bayesian graphical models resolve conflicting agent outputs into one answer carrying an uncertainty
estimate, instead of retrying until the agents happen to agree.

**[big-data-analytics](https://github.com/linuteresa/big-data-analytics)** · Spark, Airflow, Dask, PostgreSQL, MongoDB, Neo4j, Redis
Batch and stream processing with DAG orchestration, running comparable workloads across relational,
document, graph and key-value stores to see where each access pattern actually pays.

**[peekaboo-webapp](https://github.com/linuteresa/peekaboo-webapp)** · Vanilla JS, Tesseract.js, Ollama
Learning app for preschoolers with OCR and an AI tutor running Gemma3 locally through Ollama. No
framework, hand-rolled state-driven rendering, six-tier adaptive progression.

### Tech Stack

Python · Java · SQL · PyTorch · scikit-learn · pandas · NumPy · HuggingFace · LangGraph · MCP · Pinecone ·
Spark · Airflow · Dask · PostgreSQL · MongoDB · Redis · Docker · Terraform · AWS · Azure · Git
