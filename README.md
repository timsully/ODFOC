# ODFOC — Oregon Detention Facility Oversight (Initiative 2026-081)

Public-facing website and reference materials for **Initiative 2026-081**, which would create the **Oregon Detention Facility Oversight Commission**—an independent state body focused on transparency, conditions of confinement, and accountability for detention facilities on Oregon soil, including those tied to federal immigration enforcement.

The living site explains the measure in plain language, directs **Oregon registered voters** to the official **sponsorship e-sheet**, and provides a voluntary **email pledge** flow for supporters (the e-sheet is what counts for ballot sponsorship under Secretary of State rules).

## Project intentions

- **Educate** visitors about why the initiative exists and what it would do (summary cards and optional context).
- **Drive correct action** for sponsorship: download **`2026-081 SP E sheet 03202026.docx`**, complete and e-sign per the sheet’s instructions, and email it to **`ahelpinghandlocksmith@gmail.com`**.
- **Stay lightweight**: single-page static HTML, no build pipeline, easy to host on **GitHub Pages** or any static host.
- **Work on phones and desktops**: layout and tap targets are tuned for small screens; forms use 16px inputs where it matters for mobile browsers.

Legal and campaign filings live with the chief petitioner and the Oregon Secretary of State; this repository is for **outreach and clarity**, not a substitute for the official petition text or filing instructions.

## What’s in the repo

| Item | Role |
|------|------|
| `index.html` | Full site: styles, copy, e-sheet download link, mailto-based pledge form |
| `2026-081 SP E sheet 03202026.docx` | Official-style electronic signature sheet (hosted for download) |
| Other `.docx` files (if present locally) | Fact sheets, draft initiative text, etc.—may or may not be tracked in git |

## Development environment

There is **no** Node, bundler, or package install. Any static file server is enough.

### Prerequisites

- **Git** — to clone and push changes.
- **A browser** — Chrome, Firefox, Safari, or Edge.
- **Optional:** **Python 3** (often preinstalled on macOS/Linux) or **npx** (if you use Node elsewhere) for a local server.

### Clone the repository

```bash
git clone https://github.com/timsully/ODFOC.git
cd ODFOC
```

If the repo is transferred to another owner, replace the URL with `https://github.com/<owner>/ODFOC.git`.

### Run locally (recommended)

Serving over `http://localhost` behaves more like production than opening `index.html` directly (relative links and downloads match GitHub Pages).

**Python 3:**

```bash
cd ODFOC
python3 -m http.server 8080 --bind 127.0.0.1
```

Then open **http://127.0.0.1:8080/** (or **http://127.0.0.1:8080/index.html**).

**Node (npx), if you prefer:**

```bash
cd ODFOC
npx --yes serve -l 8080
```

Stop the server with **Ctrl+C** in that terminal.

### Edit and publish

1. Edit `index.html` (or add assets next to it).
2. Commit and push to the branch GitHub Pages uses (e.g. **`main`**).

For this project, Pages is configured from the **repository root**, so `index.html` at the top level is the homepage.

### GitHub Pages

With Pages enabled on **`main`** / **root**, the site is served at:

**https://timsully.github.io/ODFOC/**

That URL updates if the repository is renamed or transferred; check **Settings → Pages** after any ownership change.

## License / usage

Campaign and legal materials may be subject to separate terms or filing requirements. Treat web copy as informational; when in doubt, rely on the **filed initiative text** and **Oregon elections** guidance.
