# rag-eval-lab
Experiments for deep analysis of RAG and LLM Evals
# rag-eval-lab

Small lab to explore **RAG (Retrieval-Augmented Generation)** and **LLM evals** on real papers, starting with `Evals_Paper.pdf`.

This project currently runs **fully local** for generation (via Ollama) and **local embeddings** (via HuggingFace), so it works even without OpenAI credits.

---

## 1. Prerequisites

- Python 3.10+ installed
- Git
- VS Code (with **Python** and **Jupyter** extensions)
- [Ollama](https://ollama.com/download) installed and running
- (Optional) OpenAI account + API key if you want to use OpenAI models later

---

## 2. Clone and create virtual environment and install dependencies

```bash
git clone <your-repo-url> rag-eval-lab
cd rag-eval-lab

python -m venv .venv

pip install -r requirements.txt