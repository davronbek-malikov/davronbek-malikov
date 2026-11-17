# Hi, I'm Davronbek Malikov 👋

**LLM & RAG Engineer · Agentic AI Engineer · ML & Deep Learning Engineer · Computer Vision · PhD**
📍 Seoul, South Korea &nbsp;|&nbsp; 📧 davronbekmalikov96@gmail.com

[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=flat&logo=vercel&logoColor=white)](https://davronbek-portfolio.vercel.app)
[![CV](https://img.shields.io/badge/Download_CV-4285F4?style=flat&logo=googledrive&logoColor=white)](https://davronbek-portfolio.vercel.app/cv.pdf)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/davronbek-malikov)
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat&logo=gmail&logoColor=white)](mailto:davronbekmalikov96@gmail.com)

---

## 🧑‍💻 About Me

AI engineer with a **PhD in AI Convergence Engineering** and **5 first-author publications**, working across the full stack — **classical machine learning, deep learning, computer vision and LLM systems**. I take models from data to production: data pipelines, feature engineering, training and tuning, explainability, evaluation, deployment and monitoring.

- 🧠 **LLM & post-training:** SFT, LoRA/QLoRA, DPO, RLHF (reward modeling, PPO, RLOO), quantization, local serving (vLLM, Ollama, llama.cpp)
- 🔎 **RAG:** hybrid search (dense + BM25, RRF), cross-encoder reranking, GraphRAG, permission-aware retrieval, cited answers — pgvector, Qdrant
- 🤖 **Agentic AI:** LangGraph, LangChain, multi-agent systems, human-in-the-loop, MCP, A2A
- 📈 **Evaluation & observability:** LangSmith, Arize Phoenix, OpenTelemetry/Jaeger, Ragas, DeepEval, LLM-as-a-Judge
- 📊 **Machine learning:** ensembles and stacking, AutoML, Optuna, SHAP, clustering, leakage-safe validation
- 🔥 **Deep learning & computer vision:** PyTorch, TensorFlow/Keras, Transformers from scratch, CNNs, detection (YOLO), segmentation, OpenCV
- 🚀 **MLOps:** MLflow, Weights & Biases, Docker, GitHub Actions, FastAPI serving, ONNX/TensorRT
- 🌍 **Languages:** English · Uzbek · Turkish · Russian · Korean

---

## 💼 Current Role

**AI Engineer & Team Lead @ TripleH** *(Dec 2025 – Present)*
Leading the AI engineering team building production autonomous agent systems for enterprise clients: multi-agent orchestration, legal research, meeting intelligence and per-employee AI assistants — running fully on-premise on open-weight LLMs.

---

## 🚀 Featured Projects

### 🤖 LLM, RAG & Agentic Systems

#### [ERA Academy](https://github.com/malikov-davronbek/ERA/tree/phase-1-foundation) — AI EdTech platform · [🟢 Live](https://era-academy.vercel.app)
One provider-agnostic AI agent engine behind three role-scoped assistants (Student Tutor, Teacher Assistant, Admin Assistant).
- Claude, OpenAI and local Ollama adapters with SSE streaming, usage tracking, and cost and rate limits
- **Permission-aware RAG** on pgvector: access rules run inside the retrieval SQL query; answers cite their sources
- Prompt-injection defense · **206 automated tests**, all passing

`Next.js 15` `TypeScript` `Prisma` `PostgreSQL + pgvector` `Claude API` `Ollama`

#### [Touchline](https://github.com/davronbek-malikov/touchline) — AI scouting copilot for football
Describe the player you need; get a ranked shortlist and a cited scouting report.
- Claude agent on **LangGraph** over 7 schema-validated tools — the model never writes SQL
- Human-in-the-loop shortlist approval with persisted checkpoints
- **Hybrid RAG** (dense + BM25, RRF) in Qdrant with citations; DuckDB warehouse of 50,149 players + StatsBomb event data
- Every run traced in **LangSmith**; 120-question golden set run as experiments; 102 automated tests

`Claude API` `LangGraph` `LangSmith` `Qdrant` `DuckDB` `FastAPI` `Next.js`

#### [TeachHelp](https://github.com/davronbek-malikov/Post_Training) — post-training an LLM end to end · [🟢 Live](https://teach-help.vercel.app)
Qwen2.5 base → SFT → DPO → RLHF → deployment, with 14 models measured on the same 68-question held-out test.
- SFT took Qwen2.5-1.5B from **15/68 to 44/68**
- DPO implemented from scratch; v1's length bias diagnosed and fixed in v2 (44/68, all harmful and cheating requests refused)
- RLHF with Bradley–Terry reward models and PPO/RLOO across 4 judges, with reward-hacking checks

`PyTorch` `Transformers` `PEFT` `LoRA/QLoRA` `DPO` `PPO/RLOO` `Kaggle`

#### [TACTIQ](https://github.com/davronbek-malikov/TACTIQ) — evidence-first football intelligence *(in development)*
Ask football questions; get evidence, not guesses. Phase 1: a hand-written indexing pipeline (load → metadata → clean → token-based chunking → embeddings → Qdrant) with idempotent re-ingestion and tests for every step.

`Python` `Qdrant` `Sentence Transformers` `pytest`

#### Portiq — multi-agent job hub · [🟢 Live preview](https://portiq-gamma.vercel.app)
A LangGraph orchestrator routes 11 agents over Kafka and A2A, with a Judge agent, pgvector job matching, mock interviews in 4 languages, and OpenTelemetry + Jaeger tracing.

`LangGraph` `Kafka` `A2A` `FastAPI` `PostgreSQL + pgvector` `OpenTelemetry`

### 📊 Machine Learning & Deep Learning

#### [LLM from Scratch](https://github.com/davronbek-malikov/LLM_Model) — GPT-style Transformer in PyTorch *(pretraining in progress)*
- Decoder-only Transformer written from first principles: multi-head causal self-attention, MLP blocks, weight tying — verified with shape, random-init loss, overfit-one-batch and causality tests
- Full pretraining pipeline: cleaning, filtering, MinHash near-duplicate detection, BPE tokenizer, warmup + cosine LR, gradient accumulation, bf16/fp16 mixed precision, resumable checkpoints, top-k/top-p sampling

`PyTorch` `Transformers` `BPE` `Mixed Precision`

#### [Soccer Player Salary Predictor](https://github.com/davronbek-malikov/soccer-xG-salary_prediction) — supervised ML · [🟢 Live](https://soccer-xg-salary-prediction.onrender.com)
Leakage-safe pipeline: 21 engineered features → gradient boosting → stacking and voting ensembles, Optuna tuning, SHAP explanations. Linked to an SCIE paper (17% accuracy gain).

`XGBoost` `LightGBM` `Optuna` `SHAP` `Gradio`

#### [TacticalDNA](https://github.com/davronbek-malikov/tactical-dna) — unsupervised ML · [🟢 Live](https://soccer-player-clustering.onrender.com)
Clusters 6,314 player-seasons into six playing archetypes. A blind stat line — 25 goals, 15 assists, no name attached — matched prime Messi's 2019/20 season at **98% cosine similarity**.

`Scikit-learn` `KMeans` `Streamlit` `Plotly`

### 🛍️ Full-Stack AI Products

| Product | What it does | Live |
|---|---|---|
| **Palov** | Halal Uzbek food ordering in Korea; RAG chatbot over the menu | [palov.app](https://www.palov.app/) |
| **Hamyon** | Personal finance manager; RAG chatbot over your transactions | [hamyon](https://hamyon-six.vercel.app/) |
| **Kotib** | AI personal secretary; agent pipeline with Graph RAG and memory | [kotib](https://kotib-rouge.vercel.app/) |

---

## 📄 Publications *(5 first-author)*

1. **Predicting Soccer Player Salaries with Both Traditional and Automated Machine Learning Approaches** — *Applied Sciences (SCIE), 2025* · [DOI →](https://doi.org/10.3390/app15148108)
2. **Beyond xG: A Dual Prediction Model for Analyzing Player Performance Through Expected and Actual Goals in European Soccer Leagues** — *Applied Sciences (SCIE), 2024* · [DOI →](https://doi.org/10.3390/app142210390)
3. **Comparative Evaluation of Machine Learning Models for Predicting Soccer Injury Types** — *KSCIE, 2024* · [Link →](https://www.kci.go.kr/kciportal/ci/sereArticleSearch/ciSereArtiView.kci?sereArticleSearchBean.artiId=ART003072688)
4. **The Application of Machine Learning on the Injury Prediction of Soccer Players** — *ISE@APSEC, 2022* · [PDF →](https://ceur-ws.org/Vol-3362/ISE2022_short02_Malikov_Application.pdf)
5. **On the Construction and Properties of Lattice-Group Structure in Cartesian Product Spaces** — *Journal of Computer Science, 2020* · [DOI →](https://doi.org/10.3844/jcssp.2020.402.421)

---

## 🎓 Education

| Degree | Institution | Year |
|--------|-------------|------|
| **PhD in AI Convergence Engineering** | Gyeongsang National University, South Korea | 2020 – 2025 |
| **Master of Informatics** | Gyeongsang National University, South Korea | 2018 – 2020 |
| **Bachelor of Mathematics** | Fergana State University, Uzbekistan | 2014 – 2018 |

---

## 🛠️ Tech Stack

**LLM, RAG & Agents**
![Claude](https://img.shields.io/badge/Claude_API-D97757?style=flat&logo=anthropic&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat&logo=langchain&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat&logo=langchain&logoColor=white)
![LangSmith](https://img.shields.io/badge/LangSmith-1C3C3C?style=flat&logo=langchain&logoColor=white)
![Hugging Face](https://img.shields.io/badge/HuggingFace-FFD21F?style=flat&logo=huggingface&logoColor=black)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat&logo=ollama&logoColor=white)
![vLLM](https://img.shields.io/badge/vLLM-30A2FF?style=flat&logoColor=white)
![Qdrant](https://img.shields.io/badge/Qdrant-DC244C?style=flat&logoColor=white)
![pgvector](https://img.shields.io/badge/pgvector-4169E1?style=flat&logo=postgresql&logoColor=white)

**Post-Training & Evaluation**
![LoRA](https://img.shields.io/badge/LoRA%2FQLoRA-FF6B35?style=flat&logoColor=white)
![DPO](https://img.shields.io/badge/DPO%2FRLHF-8B5CF6?style=flat&logoColor=white)
![Arize Phoenix](https://img.shields.io/badge/Arize_Phoenix-6C2BD9?style=flat&logoColor=white)
![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry-000000?style=flat&logo=opentelemetry&logoColor=white)

**ML, Deep Learning & Computer Vision**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat&logo=tensorflow&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-189FDD?style=flat&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat&logo=opencv&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white)

**MLOps, Backend & Deployment**
![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=flat&logo=mlflow&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat&logo=redis&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat&logo=apachekafka&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat&logo=nextdotjs&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=flat&logo=vercel&logoColor=white)

---

## 📬 Contact

- 🌐 **Portfolio:** [davronbek-portfolio.vercel.app](https://davronbek-portfolio.vercel.app)
- 📄 **CV:** [Download CV](https://davronbek-portfolio.vercel.app/cv.pdf)
- 💼 **LinkedIn:** [linkedin.com/in/davronbek-malikov](https://www.linkedin.com/in/davronbek-malikov)
- 📧 **Email:** [davronbekmalikov96@gmail.com](mailto:davronbekmalikov96@gmail.com)
