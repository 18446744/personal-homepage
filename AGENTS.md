# AGENTS.md

## Project Goal

This project is for the first major assignment of Algorithm Foundations 2026.

The goal is to build a personal homepage with a first technical blog post, using an AI Agent assisted workflow. The final deliverables are:

- A public personal homepage URL.
- A blog page reachable from the homepage.
- A PDF assignment report including implementation process, AI usage, screenshots, and links.

Deadline: 2026-05-17 23:59.

## Required Features

The homepage must include:

- Personal introduction.
- Learning direction, technical interests, or research interests.
- Project display, learning records, or other personal content.
- A visible blog entry or blog list.
- A link to the first technical blog post.

The blog page must include:

- A clear title.
- A technical topic related to algorithms, data structures, math, AI, open source, learning methods, computational thinking, or future research direction.
- Personal understanding and reflection.
- A link back to the homepage.

## Tech Stack

Use a simple static website:

- HTML
- CSS
- Minimal JavaScript only if necessary
- Deploy with GitHub Pages

Do not introduce frontend frameworks unless there is a clear reason.

## Suggested File Structure

- `index.html`: homepage
- `style.css`: shared styles
- `blog/first-blog.html`: first technical blog post
- `docs/ai/decisions.md`: project decisions and rationale
- `docs/ai/handoff.md`: task handoff notes
- `report/report.tex`: assignment report draft, written in LaTeX

## Workflow Rules

Follow this workflow for non-trivial tasks:

1. Read this `AGENTS.md` first.
2. Check the current file structure and Git status.
3. If the task is unclear, ask clarifying questions before editing.
4. Before large edits, briefly describe the plan.
5. Execute in small, reviewable steps.
6. After editing, verify links, layout, and required assignment items.
7. Summarize changed files, verification results, and next steps.
8. For each meaningful content, layout, workflow, or report change, update `docs/ai/handoff.md` so later maintainers can understand what changed, why it changed, how it was checked, and what remains open.

## Report Rules

- Write the assignment report in LaTeX.
- Use `report/report.tex` as the source file.
- The report should be compilable with XeLaTeX because it contains Chinese text.
- Keep the report structure aligned with the assignment PDF: homepage introduction, blog introduction, implementation process, AI Agent usage, screenshots, and submission links.

## Content Rules

- The website should be personalized and truthful.
- Blog ideas may be polished by AI, but the core thinking must come from the student.
- Avoid fake projects, fake awards, fake research experience, or unverifiable claims.
- Keep the writing clear, specific, and suitable for a course assignment.

## Design Rules

- The homepage should be clean, readable, and visually organized.
- The layout should work on both desktop and mobile screens.
- Navigation links must be obvious.
- Avoid overly complex visual effects.
- Prioritize clarity over decoration.

## Safety Rules

Ask for confirmation before:

- Deleting files.
- Rewriting the whole project structure.
- Running deployment commands.
- Committing or pushing to a remote repository.

Do not modify files outside this project directory unless explicitly asked.

## Verification Checklist

Before reporting completion, check:

- The homepage opens normally.
- The blog page opens normally.
- The homepage links to the blog page.
- The blog page links back to the homepage.
- The layout is readable on common screen sizes.
- The project still matches the assignment PDF requirements.
- Git status and changed files are summarized.

## Handoff Format

At the end of each larger work session, update or summarize:

- Current goal
- Current state
- Files changed
- Verification performed
- Open questions
- Recommended next step
