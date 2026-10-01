# Instructions for Claude

- On every coding task, apply the `ponytail` skill (level: full) automatically, without being asked.
- Before finishing any change, run a `ponytail-review` pass on your own diff and apply the cuts it finds (never removing validation, error handling, security, or accessibility).
- Run `ponytail-audit` only when explicitly asked.
- On any bug, error, or test failure, follow the `systematic-debugging` skill: root cause first, no guess-fixes.
- Before saying anything is done, fixed, or working, follow `verification-before-completion`: run the check and show the result.
