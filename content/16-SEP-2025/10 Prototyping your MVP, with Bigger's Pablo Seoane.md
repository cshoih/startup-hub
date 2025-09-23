## Title: Prototyping your MVP, with Bigger’s Pablo Seoane

### Session context
- Format: Talk + live demo + Q&A
- Host: Louisa (Startmate)
- Speaker: Pablo Seoane (Co-founder & CEO, Bigger)
- https://www.linkedin.com/in/p-seoane/
- Audience: Launch Club founders (validation → POC → MVP build)
- Objective: How to scope, prototype, and build an MVP fast; practical frameworks and tech stack tips
- About the speaker
  - 15+ years across corporate, startups and software
  - Founded Bigger (matches founders with developers; helped 500+ startups)
  - Previously GM at a large tech company; founded subscription e‑commerce “Dating in a Box”
  - Non-technical → learned to ship software with teams; shares open-source scoping framework

### Why prototype (and what counts)
- You only learn “does it work?” when users try it
- Prototyping reduces time-to-learning by cutting non-core features and shipping earlier
- Early adopters = people desperate for the problem who will try a non-perfect solution

### MVP mindset: skateboard → bike → motorbike → car
| Principle                   | Why it matters                                                                 |
|----------------------------|---------------------------------------------------------------------------------|
| Start with a “skateboard”  | Solve the core job with the absolute minimum; get feedback immediately         |
| Iterate in public          | Each step adds comfort/speed only after user feedback                          |
| Evidence over assumptions  | Validate problem, then demand, then build MVP for early users                  |

Examples
- Airbnb v1: no payments, no map, conference-only
- Stripe v1: simple site; founders handled paperwork manually
- Dating in a Box: Wix landing page + Kmart games → bespoke boxes later
- Together (remote team bonding): PPT slide + roulette link → lightweight activity → app with Slack/Miro

### Scoping framework (open-source) Pablo uses with 500+ startups
1) Problem dump → refine to one crisp problem statement
2) Personas
   - Buyer/admin (e.g., HR), facilitator/leader, participant/user
3) Golden path (end-to-end steps)
   - Login → add org/users → select experience → invite → run → collect feedback
4) User story mapping (what’s needed per step)
   - E.g., catalog, Miro/Slack integrations, invitations, analytics
5) Prioritise with MoSCoW
   - Must/Should/Could/Won’t for now; be ruthless on scope
6) Low‑fi mockups
   - Sketch/Canva/Figma; communicate flows and components without over-designing

YC-aligned build flow
- Validate problem → validate demand (landing + waitlist/preorder) → POC (manual OK) → MVP with early users → soft launch with paying users

### What not to do vs what to do
| Don’t do                                              | Do instead                                                                 |
|-------------------------------------------------------|-----------------------------------------------------------------------------|
| 20-feature “MVPs”                                     | Cut to the smallest path that solves the job                               |
| Months of stealth building                            | Ship in weeks; use landing tests and manual delivery                       |
| Premature brand/perfection                            | Learn with scrappy POCs; quality rises with each iteration                 |
| Avoid talking to users                                 | Call early buyers; observe activation; capture objections verbatim         |

### Build options (non-technical founder)
| Path                       | Pros                                         | Cons                                          | When to choose                                 |
|---------------------------|----------------------------------------------|-----------------------------------------------|------------------------------------------------|
| Do it yourself (no/low-code, AI) | Low cost; fast; retains equity               | Time-consuming; limits/bugs                    | POC → early MVP; budget-constrained            |
| Outsource (agency/contractor)    | Faster start; senior oversight possible       | Expensive; vendor selection risk               | Need working MVP quickly; no tech lead yet     |
| Hire tech co-founder/team        | Deep expertise; long-term advantage           | Hard to find pre-traction; opportunity cost    | After early traction or if domain is complex   |

Guidance
- If non-technical and pre-traction: bootstrap POC, then outsource a tight MVP; later in-house or CTO
- Don’t burn cycles managing a dev you can’t manage; stay focused on users and distribution

### Practical tech stack recommendations
- No/low-code for MVPs
  - Softr + Airtable/Google Sheets for data; Make.com for automations
  - Internal tools: Oracle APEX (free) for back-office workflows
  - Bubble: powerful, but steeper for non-tech; if you’ll hire a Bubble dev, consider going “proper code” instead
- AI-assisted builders (for POCs → code you can hand off)
  - Lovable, Replicate (preferred in Pablo’s tests), Bolt, Manus, Genspark
  - Expect bugs/hallucinations; debug with a human dev when stuck
- Prototyping/UI
  - Google Stitch (front-end prototyping; free), Figma, Figma Make (high-fidelity UI from prompts), Framer (site with optimized templates)
- Integrations he used
  - Slack for team invites; Miro for collaborative boards; plan Teams later

### Quality and engineering hygiene (even for MVPs)
- Ask: what’s your testing approach? Don’t ship to production without basic tests
- Have rollback/monitoring; simple logs and alerts beat blind shipping
- Story: a “3‑month plan” bug charged customers 3×; testing would have caught it

### Services-as-Software (Do things that don’t scale)
- Deliver value manually with your own lightweight tooling; users don’t need to see your backend
- Great to validate workflows, pricing, and objections before user-facing app is “ready”

### Selected Q&A highlights
| Topic                                  | Takeaway                                                                                                     |
|----------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Tech vs business co-founder            | You need both “build” and “sell”; solo is OK to start, but aim to complement skills                          |
| Outsource vs internal                  | Pre-traction: outsource a tight MVP while you find users; in-house/CTO later                                 |
| Picking agencies                       | Offshore for budget; use a due-diligence checklist (Pablo to share)                                          |
| No/low-code/AI framework               | Prompting quality first; iterate prompts in a free LLM then use paid tools; bring a dev to debug             |
| Real-time mobile app via no-code       | Start with Softr + AI tools (Replicate, Lovable); consider POC without an app; only hire when blocked        |
| Bubble stance                          | Not “anti-Bubble”: just note learning curve; if paying a Bubble dev, consider going to code for scale        |
| Tool overload                          | Pick one and ship; don’t get stuck comparing tools                                                            |
| Extra tools                            | Figma Make praised for higher-fidelity outputs; Framer for sites; Stitch free for quick UI                    |

### Benchmarks and pacing
- Ship POC in days; MVP in weeks
- Early-stage: optimize time-to-learning, not completeness
- Validate with actual use and, where possible, paid pilots or trials

### MVP action template (fill this in)
| Area     | Baseline (now)                              | 2-week goal                                      | Weekly target                              | Success criteria                                  |
|----------|---------------------------------------------|--------------------------------------------------|---------------------------------------------|---------------------------------------------------|
| Problem  | Clear JTBD + personas?                      | One crisp problem statement + golden path        | 5–10 user calls validating steps            | Users agree steps lead to desired outcome         |
| Product  | POC status                                  | Clickable mock + POC (manual OK)                 | 1 build + 1 test + 1 feedback loop          | Users complete core flow; fewer manual patches    |
| Demand   | Landing/waitlist/preorders                  | Simple page + 2 value prop variants              | 2–3 creative tests; 10–20 calls             | CTR/CR to pre-order/booking hit target            |
| Tech     | Tooling choice                              | Decide stack (Softr/Make/AI) + integrations      | Ship one integration (e.g., Slack or Miro)  | Integration supports end-to-end “golden path”     |

### Practical metrics you can choose
- Activation: % who complete the core action within first 7 days
- Usage: DAU/WAU for the core experience; repeat task completion
- Retention: Day‑7 and Week‑4 return rates; cohort curves
- Love/value: “Very disappointed if removed” %, qualitative quotes
- Demand: Preorders/paid pilots/LOIs; MRR; # paying customers

### Prototyping playbook
| Step                 | Tactic                                                                                  |
|---------------------|------------------------------------------------------------------------------------------|
| Demand test         | Framer/Figma Make/Notion + Stripe checkout/preorder; run small ad tests                  |
| POC                 | Manual delivery via Google Slides + Miro/Slack; services-as-software backend              |
| MVP                 | Softr + Airtable + Make; one integration (Slack/Miro); basic analytics & feedback loop   |
| Iterate             | Weekly: change → ship → observe → talk → decide                                          |

### Action items
| # | Action                                                                                         |
|---|-------------------------------------------------------------------------------------------------|
| 1 | Write the one-line problem statement and identify buyer, facilitator, participant personas      |
| 2 | Map the golden path; create a user story map; run MoSCoW to cut scope                           |
| 3 | Draft low-fi mockups (Figma/Stitch/Figma Make); choose one stack to start                       |
| 4 | Build a manual POC this week; schedule 10 user sessions; instrument feedback                    |
| 5 | Ship a 2–3 screen “good but small” MVP in 2–3 weeks; integrate one key tool (Slack/Miro)        |

### Workshop logistics and follow-ups
- Pablo to share:
  - Open-source Miro/Mural “design sprint” scoping framework
  - Agency/vendor due-diligence checklist
  - AI tooling session video from Bigger’s tech lead
- Tools mentioned: Softr, Airtable/Sheets, Make.com, Oracle APEX, Lovable, Replicate, Bolt, Manus, Genspark, Google Stitch, Figma, Figma Make, Framer, Slack, Miro, Microsoft Teams (later)
- Connect with Pablo on LinkedIn (“Pablo Bigger”) for resources and questions