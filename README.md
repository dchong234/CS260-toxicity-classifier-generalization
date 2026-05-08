# CS 260 — Toxicity Classifier Generalization

This project investigates how well toxicity classifiers generalize across different domains and demographic contexts. We compare rule-based, ML-based, and LLM-based approaches on tweet datasets.

---

## Project Structure

```
.
├── data/           # Raw and processed datasets (not tracked by git)
├── notebooks/      # Jupyter notebooks for each pipeline step
├── results/        # Output files, predictions, and evaluation metrics
├── report/         # Final written report
├── requirements.txt
└── README.md
```

---

## Setup

### 1. Install Python dependencies

```bash
pip install -r requirements.txt
```

### 2. Install Ollama

Ollama lets you run local LLMs (e.g., Llama 3.2) without an API key.

**macOS / Linux:**
```bash
curl -fsSL https://ollama.com/install.sh | sh
```

**Windows:** Download the installer from [ollama.com](https://ollama.com).

After installing, pull the model used in this project:

```bash
ollama pull llama3.2:latest
```

Start the Ollama server (it may start automatically; if not):

```bash
ollama serve
```

### 3. Add data

Place your tweet CSV files in the `/data` directory. They are excluded from git tracking. Each CSV should contain at least a `text` column with tweet content and a `label` column with ground-truth toxicity labels (e.g., `0` = non-toxic, `1` = toxic).

### 4. Launch Jupyter

```bash
jupyter notebook
```

Open notebooks from the `/notebooks` directory in order.

---

## Notebooks

| Notebook | Description |
|---|---|
| `step3_llm_pipeline.ipynb` | Zero-shot LLM inference via Ollama (llama3.2:latest) |

---

## Results

Predictions and evaluation metrics are saved to `/results/`.
