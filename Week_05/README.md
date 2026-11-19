# Week 5 — Token Economics

## Files
- `budget.py` — calculates token usage, estimated cost, RPM/TPM capacity and budget checks.
- `test_budget.py` — four automated unit tests.
- `.env` — illustrative planning assumptions (not API credentials).
- `requirements.txt` — Python dependency.

## Run on macOS (VS Code)
1. Unzip this folder.
2. Open VS Code → **File → Open Folder…** → select `Week5_TokenEconomics`.
3. Open **Terminal → New Terminal**.
4. Check Python: `python3 --version`
5. Create a virtual environment:
   ```bash
   python3 -m venv .venv
   ```
6. Activate it:
   ```bash
   source .venv/bin/activate
   ```
7. Install dependencies:
   ```bash
   python -m pip install -r requirements.txt
   ```
8. Run the planner:
   ```bash
   python budget.py
   ```
9. Run the tests:
   ```bash
   python -m unittest -v
   ```

The sample values should produce about 2,400,000 input tokens/day, 600,000 output tokens/day, 3,000,000 total tokens/day, $1.44/day and $43.20 for 30 days. These are planning estimates only. Replace the illustrative prices and limits with the values for your actual model/account.

If VS Code asks for an interpreter, choose the Python interpreter inside `.venv`.
