# SaZo_poster — Code Init Prompt
# Generálva: 2026-07-10 · Verzió: v1.1
# Master compliance: MASTER_BEST_PRACTICES.md v1.0

Reaktiválás esetén — döntéstől függően:

## LaTeX projektként
1. `main.tex` + `beamerposter` package
2. `latexmk -pdf main.tex` build
3. `Makefile` build automatizáláshoz
4. `.gitignore`: `*.aux`, `*.log`, `*.pdf`, `*.synctex.gz`, `*.out`, `*.fdb_latexmk`

## Python matplotlib projektként
1. Python 3.11+, `matplotlib`, `seaborn`
2. `pyproject.toml` (uv / poetry)
3. Output mappa: `dist/` (gitignored)
4. `.gitignore`: `*.pdf`, `*.png`, `__pycache__/`, `.venv/`

## SVG + Inkscape projektként
1. Forrás `.svg` commitolható (szöveges XML)
2. Exportált `.pdf`/`.png` gitignore
3. Build script Inkscape CLI-vel

Commit: `<type>: <mit> — <miért>`

---
## Automatizálási szabályok
- Minden műveletet API/CLI-vel hajts végre
- GitHub → gh CLI | HubSpot → API+hs | Google → MCP API |
  Gemini → API | MS365 → MCP API | Fájl → Code | Git → Code

Ha manuális lépés kellene:
⚠️ ÁLLJ MEG
Művelet: [mit kellene manuálisan]
Miért nem automatizálható: [ok]
Kockázat: [következmény]
Must-have: IGEN / NEM

Ha jogosultság hiányzik:
→ Írd ki: "[Alkalmazás] → [Szükséges scope] → [Hol kell beállítani]"
→ Várj amíg megadják, aztán folytasd automatikusan
