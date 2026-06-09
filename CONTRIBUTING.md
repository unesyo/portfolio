# Contributing to AI Portfolio Builder

Thank you for helping turn the current portfolio into a reusable open source
AI Portfolio Builder.

## Before You Start

- Read the [roadmap](docs/ROADMAP.md) and [MVP definition](docs/MVP.md).
- Check existing issues before proposing duplicate work.
- Keep changes focused and preserve the current portfolio unless an issue
  explicitly calls for a migration.
- Clearly label prototype behavior and do not present planned features as
  production-ready.

## Proposing a Feature

Open a feature request describing the user problem, proposed behavior, scope,
and alternatives. For larger features, discuss the approach before investing
in a full implementation.

## Reporting a Bug

Use the bug report template and include reproducible steps, expected behavior,
actual behavior, browser or environment details, and screenshots when useful.

## Local Setup

The current project is a static website and has no dependency installation
step:

```bash
git clone https://github.com/unesyo/portfolio.git
cd portfolio
python -m http.server 8000
```

Open `http://localhost:8000` and verify your changes in a modern browser.

## Pull Requests

- Create a focused branch and keep the pull request small.
- Explain the problem and the chosen solution.
- Update relevant documentation.
- Test changed behavior locally.
- Preserve third-party notices and licenses.
- Include screenshots for visible UI changes.

## Quality Expectations

- Use clear, accessible, responsive UI patterns.
- Avoid committing secrets or personal data that should not be public.
- Treat extracted career data as sensitive user data.
- Keep documentation and code in English.
- Add tests when test infrastructure becomes available.
- Prefer simple architecture appropriate for the current project phase.
