# Repository Guidelines

## Project Structure & Module Organization
- Use a simple, predictable layout as the project grows:
  - `src/` — application code (modules by domain; e.g., `src/auth/`, `src/api/`).
  - `tests/` — automated tests mirroring `src/` (e.g., `tests/api/`).
  - `scripts/` — developer utilities (setup, lint, release).
  - `docs/` — architecture notes and diagrams.
  - `assets/` — static files (images, sample data).
- Keep modules small and cohesive; prefer feature folders over giant utils.

## Build, Test, and Development Commands
This repo currently has no toolchain files. When adding them, prefer Make targets or npm scripts with clear names:
- Build: `make build` or `npm run build` — compiles/bundles sources.
- Test: `make test` or `npm test` — runs unit/integration tests.
- Lint/Format: `make lint` / `make fmt` or `npm run lint` / `npm run format`.
- Local run: `make dev` or `npm run dev` — starts a watch server or CLI.
- Setup: `scripts/setup.sh` — installs dependencies and pre-commit hooks.

## Coding Style & Naming Conventions
- Indentation: 2 spaces (JS/TS, JSON, YAML), 4 spaces (Python).
- Names: `PascalCase` for types/classes, `camelCase` for functions/vars, `kebab-case` for files, `snake_case` for Python.
- Keep functions < 50 lines; extract helpers early.
- Use linters/formatters when introduced (ESLint+Prettier for JS/TS; Ruff/Black for Python). Example: `npm run lint && npm run format`.

## Testing Guidelines
- Frameworks: Jest/Vitest (JS/TS) or Pytest (Python) — choose one per language.
- Mirror `src/` structure under `tests/`; name files `*.test.ts` or `test_*.py`.
- Aim for ≥80% line coverage on critical modules; include edge cases and error paths.
- Example: `npm test -- --watch` or `pytest -q`.

## Commit & Pull Request Guidelines
- Use Conventional Commits: `feat:`, `fix:`, `docs:`, `chore:`, `refactor:`, `test:`.
- Write imperative, present-tense subjects; include scope when helpful: `feat(api): add rate limiting`.
- PRs must include: clear description, linked issue (e.g., `Closes #12`), screenshots or logs for UI/UX or CLI changes, and test updates.
- Keep PRs under ~300 lines of reviewable change; split large work.

## Security & Configuration
- Never commit secrets. Use `.env` for local, and track a sanitized `./.env.example` with required keys.
- Add `.gitignore` entries for environment files, build artifacts, and IDE files.
- Document config in `docs/config.md` once stabilized.

