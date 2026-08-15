# The AI User Journey

**A nine stage, four lane map of how a user moves from an unsolved problem to advocating for an AI product, and what a product manager measures at each stage.**

## Read this in 60 seconds

- **What it is:** a journey map covering 9 stages, each broken into what the user thinks, what the user does, what the AI system must do, and what the PM measures.
- **What it proves:** that AI product work is a lifecycle problem, not a generation problem. Six of the nine stages happen before or after the model produces a token.
- **What it gives you:** 27 named metrics tied to specific stages, ready to drop into a PRD or an analytics spec.

Full map: [`docs/journey-map.md`](docs/journey-map.md)
Metric table: [`docs/metric-reference.md`](docs/metric-reference.md)

---

## Problem

Most AI product roadmaps optimise the generation step. Latency, model choice, prompt quality, output formatting.

Generation is one stage out of nine. A product can generate excellent output and still fail, because the user could not express intent, could not supply context, could not correct a near miss, or never came back after the first good result.

The failure modes outside generation are the ones that are least instrumented and least owned.

## User

The primary user of this artifact is a product manager, designer, or engineer who owns an AI feature and needs to answer three questions:

- Where in the lifecycle is our product actually losing people
- What should the AI system be doing at that specific point
- What number tells us whether it is working

## Product thesis

If you can name the stage, you can name the system behaviour, and if you can name the system behaviour, you can name the metric. Mapping the three together in one grid turns vague AI quality complaints into a specific, instrumentable product problem.

## Structure

Nine stages:

| Stage | User frame | Emotional state |
|---|---|---|
| 1. Problem Recognition | "I need help with X" | 😤 |
| 2. Intent Expression | "Here's what I want" | 🤔 |
| 3. Context Building | "AI needs more info" | 🧩 |
| 4. Generation | "Show me a solution" | ⏳ |
| 5. Evaluation | "Is this useful?" | 🔍 |
| 6. Correction | "Not exactly..." | 😕 |
| 7. Trust Formation | "I can rely on this" | 😌 |
| 8. Habit Loop | "This saves me time" | 😊 |
| 9. Advocacy | "Others should use this" | 🤩 |

Four lanes per stage: User Thinking, User Action, AI System, PM Metrics.

## How to use it

**As a discovery tool.** Walk a real user session through the nine stages and mark where it broke. The stage where it broke tells you which lane to fix.

**As a metric spec.** The PM Metrics lane gives 27 candidate metrics with the stage they belong to. Pick the three that match your current bottleneck rather than instrumenting all of them.

**As an architecture prompt.** The AI System lane states what the system must do at each stage. Any stage where your system does nothing is a deliberate product decision or an accidental gap. This map makes you name which.

## Product decisions

**Four lanes, not three.** Separating User Thinking from User Action matters because AI products fail most often in the gap between the two. A user who abandons a prompt before submitting produces no action data at all, so the thinking lane is where the hypothesis lives and the action lane is where it gets tested.

**An explicit Correction stage.** Correction is usually folded into evaluation. Separating it makes recovery a first class product surface with its own metrics, because the difference between a product users tolerate and one they trust is how cheaply a near miss becomes a hit.

**An emotional arc.** Peak anxiety sits at Generation, not at failure. That places latency and streaming behaviour in the emotional design conversation rather than only the engineering one.

**Trust and Habit are separate stages.** Trust is a change in scrutiny. Habit is a change in default behaviour. They are measured differently: edit rate decline versus active days per week.

## Trade-offs

**Linear stages, non linear reality.** Real users skip stages, loop between 4 and 6 repeatedly, and reach advocacy without ever hitting habit. The linear form is chosen for diagnostic clarity, at the cost of fidelity.

**Generic across use cases.** The map does not distinguish a coding assistant from a support agent from a document tool. That makes it reusable and makes it shallow on any single one. It is a starting grid, not a finished spec.

**Metrics are named, not defined.** Each metric has a name and a stage, not a calculation. Definitions are product specific and belong in your analytics spec.

## Failure modes this map exposes

- **Silent abandonment at stage 2.** Users who compose and delete never appear in prompt volume.
- **Context burden at stage 3.** Re explaining known facts is friction the system should have absorbed.
- **Anxiety at stage 4.** The wait is the product experience, not a gap before it.
- **Undetected rejection at stage 5.** Output that is read and discarded looks identical to output that is read and used unless implicit signals are captured.
- **Expression gap at stage 6.** Users know what is wrong but not how to say it. That is a system design problem, not a user problem.
- **Trust plateau at stage 7.** Scrutiny that never relaxes means reliability was never proven.

## Metrics

27 metrics across 9 stages. See [`docs/metric-reference.md`](docs/metric-reference.md).

## Limits

This repository is a framework artifact, not a running system. It contains no measured data, no benchmark results, and no production numbers. Metrics are specified, not observed.

## Next iteration

- A worked application of the map to one named AI product
- Per stage instrumentation guidance: event names, properties, sampling
- A variant for agentic products where the system acts between stages rather than only responding

## Licence

MIT. See [`LICENSE`](LICENSE).

## Author

**Shubham Shukla** — [LinkedIn](https://www.linkedin.com/in/aiproductshubham/) · [GitHub](https://github.com/shubrepo04)
