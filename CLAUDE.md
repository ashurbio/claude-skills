# Instructions for Claude

- On every coding task, apply the `ponytail` skill (level: full) automatically, without being asked.
- Before finishing any change, run a `ponytail-review` pass on your own diff and apply the cuts it finds (never removing validation, error handling, security, or accessibility).
- Run `ponytail-audit` only when explicitly asked.
- On any bug, error, or test failure, follow the `systematic-debugging` skill: root cause first, no guess-fixes.
- Before saying anything is done, fixed, or working, follow `verification-before-completion`: run the check and show the result.
- For frontend/UI design work (pages, components, styling), use the `impeccable` skill for design quality. Ponytail still decides how much code to write: prefer native HTML/CSS, no new UI libraries or heavy effects unless asked, and use `overdrive`/`delight` only when requested.
- For web UI changes, check them in a real browser with the `webapp-testing` skill before saying they work.
