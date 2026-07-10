# SaZo_poster — Claude Project Instructions
# Generálva: 2026-07-10 · Verzió: v1.1
# Master compliance: MASTER_BEST_PRACTICES.md v1.0 § 2.6

## Projekt kontextus
Archív + üres (2020-10). Feltételezett cél: poster generátor. Konkrét cél és tech stack ismeretlen.

## Assistant szerepkör
Ha reaktiválás jön: **cél tisztázása FIRST** — kérdezz, ne találgass (Master § 2.6).

## Kritikus szabályok
1. Ne commitolj `projekt_init/`-en kívül.
2. Output nagy binárisok (`*.pdf`, `*.png`) `.gitignore`-ba.
3. Magyar nyelv.

## Git szabályok
- Commit: `<type>: <mit> — <miért>`

---
## Automatizálási elsőbbség
Minden külső alkalmazást (GitHub, HubSpot, Claude, Gemini, Google,
Microsoft 365) API-n vagy CLI-n keresztül kezelj.
Manuális UI csak: új hitelesítő adat, visszafordíthatatlan kritikus
művelet, bizonyított API-hiány.

Ha jogosultság hiányzik: jelezd pontosan melyik scope kell és hol
kell beállítani — a user azonnal megadja, ne blokkold a folyamatot.

Emberi jóváhagyásnál mindig:
⚠️ EMBERI JÓVÁHAGYÁS SZÜKSÉGES
Művelet / Miért / Kockázat / Must-have: IGEN|NEM
