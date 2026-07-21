# Changelog

All notable changes to this repository are documented here. Format loosely follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [1.0.0] — 2026-07-22

### Added
- Repository restructured from the previous `Workflows` repo into a portfolio-style layout under `AI-Projects/`.
- Five agent projects added, each with its own README, `.env.example`, license, and exported workflow JSON:
  - `ai-hr-recruitment-agent` — candidate intake, AI resume scoring, ATS tracking, and interview/rejection automation.
  - `ai-email-agent` — inbox triage, AI-drafted replies, and deadline-driven calendar event creation.
  - `ai-executive-assistant-agent` — daily email/meeting/Slack/to-do assistant built on Claude.
  - `ai-multi-agent-orchestrator` — Telegram-based orchestrator that routes to specialist sub-agents.
  - `ai-research-agent` — callable research sub-agent (Wikipedia → Hacker News → SerpAPI fallback chain).
- Root-level documentation: `README.md`, `ARCHITECTURE.md`, `CONTRIBUTING.md`, `LICENSE`, `.gitignore`.

### Changed
- Workflow files renamed from their original export names to consistent, professional, kebab-case filenames (see individual project READMEs for the old → new mapping).

### Notes
- This is the first documented release of the restructured portfolio. Prior history from the `Workflows` repository is not carried forward; see project READMEs for a description of each workflow's original source file.
