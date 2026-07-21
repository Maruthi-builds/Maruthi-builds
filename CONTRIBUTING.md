# Contributing

Thanks for your interest in this project. While this repository primarily serves as a personal portfolio of AI agent workflows, contributions, suggestions, and forks are welcome.

## Ways to contribute

- **Bug reports** — if you import a workflow and something's broken or a README is inaccurate, please open an issue.
- **Improvements** — better prompts, more robust error handling, additional guardrails, or cleaner node organization are all welcome.
- **New agents** — if you build a complementary agent that fits this repo's style, feel free to propose it via PR (see [`ARCHITECTURE.md`](./ARCHITECTURE.md) for the expected structure).
- **Documentation** — typo fixes, clearer setup steps, and additional examples are always appreciated.

## Ground rules

1. **Don't commit secrets.** Never include real API keys, OAuth tokens, or credential values in a workflow JSON, README, or example file. Use placeholders (see the `.env.example` files for the expected format).
2. **Preserve workflow logic.** If you're proposing a documentation or structure change, don't alter the underlying automation logic in the same PR — keep functional changes and cosmetic/organizational changes separate so they're easy to review.
3. **Follow the existing project structure.** Each agent folder should contain a `README.md`, `LICENSE`, `.env.example`, and a `workflow/` folder with the exported JSON. See [`ARCHITECTURE.md`](./ARCHITECTURE.md) for the full convention.
4. **Write in the same documentation style.** Each project README covers: overview, problem statement, features, architecture/workflow, setup, environment variables, usage, and future improvements. Keep new/edited READMEs consistent with that structure.

## Submitting a change

1. Fork the repository.
2. Create a feature branch: `git checkout -b feature/short-description`.
3. Make your changes.
4. Commit with a clear message: `git commit -m "Add retry logic to email agent"`.
5. Push and open a pull request describing what changed and why.

## Code of conduct

Be respectful and constructive. This is a small, personal-portfolio-style project — issues and PRs should be scoped accordingly.
