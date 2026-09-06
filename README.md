# Burt Gardner

I build LLM-powered systems the way security tooling has to be built: the model
gets a voice, never a vote. Eighteen years shipping production code at Walmart
Global Tech, and a year since on self-directed R&D into making generated code
safe to trust.

*Open to AI engineering roles — [résumé](https://github.com/bgard68/bgard68/blob/main/Burt_Gardner_Resume.pdf) · [contact below](#reach-me).*

## Start here

**[DevSecOps Sentinel](https://github.com/bgard68/DevSecOpsSentinel)** — a
GitHub Actions supply-chain analyzer where deterministic rules decide what is
true and a schema-constrained model explains it.
**[Try it live](https://gentle-ground-047e1fb10.7.azurestaticapps.net)** — no
signup, nothing to install.

**The part I'd want you to look at:** the test suite includes a workflow whose
comments tell the model to invent a finding and suppress a real one — the
prompt-injection case, since scanned content is attacker-controlled — plus a
recorded reply where the model *obeys*. The reply is rejected anyway, because a
rule id the scanner never produced cannot survive the containment gate.
**Weaken that gate to a count comparison and 5 of its 14 containment tests
fail.**

The rules are scored against a golden corpus written independently of the code,
and the whole eval runs offline in CI — no API key, no network, no spend.
Scanned against 564 workflows from 14 major OSS repositories: 100% parsed, 94%
carried findings, and two Critical rules returning zero across every file
alongside 796 unpinned-action hits — a rule set discriminating, not spraying.

**[WidgetWorks](https://github.com/bgard68/WidgetWorks)** — an e-commerce store
built to a production security posture: JWT with rotating refresh tokens, TOTP
2FA, Google sign-in, atomic stock reservation, server-side re-priced checkout,
pluggable payments. **[Live store](https://black-wave-0aaf4010f.7.azurestaticapps.net)**
— demo accounts for all three roles are on the landing page.

## Also shipped

- **[BI-Simulator](https://github.com/bgard68/BI-Simulator)** — the
  "bring 18 data sources together" problem, done agentically twice over: an
  AI agent built the pipeline (messy SQLite/CSV/JSON/JSONL/XML exports
  conformed, joined, flattened into one analytical model with a live
  cross-filtering dashboard), and an LLM now runs *inside* it — mapping an
  unseen 19th source from a closed transform vocabulary, landing only past
  eleven deterministic gates, negative-case tested, prompt-injection canary
  included. Deterministic by seed, replayed by CI on every push.
  [Try it live](https://bgard68.github.io/BI-Simulator/) ·
  [the evidence](https://bgard68.github.io/BI-Simulator/mapping.html)
- **[ClaudeChessApp](https://github.com/bgard68/ClaudeChessApp)** — chess fully
  client-side: Stockfish, clocks, 2,969 World Championship games, a SQLite
  library, no backend at all,
  [try it live](https://happy-coast-011b8f510.7.azurestaticapps.net)
- **[data-structure-studio](https://github.com/bgard68/data-structure-studio)** —
  an animated data-structure lab for CS students: every frame is driven by real
  pointer mutations, a live step counter makes Big-O observable, and the trees
  run up to hand-implemented AVL and CLRS red-black. Zero dependencies,
  [try it live](https://bgard68.github.io/data-structure-studio/)
- **[Net10Sudoku](https://github.com/bgard68/Net10Sudoku)** — Blazor
  generator/solver,
  [try it live](https://blazor-sudoku-net10.azurewebsites.net)
- **[LotteryApp](https://github.com/bgard68/LotteryApp)** — Powerball & Mega
  Millions checking against 4,493 real drawings — Mega Millions back to 2002,
  Powerball to 2010 — .NET 10 + Dapper,
  [try it live](https://thankful-grass-06c113f10.7.azurestaticapps.net)
- **[ToDoApp](https://github.com/bgard68/ToDoApp)** — Clean Architecture + CQRS
  kanban with revocable JWT auth, React SPA over a .NET 10 API,
  [try it live](https://salmon-field-054249810.7.azurestaticapps.net) — demo
  account is on the sign-in page

Everything above is .NET 10 / C# — with React front ends on ToDoApp,
WidgetWorks and Sentinel, and Angular on LotteryApp — except ClaudeChessApp,
which is React and TypeScript with no backend at all, the BI simulator, which
is deliberately dependency-free Python, and the data-structure studio, which is
zero-dependency vanilla JavaScript. All of it is CI-gated: CodeQL across the
board, dependency review on every repo with dependencies to review (the BI
simulator and the studio, dependency-free, have none), and secret
scanning everywhere — gitleaks in CI on five repos, GitHub push protection on
Net10Sudoku and the BI simulator. Deployed on free tiers — Azure and GitHub
Pages — and built in collaboration with AI agents under the constraint the
flagship demonstrates: generated code ships only after deterministic checks say
it may.

## Reach me

Open to AI engineering roles — building LLM-powered systems, or putting
guardrails around the ones that already exist.

[bgard68@gmail.com](mailto:bgard68@gmail.com) ·
[LinkedIn](https://linkedin.com/in/burt-gardner) ·
[Résumé (PDF)](https://github.com/bgard68/bgard68/blob/main/Burt_Gardner_Resume.pdf)
