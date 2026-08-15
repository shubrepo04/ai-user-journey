# Metric Reference

Every metric in the journey map, in one table, for direct use in a PRD or an analytics spec.

| Stage | Metric | What it tells you |
|---|---|---|
| 1. Problem Recognition | Entry rate: percentage of active users who initiate an AI interaction per session | Whether the feature is discoverable and reached for |
| 1. Problem Recognition | Time from product open to first AI engagement | Friction between arriving and starting |
| 1. Problem Recognition | Intent detection accuracy before explicit input | Quality of pre prompt context inference |
| 2. Intent Expression | Prompt success rate: first prompt leads to an output the user uses | Whether users can express intent in one attempt |
| 2. Intent Expression | Prompt abandonment rate: types something then deletes and closes | Hidden failure that never reaches the model |
| 2. Intent Expression | Time from feature open to first submission | Cost of composing an intent |
| 3. Context Building | Context completeness score before generation | Whether the system has enough to answer |
| 3. Context Building | Average number of context additions before first generation | User effort spent supplying background |
| 3. Context Building | Clarifying question acceptance rate | Whether clarifying questions help or annoy |
| 4. Generation | Generation latency: P50 and P99 time to first token and completion | The peak anxiety window |
| 4. Generation | Automated quality score from eval suite on output samples | Output quality independent of user reaction |
| 4. Generation | Output length aligned to task complexity | Over generation and under generation |
| 5. Evaluation | Acceptance rate: output used without significant editing | The core usefulness signal |
| 5. Evaluation | Time spent on output before first action | Review burden |
| 5. Evaluation | Implicit signals: scroll completion, copy rate, application rate | Satisfaction without asking |
| 6. Correction | Regeneration frequency: how often users ask for a second attempt | First attempt failure rate |
| 6. Correction | Correction type distribution: structural, factual, tonal, format | Where the system is actually weak |
| 6. Correction | Correction to acceptance conversion rate | Whether recovery works |
| 7. Trust Formation | Trust proxy: reduction in edit rate over time for the same user | Trust made measurable |
| 7. Trust Formation | Feature return rate within 7 days of first successful use | Whether one good outcome brings them back |
| 7. Trust Formation | Review time on output decreasing as tenure increases | Scrutiny relaxing as reliability is proven |
| 8. Habit Loop | DAU to WAU ratio: active days per week | Habit strength |
| 8. Habit Loop | Session frequency and average tasks per session | Depth of routine use |
| 8. Habit Loop | Workflow integration depth: starts tasks in the AI versus brings tasks to it | Whether the AI is the workflow or an add on |
| 9. Advocacy | Referral rate: new users from a share or recommendation | Organic growth |
| 9. Advocacy | Shared output open rate | Whether shares convert |
| 9. Advocacy | Viral coefficient within organisations | Land and expand inside accounts |

## Notes on use

The right hand column is interpretation, not part of the source artifact.

No measured values are published in this repository. Any number placed against these metrics must come from a real instrumented product.
