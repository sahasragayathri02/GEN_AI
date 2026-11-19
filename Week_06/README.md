# Week 6 — Llama 3.2 Baseline Evaluation (Release v0.1)

## Files
- `golden_set.json` — 30 questions, expected answers, keywords and source links from the lab handout.
- `main.py` — sends questions to Ollama, scores keyword coverage and writes a CSV report.
- `requirements.txt` — Python dependency (`requests`).

## Run on macOS (VS Code)
1. Install the **Ollama** macOS app from https://ollama.com/download and open it.
2. In VS Code, choose **File → Open Folder…** and open `Week6_Llama32_Baseline`.
3. Open **Terminal → New Terminal**.
4. Check Python:
   ```bash
   python3 --version
   ```
5. Check Ollama:
   ```bash
   ollama --version
   ```
6. Download the model (one-time download):
   ```bash
   ollama pull llama3.2
   ```
   Keep Ollama running in the background.
7. Create and activate a virtual environment:
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```
8. Install the dependency:
   ```bash
   python -m pip install -r requirements.txt
   ```
9. Run the baseline:
   ```bash
   python main.py
   ```

When it finishes, `baseline_results.csv` is created in this same folder. It contains the LLM answer, expected answer, matched/missing keywords, score, status, source, model and release version for each question.

## If something goes wrong
- `ollama: command not found`: install/open the Ollama app, then close and reopen VS Code Terminal.
- Connection refused at `localhost:11434`: start/open Ollama and retry.
- Model not found: run `ollama pull llama3.2` and wait for it to finish.
- Missing `requests`: activate `.venv` and run `python -m pip install -r requirements.txt`.

Note: The handout's printed command says `pip install requirements.py`; the correct command for this folder is `python -m pip install -r requirements.txt`.
