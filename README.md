# Burt Gardner

Full-stack .NET & Azure engineer — 18 years at Walmart Global Tech. I build
LLM-assisted systems the way security tooling has to be built: the model gets a
voice, never a vote.

## Start here

**[DevSecOps Sentinel](https://github.com/bgard68/DevSecOpsSentinel)** — a
GitHub Actions supply-chain analyzer where deterministic rules decide what is
true and a schema-constrained model explains it.
**[Try it live](https://gentle-ground-047e1fb10.7.azurestaticapps.net)** — no
signup, nothing to install.

The part I'd want you to look at: the test suite includes a workflow whose
comments tell the model to invent a finding and suppress a real one — the
prompt-injection case, since scanned content is attacker-controlled — plus a
recorded reply where the model *obeys*. The reply is rejected anyway, because a
rule id the scanner never produced cannot survive the containment gate. The
gate is mutation-tested, the rules are scored against a golden corpus written
independently of the code, and the whole eval runs offline on every push.
Scanned against 564 workflows from 14 major OSS repositories: 100% parsed, 94%
carried findings, zero false positives on the clean baseline.

**[WidgetWorks](https://github.com/bgard68/WidgetWorks)** — an e-commerce store
built to a production security posture: JWT with rotating refresh tokens, TOTP
2FA, Google sign-in, atomic stock reservation, server-side re-priced checkout,
pluggable payments. **[Live store](https://black-wave-0aaf4010f.7.azurestaticapps.net)**
— demo accounts for all three roles are on the landing page.

## Also on the shelf

- **[ClaudeChessApp](https://github.com/bgard68/ClaudeChessApp)** — chess fully
  client-side: Stockfish, clocks, 2,987 World Championship games, a SQLite
  library, no backend at all
- **[Net10Sudoku](https://blazor-sudoku-net10.azurewebsites.net)** — Blazor
  generator/solver, deployed
- **[LotteryApp](https://github.com/bgard68/LotteryApp)** — Powerball & Mega
  Millions checking against 24 years of real drawings, .NET 10 + Dapper
- **[ToDoApp](https://github.com/bgard68/ToDoApp)** — Clean Architecture + CQRS
  kanban with revocable JWT auth

Everything above is .NET 10 / C#, CI-gated with CodeQL, gitleaks and dependency
review, deployed on Azure free tiers, and built in collaboration with AI agents
under the constraint the flagship demonstrates: generated code ships only after
deterministic checks say it may.
