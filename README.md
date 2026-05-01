# Pamplin AI Teaching Workshop Triage Platform

## Local development

This platform requires being served from a local HTTP server (it cannot be opened from `file://` due to fetch behavior in modern browsers).

From this directory, run:

    python -m http.server 8000

Then open `http://localhost:8000/` in a browser.

To run the smoke test, open `http://localhost:8000/test_smoke.html` after the platform is loaded.

## Production deployment

Host the project root on any static-file web server. The platform makes no API calls except to the agent URL and the backend endpoint, both of which live in `config.json`.

## Files

- `index.html` — the platform itself.
- `config.json` — all committee-revisable content (Step 1/2/4 options, departments, copy strings, agent URL, backend URL).
- `PROMPT_AGENT.md` — the prompt template the platform fills in for faculty.
- `test_smoke.html` — synthetic end-to-end walkthrough for sanity checking after edits.
- `README.md` — this file.

## Documentation

For architecture, design rationale, and deployment instructions, see `SPEC.md` and `BACKEND_STUB.md` in the project repository.
