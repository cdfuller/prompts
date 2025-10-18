# Global Agent Guidelines

## Core Safety Practices
- Treat `.env`, secrets, production data, and other sensitive artifacts as read-only unless explicit approval is given; never make write-based API calls without instruction.
- Prefer automated tooling (linters, formatters, analyzers) over manual inspection when verifying code quality.

## Coding Standards
- In Python use 4-space indentation, `snake_case` for modules, functions, and variables, `PascalCase` for classes, and `UPPER_SNAKE_CASE` for constants.
- Skip Python type annotations; capture expectations with concise Google style docstrings or module comments when clarity is needed.
- Target Python 3.13 and manage dependencies with `uv` for Python projects.

## Tooling & Automation
- Reach for linting or static-analysis tools before manual review when identifying issues.
- Use Playwright MCP utilities when automated browser interaction or UI verification is required.

## Clarifying Questions
- Pause and initiate a clarifying round whenever goals, constraints, or priorities are unclear before generating major artifacts.
- Present questions as a numbered list; under each number provide alphabetical options, reserving Option A for the recommended path when one exists and keeping labels in order.
- Pair each option with a concise trade-off note so the user understands the implications of their choice.
- Conclude every question set with `Option X: Explain the options` to invite deeper exploration instead of committing immediately.

## Documentation & Onboarding
- Ensure project READMEs list baseline commands for installing dependencies, running the application, and executing tests.
- Include a concise tagline followed by a short description (no more than four sentences) that explains the problem the application solves.

## Session Summaries (On Request)
- Update `SESSION_SUMMARIES.md` only when the user explicitly asks or uses a trigger phrase (e.g., “append session”, “log session”, “update session summaries”, “follow SESSION_SUMMARIES.md”). If unsure, ask, “Do you want me to append a `SESSION_SUMMARIES.md` entry for this work?”
- Add new entries to the top (reverse-chronological), include `HH:MM` in the header, keep bullets concise, and link touched files.
- Follow the standard template exactly:

  ```
  ## [YYYY-MM-DD HH:MM] Short Title

  <1–3 sentence summary explaining major changes and key decisions.>

  - Agent: <agent name>
  - Model: <model name>
  - Changes: <key files/routes/views updated>
  - Decisions: <concise rationale>
  - Next: <1–3 concrete follow-ups>
  ```

- Write the summary paragraph in clear prose, highlighting major changes and decisions.
- Prefer `apply_patch` (or an equivalently focused approach) so the diff isolates the new entry.

## Version Control
- Compose commit messages using imperative verbs (Add, Update, Fix, Remove, Refactor, Create, etc.) and keep them to a single line with no trailing punctuation or personal pronouns.
- Avoid prefixes such as `feat:` or `fix:`; the leading verb conveys intent.
- Incorporate precise technical terms (file names, models, tools) as appropriate, and separate multiple related updates with commas or semicolons when needed.
- When multiple related changes are included, separate them with commas or semicolons in a single line
- Use minimal, precise wording, skipping unnecessary filler words

