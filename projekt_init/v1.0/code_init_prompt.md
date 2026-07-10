# SaZo_poster — Code Init Prompt
# Generálva: 2026-07-10 · Verzió: v1.0

Ha reaktiváljuk mint LaTeX projekt:
1. `main.tex` + `beamerposter` package
2. `.gitignore`: `*.aux`, `*.log`, `*.pdf`, `*.synctex.gz`, `*.out`, `*.fdb_latexmk`
3. `latexmk -pdf main.tex` build parancs
4. `Makefile` build automatizáláshoz

Ha Python matplotlib projekt:
1. Python 3.11+, `matplotlib`, `seaborn`
2. `pyproject.toml` (uv / poetry / pip)
3. `.gitignore`: `*.pdf`, `*.png`, `__pycache__/`, `.venv/`
4. Output mappa: `dist/` (gitignored)

Commit: `<type>: <mit> — <miért>`
