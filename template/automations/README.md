# automations/ — what runs on its own

Each automation gets one folder here holding its record: an ABOUT.md (what it
does, where it lives, its trust status), a SETUP.md (how it was authorized and
how to verify it), and its logs — or a pointer to where logs land.

Two things worth knowing:

- **The code may live elsewhere.** Bigger automations that run in the cloud
  get their own small, clearly-labeled repo so runs stay fast and lean. The
  ABOUT.md always says where. This folder is the map; the machinery can sit
  in another building.
- **Every automation climbs a trust ladder.** It starts as a **beta**
  (a person checks every run), gets **proven** (it passes this business's
  custom quality checks consistently), and only then runs **automated**.
  Anything that sends outbound messages or moves money keeps a human yes
  forever, unless the owner explicitly decides otherwise.

Every automation here was watched running successfully before it was
installed, and each one keeps logs so its health can be checked at any time.

Copy `_template/` to start a new automation record.
