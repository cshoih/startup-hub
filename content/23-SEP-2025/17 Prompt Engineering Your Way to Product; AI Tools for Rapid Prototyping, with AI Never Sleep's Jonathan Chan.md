## Title: Prompt Engineering Your Way to Product: AI Tools for Rapid Prototyping, with AI Never Sleep’s Jonathan Chan 

### Session context

- Format: 80% practical demo + 20% concepts; live Q&A
- Host: Louisa (Startmate); Speaker: Jonathan Chan (AI Never Sleeps; ex-BCG, Westpac strategy, SocietyOne → MoneyMe)
- https://www.linkedin.com/in/jonathanchan/
- Audience: Non-technical founders building technical products; goal = ship MVPs with AI-assisted “vibe coding” while staying safe for prod

### Why prompt engineering matters

- Quality in = quality out: vague prompts produce random, inconsistent outputs
- Prompting > syntax for non-devs: you can ship full web/mobile MVPs with AI + guardrails
- Shift: from waterfall or even agile → iterative AI loops guided by precise instructions

### Core prompt framework: ICE (Identity, Command, Examples)

|Element|How to do it|Example (condensed)|
|---|---|---|
|Identity|Assign expertise, persona, and constraints to the model|“You are an award-winning food stylist and pro photographer…”|
|Command|State the task and exact specs (tech, style, lens, lighting, API, auth)|“Generate a high-res image… on a wooden board… 50mm, soft natural light…”|
|Examples|Show target outputs, formats, and non-goals; provide references|“Match Donna Hay magazine style; avoid plastic/CGI look; output JSON schema X”|

Guidelines

- Be specific; de-ambiguate requirements; avoid “build me an awesome app”
- One task at a time to prevent collateral breakage
- Use AI to co-write your prompts; iterate to add missing constraints

### Tooling landscape (start right → move left as you mature)

|Category|Tools (examples)|Use when|
|---|---|---|
|Web-app builders|Lovable, Replicate/Refine, v0, v0.dev, Vercel v0|Fast front-end MVPs, quick demos|
|Mobile builders|VibeCode.app, Supernova|iOS/Android MVPs; simple native flows|
|IDEs (AI-native)|Cursor, Claude Code (init), Windsurf|E2E coding, refactors, tests, deployment|
|CLIs|Codex CLI, OpenAI/Anthropic SDKs|Experienced users; pipelines/agents|
|Hosting/deploy|Vercel, Railway, Fly.io, Render|Simple, scalable hosting pre-AWS/Azure|
|Design/wireframing|tldraw, Figma|Wireframes → screenshots for AI-to-UI tools|
|Testing|PyTest, Playwright/Cypress, BrowserStack|Automated tests, cross-browser/device checks|

Practical note

- Web builders are great for v0; migrate to GitHub + IDE for prod hardening and integrations

### AI-driven software workflow (lightweight SDLC)

|Phase|What to do|Tools|
|---|---|---|
|Plan & design|Define user stories, flows, data model, auth; select frameworks/libraries; draw wireframes|ChatGPT/Claude, tldraw/Figma|
|Scaffold|Generate front-end from wireframe screenshot; stub backend; pick UI kit|v0/Lovable → GitHub|
|Develop|Move to Cursor; generate project rules; small, atomic changes; add APIs/auth/db|Cursor (rules), Claude Code|
|Test|Unit/integration tests; security checks; cross-browser/device|PyTest/Playwright, BrowserStack|
|Deploy|CI/CD; environment separators; logs/alerts; rollback plan|Vercel/Railway + GitHub|
|Harden|Guardrails, secrets management, rate limits; code reviews; performance|Cursor Ask/Agent, dotenv, Sentry|

### Guardrails and safety (avoid “vibe chaos”)

- Markdown rulebook in repo: “Do NOT drop/alter production tables; never delete customer data; require migrations”
- Cursor rules: auto-generate with “/generate cursor rules,” then customize (architecture, styling, deployment, data)
- Claude Code init: “/init” reads Cursor rules; keep them source-of-truth
- Secrets: use env vars, never hardcode; rotate keys; least-privilege DB users
- Agent modes: prefer Ask mode; use Agent/Background only with Git branching and CI checks
- Logging/monitoring: add Sentry/Logtail early; basic health checks
- Tests: require green tests before merge; include auth, payments, and PII paths

### Prompt patterns that work (coding)

- Scaffolding
    - “You are a senior Next.js + Prisma engineer. Create a minimal multi-tenant SaaS scaffold with magic.link auth, Stripe billing, dashboard with KPI cards, and audit logging. Use Tailwind + shadcn. Generate ERD for Postgres via Prisma schema.”
- Small diffs
    - “Implement optimistic UI for create/edit on Tasks page; update tests; do not touch schema or billing code.”
- API auth fixes
    - “Diagnose OAuth2 PKCE failure with provider X on mobile; list hypotheses; propose logs; patch with minimal changes.”
- Testing
    - “Write Playwright tests for onboarding golden path; stub Stripe; add CI workflow on pull_request targeting main.”
- Security/perf
    - “Perform lightweight security review; list top 5 risks; patch CSRF, add rate limiting to auth routes; explain changes.”

### Common pitfalls to avoid

- Vague prompts; multi-task prompts; skipping tests; hardcoded secrets
- Overreliance on web builders; never migrating to version control/IDEs
- Deploying without basic monitoring/rollback
- Letting agents run without repo guardrails

### Benchmarks and pacing

|Area|Practical bar|
|---|---|
|Time-to-MVP|3–10 days for simple web; 5–14 days for basic mobile (app store review may be longer)|
|Prompting|3–5 iterations to reach spec-level clarity per feature|
|Testing|Golden path automated in week 1; smoke tests on every deploy|
|Deploy|Staging by day 3–5; prod by week 2 with logs and rollback|

### Selected Q&A highlights

|Topic|Takeaway|
|---|---|
|Claude Code vs Codex CLI|Claude Code = “Mercedes” experience; Codex = “Toyota” utility; both evolving|
|Best front-end/back-end stacks|Choose community-backed frameworks; ask LLM for pros/cons given your requirements|
|Architecting with LLMs|Use LLMs to brainstorm options; you still decide; capture decisions in rules/README|
|Cursor safety|Use repo rulebooks; turn on Ask mode; branch before big changes; protect DBs via roles|
|Non-web ML scripts|Cursor can help build/ship Python ML (clean, train, infer) beyond web apps|
|Deployment for non-devs|Railway/Vercel simplest; move to AWS/Azure later|

### 8-week execution template (fill this in)

|Track|Baseline (now)|2-week goal|Weekly target|Success criteria|
|---|---|---|---|---|
|Design|Loose idea, no flows|Wireframes (tldraw/Figma), user stories, ERD|1 design-review loop/week|Golden path defined|
|Build|0|v0 front-end + auth + stub backend|2–3 small diffs/day via Cursor|Staging live with logs|
|Test|None|Golden path tests (Playwright/PyTest)|Add tests per feature|CI green pre-merge|
|Deploy|None|Staging on Vercel/Railway; prod behind flag|One deploy/week|Rollback + monitoring configured|
|Safety|No guardrails|Repo rules + .md guardrails + secrets in .env|Weekly security/perf pass|No secrets in code; rate limits enabled|

### Practical metrics you can choose

- Engineering: cycle time per change; % PRs with tests; error rate; TTI/LCP (web)
- Safety: incidents; time-to-rollback; secrets exposure = 0
- Delivery: days to staging/prod; % green CI runs; flaky test count
- Product: activation of golden path; crash-free sessions (mobile)

### Workshop logistics and follow-ups

|Item|Details|
|---|---|
|Slides/resources|AI Never Sleeps newsletter; “vibe coding” tool lists; Cursor rule templates|
|Connect|LinkedIn (Jonathan Chan); Office Hours via Startmate|
|Try next|Cursor (free), Vercel/Railway deploys, v0/lovable for scaffolding|

### Your next 5 actions

1. Draft wireframes in tldraw/Figma; write user stories and data model
2. Generate front-end with v0/Lovable; push to GitHub
3. Open in Cursor; “/generate cursor rules”; add repo guardrails markdown
4. Implement golden path + auth + logging; write Playwright/PyTest basics
5. Deploy to Vercel/Railway; add monitoring and rollback; iterate with small prompts and tests
