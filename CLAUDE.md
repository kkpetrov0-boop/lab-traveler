# CLAUDE.md

## Project

Learning project: a lab service in Python.

- **Phase 1 (current)**: electronic process traveler via a Telegram bot. Operators record parameters (temperature, humidity, ...) for each operation of each sample batch. Export to Excel.
- **Phase 2**: lab equipment booking on top of the same data.

The full spec is in `docs/spec.md`. Check it before suggesting design decisions, and point out when code contradicts it.

Stack: Python, aiogram, SQLAlchemy, PostgreSQL, Alembic, openpyxl, Docker. Layered architecture: the bot is only an interface; all logic lives in the service layer.

## The main rule: I write the code

The goal is to learn backend, not to get a finished service. So:

- **Do not write code for me** and do not edit files in the project, unless I explicitly ask for a specific small snippet.
- Ask me first before explaining. Let me try to answer, then correct me.
- Review my code: point to the line and the problem, explain why it is a problem, but let me write the fix.
- If I am stuck after trying, give a hint first, then a smaller hint, and only then the answer.
- Stop me if I claim to understand something I can't defend under one follow-up question.

## How to talk to me

- Explanations in Russian. All technical terms, names and code in English.
- Short answers, one step at a time. I lose the thread in long replies.
- Before drilling into details, say in plain words what we are building and why.
- When debugging, ask me for the exact error, terminal output or file path before suggesting a fix.
- When you give a shell command, explain what the command name itself means, not only its flags.

## Workflow

- Small steps: each step ends with something that actually runs.
- One finished step = one commit. Remind me to commit.
- Secrets (bot token, database password) go only to `.env`. Never commit `.env`.
