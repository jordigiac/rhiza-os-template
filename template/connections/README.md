# connections/ — the lines out to your tools

Each file here describes one tool the OS can reach (email, calendar, tasks,
customers, money) and exactly what it's allowed to do there.

How these work, in plain terms:

- **Built once, then healing forever.** Each tool gets explored on first
  contact — test what actually works, then write the reference file from
  the truth. From then on the file is a living document: every failed
  call, broken endpoint, or discovered quirk gets written in the moment
  it's found, so the next run reads the lesson instead of repeating the
  mistake. The owner never has to touch this folder.
- **OAuth over pasted secrets, wherever possible.** A native Claude
  connector first (sign in once, revoke anytime, no keys in the folder),
  an MCP server second, an API key in `.env` only when neither exists.
- **Restricted on purpose.** Wherever possible, the OS gets its own limited
  account per tool — it can never act as you. Read-only until there's a
  reason to trust it with more.
- **Keys live in `.env` only** — gitignored, owned by you, never written in
  any file here and never pasted into chat.

Copy `_template.md` to start a new connection file.
