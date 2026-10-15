## Hi, I'm Olga 👋

**Software Engineer (C#/.NET)** with 12+ years of building backend services, enterprise systems, desktop tools and automation. I care about clean architecture, tests that actually catch bugs, and software that is safe to run in production.

🌍 Open to **remote** roles · 📫 [olgaantonikova@gmail.com](mailto:olgaantonikova@gmail.com) · 💼 [LinkedIn](https://www.linkedin.com/in/olga-antonikova-05385b162)

### Tech stack

| Area | Tools |
|---|---|
| Backend | C#, .NET 8, ASP.NET Core (minimal APIs, controllers), EF Core, LINQ, REST, DI, Clean Architecture, DDD |
| Frontend & desktop | Blazor WebAssembly, WPF (MVVM), vanilla JS, Telegram Mini Apps |
| Data | PostgreSQL, Oracle (PL/SQL, ODP.NET), MySQL, SQLite |
| Testing | xUnit, `WebApplicationFactory`, SpecFlow, test automation frameworks, mutation testing |
| DevOps | Docker, GitHub Actions, Linux/systemd, DigitalOcean |
| Integrations & AI | OpenAI API, ML.NET, Telegram Bot API, external REST APIs, Claude Code |

### Featured projects

| Project | What it shows |
|---|---|
| [**exchange-miniapp-dotnet**](https://github.com/OlgaAntonikova/exchange-miniapp-dotnet) | Telegram Mini App for a currency-exchange office: ASP.NET Core 10, EF Core, PostgreSQL, Docker |
| [**shared-balance**](https://github.com/OlgaAntonikova/shared-balance) | Shared family balance used in production; Telegram `initData` signature check, JWT, ASP.NET Core 8, SQLite |
| [**xml-oracle-loader**](https://github.com/OlgaAntonikova/xml-oracle-loader) | WPF/MVVM tool that validates 1C:Enterprise XML exports and loads them into Oracle in one transaction (ODP.NET array binding) |
| [**coloringbook**](https://github.com/OlgaAntonikova/coloringbook) | Seeded procedural mandala generator with live preview and vector PDF export; ASP.NET Core + Blazor WebAssembly, Docker |

Each repository has a README with screenshots, tests and CI.

### How I work with AI: Claude Code

I use **Claude Code** every day as a pair engineer, and I treat it like a team member who needs a clear process, not like autocomplete:

- **Spec first, test first.** The task is written down before code. Tests are derived from it, and the agent implements against them.
- **Adversarial review.** A separate reviewer agent with a clean context checks every change before it is committed. It does not trust the author's summary and re-runs the build and the tests.
- **Proof, not claims.** Bug fixes come with a test that fails on the old code. Security issues are reproduced before they are fixed.

The four projects above were brought to their current state this way. The work included secret rotation, git history cleanup, a path-traversal fix, vector PDF export, an MVVM rewrite, end-to-end checks against a real Oracle in Docker, and CI.

#### dev-factory

**dev-factory** is my own Claude Code plugin that turns this process into code. A new project becomes a repository, the plugin and a spec. It has three parts:

- **Skills**: how to write a spec, how to run the test-first build loop, how to review.
- **Agents**: an adversarial `reviewer`, a cheap `scout` for codebase exploration, and a `verifier` that reproduces claims instead of believing them.
- **Hooks**: rules the agent cannot talk itself out of, because they are code. Examples:
  - only work branches and pull requests, never pushing to `main`;
  - no ad-hoc package installs;
  - English-only repository artifacts;
  - a session cannot finish while the project's build and test commands are undeclared or failing.

Every guard is proven by mutation testing. The plugin has 207 tests. dev-factory is currently private; I am happy to walk through it in an interview.

### Languages

English (B1/B2) · Serbian (B2) · Russian (native)
