# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Purpose

This app performs a deep dive into the YouTube algorithm and uses that data to analyze a YouTube channel to find solutions for its success.

## Current State

The repository is in its initial scaffolding phase — no application code exists yet. The stack, framework, and project structure have not been chosen. Before writing any code, establish and document:

- The technology stack (e.g., Next.js, Python/FastAPI, Node + Express)
- How YouTube data will be fetched (YouTube Data API v3 requires an API key; OAuth 2.0 is needed for private channel data)
- Where and how analysis results will be stored
- Update this file with build/test/run commands once a stack is chosen

## License

GPL v3 — all contributions must remain GPL v3 compatible.

## CI

Two GitHub Actions workflows exist in `.github/workflows/`:

- **blank.yml** — placeholder CI triggered on push/PR to `main`; replace the echo steps with real build and test commands once the stack is chosen
- **codeql.yml** — CodeQL security scanning on push/PR to `main` and weekly on Sunday; currently only scans `actions` language; add the chosen application language(s) to the `matrix.include` list

When the stack is established, update `blank.yml` to run lint, tests, and build, and add the appropriate language entry in `codeql.yml`.
