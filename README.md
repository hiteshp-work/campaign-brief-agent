# Campaign Brief Agent

An AI agent that turns a raw campaign idea into a **decision-ready demand generation launch brief** — with an honest go/kill verdict, ICP fit check, messaging angles, channel mix with budget allocation, timeline, KPIs, and risks.

Built by a B2B SaaS growth marketer as a working demonstration of how AI agents compress campaign planning from days of back-and-forth into a single rigorous pass — without losing senior-level judgment.

## What it does

Give it a campaign idea (even a half-formed one) and it returns a complete launch brief:

1. **Verdict first** — GO / REFINE / KILL, with reasoning. Weak ideas get reshaped or killed, not dressed up.
2. **ICP fit check** — scores the idea against the target buyer on role, segment, triggers, and reachability. Mismatches spelled out.
3. **Messaging** — one-line value prop, 3 distinct creative angles with headlines and CTAs, and the one objection the copy must beat.
4. **Channel mix & budget** — every dollar allocated across channels with benchmark CPL ranges and the strategic reason each channel earned its place.
5. **Funnel & assets** — everything that must be built, and who owns it (marketing vs. sales vs. ops).
6. **Timeline** — build → launch & optimize → evaluate, with slip risks called out.
7. **KPIs & measurement** — leading indicators, lagging outcomes, and the attribution model.
8. **Risks & mitigations** — top 3 risks, each with a concrete mitigation.
9. **Next decision** — the single thing the marketer must confirm to greenlight it.

Every number is labeled as a benchmark, an assumption, or a supplied fact. No invented precision.

## Example

**Input:**

> Launch an ABM campaign targeting Heads of L&D and Ops at mid-market Canadian credit unions for our new AI-powered staff training module. Budget $40K, 8 weeks, goal: 20 sales-accepted opportunities.

**Output (excerpt):**

> **Verdict:** GO with a refinement — narrow the ICP to credit unions with 200–2,000 employees and lead with the compliance angle; the generic "AI training" pitch is too broad for this budget.
>
> | Channel | Share | $ | Funnel role |
> |---|---|---|---|
> | LinkedIn Ads (ABM, matched audiences) | 45% | $18,000 | Demand capture |
> | Targeted email (1st-party + intent) | 20% | $8,000 | Demand capture |
> | Webinar (compliance readiness) | 15% | $6,000 | Mid-funnel conversion |
> | Retargeting | 10% | $4,000 | Funnel acceleration |
> | Content syndication | 10% | $4,000 | Top-funnel fill |

See the [full example brief](references/example-brief.md).

## How it works

This is a **prompt-based agent** — no code, no dependencies. The agent's behavior is defined in [`SKILL.md`](SKILL.md):

- **Workflow** — the 10-step planning process the agent follows on every run
- **Output Contract** — what a finished brief must contain (verdict first, labeled numbers, scannable in 3 minutes)
- **Operating Rules** — honesty over enthusiasm, never invent benchmarks, one campaign per brief

Supporting files live in `references/`:

| File | Purpose |
|---|---|
| `brief-template.md` | The exact markdown structure of every brief |
| `example-brief.md` | A full example brief produced by the agent |

## How to use it

**With Muse / Claude:** drop this repo's `SKILL.md` into your skills directory (or paste it as a system prompt into any capable LLM), then just say:

> Brief my campaign: [your idea, budget, timeline]

The agent asks at most one round of questions for facts only you'd know (real budget, hard deadline, must-use channels), fills the rest with B2B SaaS defaults, and labels every assumption.

## Design principles

- **One job, done well.** Narrow agents beat generalists — this agent briefs campaigns and nothing else.
- **Judgment is the feature.** The verdict and the ICP fit check are what make this more than a template filler.
- **Labeled numbers.** Benchmarks are directional; the brief says so every time.
- **Terse by default.** A VP should grasp the whole brief in 3 minutes.

## Roadmap

Ideas for sibling agents in this series:

- **Account research agent** — enrich target accounts with firmographics, trigger events, and outreach angles
- **Content repurposing agent** — turn one core asset (webinar, report) into campaign-ready emails, ads, and social copy

## Author

**Hitesh Patel** — Senior B2B SaaS growth marketing leader (demand generation, ABM, attribution, paid media, CRO), based in Toronto.

## License

MIT — see [LICENSE](LICENSE).
