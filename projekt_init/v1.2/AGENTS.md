# SaZo_poster — Claude munkajegyzőkönyv
# Generálva: 2026-07-10 · Verzió: v1.1
# Master compliance: MASTER_BEST_PRACTICES.md v1.0 (cafc412)
# Projekt-típus: **Placeholder / üres** (MASTER § 2.6)


## ⚡ Automatizálási elsőbbség

**Minden külső alkalmazást API/CLI-n keresztül kezelünk.**
Manuális UI csak az alábbi kivételekben megengedett:
- Új hitelesítő adat generálása (token, jelszó, API key)
- Visszafordíthatatlan kritikus művelet (explicit jóváhagyással)
- Bizonyított, dokumentált API-hiány

### Automatizálható alkalmazások és eszközök
| Alkalmazás | Eszköz | Scope / előfeltétel |
|---|---|---|
| GitHub | gh CLI + GitHub API | repo, workflow, read:org |
| HubSpot CRM | HubSpot API + hs CLI | Private App token |
| HubSpot CMS | hs cms upload | PAK token |
| Claude | Anthropic API + MCP | API key |
| Gemini | Gemini API | API key |
| Google Drive | Drive API (MCP) | OAuth csatolva |
| Gmail | Gmail API (MCP) | OAuth csatolva |
| Google Calendar | Calendar API (MCP) | OAuth csatolva |
| Microsoft 365 | MS Graph API (MCP) | OAuth csatolva |
| OneDrive sync | sync.ps1 (rclone) | rclone config |
| Fájlírás | Claude Code | — |
| Git | Claude Code | gh auth |
| Web keresés | Claude Chat tool | — |

### Jogosultság hiány esetén
Ha egy automatizáláshoz jogosultság hiányzik:
1. Jelezd pontosan: melyik scope / permission kell
2. Jelezd hol kell beállítani (pl. GitHub token → Settings → Developer)
3. Folytasd amint megvan — ne várj tovább

### Emberi jóváhagyás — kötelező formátum
Ha mégis kérdezni KELL (csak kritikus esetben):

⚠️ EMBERI JÓVÁHAGYÁS SZÜKSÉGES
Művelet: [pontosan mit hajt végre]
Miért kell jóváhagyás: [konkrét ok]
Kockázat: [mi történhet rossz döntés esetén]
Must-have a folytatáshoz: IGEN / NEM
→ Válaszolj: IGEN / NEM

---

## ⚠️ Élesség és kockázat
- **Élesség:** ARCHÍV + ÜRES — 2020-10 óta 1 commit, csak README
- **Kockázati szint:** MINIMÁLIS (nincs kód, nincs adat)
- **Következmények:** —

---

## 1. Projekt
- **Név:** SaZo_poster
- **Cél:** Feltételezett — tudományos/konferencia poster generátor (LaTeX beamerposter vagy Python matplotlib). Nem biztos.
- **Tulajdonos:** ilozas / Zoltan Sas
- **Git repo:** https://github.com/ilozas/SaZo_poster
- **Élesség:** placeholder — reaktiváláskor tisztázandó cél

## 2. Tech stack
❓ Nincs rögzítve (üres repo)

## 3. Mappastruktúra
```
SaZo_poster/
├── README.md               ← csak 1 sor ("# SaZo_poster")
└── projekt_init/{v1.0,v1.1,CHANGELOG.md}
```

## 4. Titkok és érzékeny fájlok
Nincs — üres repo.

## 5. Ismert biztonsági problémák
Nincs.

## 6. API / integrációk
Nincs.

## 7. Jogi / GDPR
Nem alkalmazható.

## 8. Fejlesztési sorrend (ha reaktiválás)
**MASTER § 2.6 (Placeholder projekt) alapján:**
1. **Cél tisztázása FIRST** — kérdezz explicit kérdéseket, ne találgass:
   - Mire kell a poster? (Konferencia? Egyetemi? Marketing?)
   - Formátum? (A0/A1/custom, PDF/PNG)
   - Tech? (LaTeX beamerposter / Python matplotlib / SVG+Inkscape)
   - Adatforrás? (statikus / élő pl. Grafana snapshot)
2. **README kibővítés** cél + tech döntéssel
3. **`.gitignore`** létrehozás
4. **Példa input adat + kimeneti template**

## 9. Automatizálási elsőbbség
| Feladat | Módszer |
|---|---|
| Build | `latexmk` / Makefile / Python script |
| Output nagy binárisok | `.gitignore` (nem commit) |

## 10. Commit szabályok
Commit: `<type>: <mit> — <miért>`

**Ne commit:** output binárisok (`*.pdf`, `*.png`), `*.aux`, `*.log` (LaTeX build)

## 11. Session start checklist
- [ ] Cél tisztázva?
- [ ] Tech stack eldöntve?
- [ ] Formátum specifikáció megvan?

## 12. Ismert korlátok
| Korlát | Kezelés |
|---|---|
| Cél nincs specifikálva | Kérdezz user-től első lépésként |
| Nagy output fájlok | `.gitignore`, esetleg Git LFS |

## 13. Technikai döntések
| Döntés | Indok |
|---|---|
| Placeholder-státusz dokumentálva | Elkerüli a "csak README-val kezdek" újbóli megismétlést |
| Cél-tisztázás kötelező reaktiváláskor | Master § 2.6 |
