# EV Gate Rulebook

Last Updated: 2026-05-13

---

# Conflict Priority Order

1. Consumer clarity
2. Consumer safety
3. Deterministic consistency
4. UX simplicity
5. Completion speed
6. Visual aesthetics

---

# UX Rules

## UX-001

RULE ID: UX-001

CATEGORY: Question Design

TYPE: Hard Rule

RULE:
Every question must be understandable by a non-EV owner within 3 seconds without additional explanation.

RATIONALE:
Reduces abandonment and prevents industry-assumption bias.

EXAMPLE:
Good:
"Where would the vehicle normally be parked overnight?"

Bad:
"Do you have access to residential EV charging infrastructure?"

CONFLICTS:
None

LAST UPDATED:
2026-05-13

---

## UX-002

RULE ID: UX-002

CATEGORY: Question Flow

TYPE: Hard Rule

RULE:
Only one primary question may appear on screen at a time.

RATIONALE:
Reduces cognitive overload and increases completion clarity.

EXAMPLE:
Good:
Single question with 4–6 selectable answers.

Bad:
Multi-section survey pages with stacked questions.

CONFLICTS:
None

LAST UPDATED:
2026-05-13

---

## UX-003

RULE ID: UX-003

CATEGORY: Question Design

TYPE: Hard Rule

RULE:
Each question must have a single identifiable purpose.

RATIONALE:
Questions that attempt to measure multiple variables simultaneously create ambiguity and weaken deterministic logic.

EXAMPLE:
Bad:
"Do you own your home and have charging access?"

Good:
Separate ownership and charging practicality into different logic checks.

CONFLICTS:
None

LAST UPDATED:
2026-05-13

---

## UX-004

RULE ID: UX-004

CATEGORY: Cognitive Load

TYPE: Hard Rule

RULE:
Questions must avoid industry jargon, technical EV terminology, or assumptions of prior EV knowledge.

RATIONALE:
The engine is designed primarily for non-EV owners evaluating viability.

EXAMPLE:
Bad:
"Do you anticipate DC rapid charging dependency?"

Good:
"Would you regularly rely on public charging?"

CONFLICTS:
None

LAST UPDATED:
2026-05-13

---

## UX-005

RULE ID: UX-005

CATEGORY: Question Context

TYPE: Hard Rule

RULE:
Any question that may not have an obvious connection to EV viability must include a short supporting sentence explaining why it is being asked.

RATIONALE:
Users should understand the relevance of each question without needing EV knowledge.

EXAMPLE:
Question:
"Where would the vehicle normally be parked overnight?"

Supporting text:
"This helps assess how practical regular EV charging may be for your routine."

CONFLICTS:
None

LAST UPDATED:
2026-05-13

---

## UX-006

RULE ID: UX-006

CATEGORY: Cognitive Load

TYPE: Hard Rule

RULE:
Early-stage questions should prioritise behavioural patterns over precise numerical inputs where possible.

RATIONALE:
Approximate behavioural questions reduce hesitation and improve response confidence for non-technical users.

EXAMPLE:
Good:
"Mostly short local trips"

Bad:
"Estimate your average weekly mileage."

CONFLICTS:
May conflict with later-stage precision scoring requirements.

LAST UPDATED:
2026-05-13

---

## UX-007

RULE ID: UX-007

CATEGORY: Assessment Scope

TYPE: Hard Rule

RULE:
The engine should aim to achieve high-confidence viability assessment using the minimum number of questions necessary.

RATIONALE:
Shorter assessments improve completion rates, reduce fatigue, and increase perceived confidence in the engine’s logic.

EXAMPLE:
7 high-impact questions are preferred over 20 low-impact questions.

CONFLICTS:
May conflict with highly granular scoring ambitions.

LAST UPDATED:
2026-05-13

---

## UX-008

RULE ID: UX-008

CATEGORY: Question Clarity

TYPE: Hard Rule

RULE:
Questions should prioritise concrete real-world scenarios over abstract hypothetical situations wherever possible.

RATIONALE:
Abstract hypothetical wording increases interpretation ambiguity and weakens response confidence.

EXAMPLE:
Good:
"Would the EV likely be your only regularly available vehicle?"

Bad:
"If charging became temporarily inconvenient, how disruptive would that realistically be?"

CONFLICTS:
None

LAST UPDATED:
2026-05-13

------

## UX-009

RULE ID: UX-009

CATEGORY: Question Architecture

TYPE: Hard Rule

RULE:
Questions should feel operationally practical and immediately understandable without requiring hypothetical interpretation.

RATIONALE:
Users should understand the purpose of a question instantly without needing examples or clarification.

EXAMPLE:
Good:
"Would the EV likely be your only regularly available vehicle?"

Bad:
"If charging became temporarily inconvenient, how disruptive would that realistically be?"

CONFLICTS:
May reduce theoretical modelling flexibility.

LAST UPDATED:
2026-05-13

---

## ARCH-001

RULE ID: ARCH-001

CATEGORY: Project Architecture

TYPE: Hard Rule

RULE:
The initial EV Gate prototype should remain a static deterministic implementation using plain HTML, CSS, and JavaScript without frameworks or backend dependencies.

RATIONALE:
A lightweight architecture improves iteration speed, portability, debugging simplicity, deployment speed, and logic transparency during early-stage development.

EXAMPLE:
Preferred:
Single static project deployed through Cloudflare Pages.

Avoid initially:
React applications, databases, authentication systems, or AI-generated runtime logic.

CONFLICTS:
May limit scalability in later development phases.

LAST UPDATED:
2026-05-13

---

## OBS-003

Users respond better to practical transport and ownership framing than abstract charging hypotheticals.

Implication:
Question wording should prioritise concrete ownership situations over theoretical EV scenarios.

LAST UPDATED:
2026-05-13

# Logic Rules

## LOGIC-001

RULE ID: LOGIC-001

CATEGORY: Deterministic Logic

TYPE: Hard Rule

RULE:
Every question must materially influence either outcome classification, confidence level, or friction scoring.

RATIONALE:
Questions without measurable logic impact increase completion time without improving decision quality.

EXAMPLE:
If removing a question does not materially change outcomes, the question should be removed.

CONFLICTS:
None

LAST UPDATED:
2026-05-13

---

## LOGIC-002

RULE ID: LOGIC-002

CATEGORY: Question Sequencing

TYPE: Hard Rule

RULE:
Questions should build context progressively, with each question logically following the previous answer context where possible.

RATIONALE:
Conversational progression reduces cognitive friction and improves completion flow.

EXAMPLE:
Parking practicality before charging expectations.

Bad Example:
Jumping from overnight parking directly to annual salary.

CONFLICTS:
May conflict with optimisation for shortest completion path.

LAST UPDATED:
2026-05-13

---

## LOGIC-003

RULE ID: LOGIC-003

CATEGORY: Behavioural Logic

TYPE: Hard Rule

RULE:
The engine should evaluate operational friction and lifestyle compatibility rather than theoretical technical capability alone.

RATIONALE:
Most EV dissatisfaction originates from routine friction, charging inconvenience, or expectation mismatch rather than inability of the vehicle itself.

EXAMPLE:
An EV may technically support high mileage usage while still producing high lifestyle friction due to charging dependency.

CONFLICTS:
None

LAST UPDATED:
2026-05-13

---

# Wording Rules

## WORDING-001

RULE ID: WORDING-001

CATEGORY: Tone & Language

TYPE: Hard Rule

RULE:
The engine must not use persuasive, urgency-driven, or emotionally manipulative language.

RATIONALE:
The engine exists to reduce poor-fit decisions, not maximise conversions.

EXAMPLE:
Bad:
"Secure the savings before fuel prices rise."

Good:
"Public charging reliance may increase operational costs and inconvenience."

CONFLICTS:
None

LAST UPDATED:
2026-05-13

---

## WORDING-002

RULE ID: WORDING-002

CATEGORY: Tone & Accessibility

TYPE: Hard Rule

RULE:
Questions should use real-world behavioural language instead of technical EV terminology wherever possible.

RATIONALE:
The engine is designed primarily for consumers evaluating EV suitability, not EV enthusiasts or industry professionals.

EXAMPLE:
Good:
"Planning journeys around charging availability"

Bad:
"Managing DC rapid charging dependency"

CONFLICTS:
None

LAST UPDATED:
2026-05-13

---

# Observations

## OBS-001

Users may not immediately associate overnight parking with EV charging practicality.

Implication:
Questions involving parking must include contextual framing related to charging practicality.

LAST UPDATED:
2026-05-13

---

## OBS-002

Users may struggle to understand hypothetical charging disruption scenarios when examples are required for clarification.

Implication:
Questions should prioritise concrete real-world transport situations over abstract hypothetical charging scenarios.

LAST UPDATED:
2026-05-13