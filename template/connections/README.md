# connections/ — the lines out to your tools

Each file here describes one tool the OS can reach (email, calendar, tasks,
customers, money) and exactly what it's allowed to do there.

How these work, in plain terms:

- **Built once, reused forever.** Each tool gets researched once and written
  into a reference file here, so the OS never re-researches it. The owner
  never has to touch this folder.
- **Restricted on purpose.** Wherever possible, the OS gets its own limited
  account per tool — it can never act as you. Read-only until there's a
  reason to trust it with more.
- **Keys live in `.env` only** — gitignored, owned by you, never written in
  any file here and never pasted into chat.

Copy `_template.md` to start a new connection file.
