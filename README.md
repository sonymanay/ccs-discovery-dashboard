# CCS Content Authoring — Discovery Dashboard

Interactive single-file dashboard for live findings synthesis.

## How to use

### Option A — Live (hosted)
1. Open the dashboard URL from this repo (or GitHub Pages mirror).
2. Dashboard auto-loads `findings/baseline.json` on first visit.
3. Edit any field — changes auto-save to your browser's localStorage.
4. **Export** to share findings as JSON with the team.
5. **Import** a JSON file from a teammate to load their findings.

### Option B — Offline (download)
1. Download `index.html` + `findings/baseline.json`.
2. Open `index.html` in any modern browser.
3. (Auto-fetch won't run on `file://` — use **Import** to load baseline.json manually.)
4. Edit, Export, Import, Print as in Option A.

## Tabs
- **Overview** — project metadata, vision statement, persona snapshot cards.
- **Personas** — detailed profile + verbatim quotes per persona.
- **Pillar × Persona** — clickable H/M/L heat-map across the 6 pillars.
- **Lifecycle × Persona** — friction map across 8 lifecycle stages.
- **Themes** — recurring cross-persona patterns tagged to pillars.
- **Opportunities** — backlog with impact × effort scatter plot.
- **Decisions & Next Steps** — open decisions and concrete actions.

## Source of truth workflow
- `findings/baseline.json` — canonical starting state. Regenerated automatically by the daily sync from `sync/regenerate_baseline.py`. **Do not hand-edit** — change the Python script instead.
- `findings/YYYY-MM-DD-readout.json` — point-in-time synthesis snapshots. Commit one after each readout.
- Teammates: Import the latest snapshot to view current findings.

## Notes
- No backend, no external network calls — works offline.
- Theme follows system preference; toggle in the header.
- Reset clears localStorage (export first if you want a backup).
- All seed cell values, themes, opportunities are **HYPOTHESES to validate**, not findings.
