# RAG Evaluation Lab

A systematic exploration of RAG (Retrieval-Augmented Generation) evaluation methods using real academic papers. This project demonstrates common RAG failure modes and implements solutions, with full experimental results for reproducibility.

## 🎯 Project Goals

1. **Recreate production RAG challenges** in a controlled, shareable environment
2. **Systematically test solutions** with measurable improvements
3. **Document learnings** for the community through blog posts and code
4. **Build evaluation frameworks** that others can adapt

## 📚 Dataset

This project uses **30+ research papers** on RAG and LLM evaluation from ArXiv:
- Foundational RAG papers (RAG, Self-RAG, CRAG, etc.)
- Evaluation frameworks (RAGAS, ARES, LLM-as-Judge)
- Retrieval methods (DPR, HyDE, etc.)
- Recent advances (Graph RAG, etc.)

Papers are **not** included in this repository. Download them using the provided script (see Setup).

## 🚀 Quick Start

### Prerequisites

- Python 3.9+
- Git
- (Optional) Ollama for local LLM inference
- (Optional) OpenAI API key for faster inference

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/yourusername/rag-eval-lab.git
cd rag-eval-lab

# 2. Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Download papers (takes ~5 minutes)
python scripts/download_papers.py download

# 5. Set up environment variables (if using OpenAI)
cp .env.example .env
# Edit .env and add your OPENAI_API_KEY
```

### Running Experiments

```bash
# Run baseline RAG
jupyter notebook notebooks/01_basic_rag.ipynb

# TODO: Run improved versions
jupyter notebook notebooks/02_improved_rag.ipynb

# TODO: See evaluation results
jupyter notebook notebooks/03_evaluation.ipynb
```


## 🧪 Experiments

### Baseline RAG
- Basic vector similarity search
- Small chunk size (512 tokens)
- Top-3 retrieval
- **Results**: ~60% accuracy on eval set

### Improved V1: Query Rewriting
- LLM-based query reformulation
- Better semantic matching
- **Results**: ~75% accuracy (+15%)

### Improved V2: Enhanced Retrieval
- Larger chunks (1024 tokens)
- Higher top-k (10 chunks)
- Cross-encoder reranking
- **Results**: ~85% accuracy (+10%)

### Improved V3: Structured Prompting
- Clear instruction format
- Citation requirements
- Better consistency
- **Results**: ~90% accuracy (+5%)

Full results and analysis in `results/` directory.

## 🛠️ Project Structure

```
rag-eval-lab/
├── data/
│   ├── raw/              # PDFs (gitignored, download via script)
│   └── processed/        # Embeddings, indexes (gitignored)
├── cache/                # Cached responses (gitignored)
├── results/              # Evaluation results (committed)
├── scripts/              # Utility scripts
│   └── download_papers.py
├── notebooks/            # Jupyter notebooks
├── src/                  # Reusable code
│   ├── evals
│   ├── rag
└── requirements.txt
```


## 🤝 Contributing

Contributions welcome! Areas of interest:
- Additional evaluation questions
- New RAG architectures to test
- Improved evaluation metrics
- Visualization tools

## 📄 License

MIT License - see LICENSE file for details.

## 🙏 Acknowledgments

- Papers from ArXiv (see `scripts/download_papers.py` for full attribution)
- Built with LlamaIndex, OpenAI, and Streamlit
- Inspired by production RAG challenges at my work


## 📞 Contact

- LinkedIn: [\[My LinkedIn\]](http://www.linkedin.com/in/gowsiyashek)


---

**Note**: This is a research/learning project. The approaches shown here are for educational purposes and should be adapted for production use cases with appropriate safeguards.