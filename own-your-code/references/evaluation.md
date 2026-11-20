# Evaluation rubric — Own Your Code v0.1

The rubric evaluates **demonstrated comprehension**, not code authorship, confidence, or professional developer status.

Score each dimension 0–3 **only when the learner's response supplies evidence**.

| Dimension | 0 | 1 | 2 | 3 |
| --- | --- | --- | --- | --- |
| Functional explanation | Cannot explain what happens | Can name an actor or one step | Can explain the main sequence accurately | Can explain the sequence with conditions and error paths |
| System relationships | Cannot locate roles | Names one module/service | Connects UI, service, and backend correctly | Traces responsibility and data flow with grounded code references |
| Change impact | Cannot predict impacts | Makes an unsupported guess | Predicts a plausible consequence with rationale | Predicts consequences, boundaries, and an appropriate verification check |

## Rules
1. Record which learner statements support each score. A high score requires an actual response, not the fact that the agent explained something.
2. If not assessable, write **N/A**; never replace a missing answer with 0.
3. Give the **same or equivalently difficult prompt** for before/after assessment.
4. Treat baseline as the learner's hypothesis; the source code is the basis for checking it.
5. Cross-check real behavior with tests/logs/deployed code if claiming runtime truth.
6. Compare with ordinary agent explanations using a different, similarly complex feature or a new session, so the specialized skill does not contaminate the control.

## Completion template

- Feature:
- Repository revision:
- Initial user hypothesis:
- Baseline: function __ / 3, relationships __ / 3, impact __ / 3 (or N/A)
- Follow-up response (learner's words):
- After: function __ / 3, relationships __ / 3, impact __ / 3 (or N/A)
- What was newly understood:
- What remains unverified:
- One next learning exercise:
