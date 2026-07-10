# SaZo_poster — Claude munkajegyzőkönyv
# Generálva: 2026-07-10 · Verzió: v1.0

> **⚠️ ARCHÍV REPO — 2020-10 óta inaktív. LÉNYEGÉBEN ÜRES.**

## Aktuális állapot
- 1 commit (Initial commit, 2020-10-16)
- Csak `README.md` van benne, minimális tartalommal (`# SaZo_poster`)
- Nincs kód, nincs konfiguráció, nincs dokumentáció a projekt céljáról

## Feltételezett cél (README nélkül)
A név alapján valószínűleg **tudományos/konferencia poster generátor** — SaZo (Sas Zoltán?) nevéhez kapcsolódóan. Vagy LaTeX beamerposter, vagy Python matplotlib alapú. Nem biztos.

## Ha a projektet felélesztjük — döntendő kérdések
1. Mi a poster célja? (Konferencia? Egyetemi? Marketing?)
2. Formátum? (A0 / A1 / custom, PDF / PNG)
3. Tech: LaTeX + tikz / Python matplotlib / SVG + Inkscape?
4. Adatforrás: statikus / élő (pl. Grafana snapshot)?

## Ha újraaktiváljuk
- Új branch: `feature/reactivate-2026`
- README kibővítés: konkrét cél, formátum, tech stack
- `.gitignore`: `*.pdf`, `*.png`, `*.aux`, `*.log` (LaTeX build artifacts)
- Példa input adat + kimeneti template mentés

## Munkamenet szabályok Claude számára
- Ne javasolj tech stack-et user preferencia nélkül
- Output fájlok (`*.pdf`, `*.png`): `.gitignore`, nem commit (nagy binárisok)
- Commit: `<type>: <mit> — <miért>`
