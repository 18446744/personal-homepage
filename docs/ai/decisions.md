# Project Decisions

## 2026-05-04: Use a Static Website

Decision: Build the assignment as a static website using HTML and CSS, with minimal JavaScript only if necessary.

Reason:

- The assignment requires a personal homepage and a technical blog page, not a complex web application.
- Static pages are easy to inspect, deploy, and maintain.
- GitHub Pages can host the result for free and produces a stable public URL.

## 2026-05-04: Use `AGENTS.md`

Decision: Use `AGENTS.md` as the AI Agent project instruction file.

Reason:

- The course handout recommends using a project specification document such as `CLAUDE.md` or `AGENTS.md`.
- This keeps project goals, constraints, verification rules, and handoff format in the repository.
- Future AI-assisted work can start from the same context instead of relying only on chat history.
