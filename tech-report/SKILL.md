---
name: tech-report
description: >-
  Write, revise, or review technical reports, evaluation and benchmark writeups,
  experiment logs, design decisions, and incident analyses. Clarify the question,
  evidence, reasoning, measurements, and limits in Markdown or HTML. Use for
  requests such as "write up the results", "document this experiment", or "make
  this report clearer"; not for academic manuscript preparation.
---

# Tech Report

Help the intended reader understand what a technical report establishes, why the
evidence matters, and what remains uncertain. Borrow disciplined reasoning from
academic writing without adding literature reviews, scholarly citation or
bibliography requirements, novelty claims, or publication conventions.

## Choose the scope

Infer the report's purpose, audience, requested depth, available evidence, and
output format from the task and existing material. Ask only for missing
information that could materially change the result. Reuse context and
authorization already supplied.

For a quick clarity pass or local revision, address the affected passage and its
consequential dependencies; do not restart a full writing process. Preserve the
original meaning, values, units, negation, conditions, uncertainty, equations,
code, identifiers, and user voice. If a factual correction is needed, distinguish
it from a wording change and ground it in evidence.

Use **doc-coauthoring** conditionally for substantial collaborative document work
or an explicit request. It can organize collaboration; this skill supplies the
reasoning and clarity lens. Do not restart intake or approval loops already
resolved in the current task. Fresh-reader tests assess comprehension, not
independent factual validity.

Support Markdown and HTML. Generate only the requested format or formats. If
unspecified, preserve the existing format; otherwise default to Markdown. When
producing or checking either format, read
[Markdown and HTML production](references/markdown-html.md). This skill does not
include hosting, website publishing, or deployment.

## Build the reasoning

Use **question → judgment criteria → approach → observations → interpretation →
conclusion** as a reasoning aid, not mandatory headings. Scale it to the task:

1. Identify the question or decision the report must support. Explain why each
   measurement or comparison is needed to answer it.
2. State relevant judgment criteria when available. Use documented expectations
   and thresholds; do not invent them or imply they were selected before the
   work. Label retrospective interpretation as retrospective.
3. Explain the approach and comparison conditions enough to assess the result.
   Read actual code, data, logs, or supplied records for consequential claims
   rather than relying on memory. Code inspection supports claims about what
   the code specifies; it does not prove a runtime measurement occurred.
4. Separate observations from supported interpretations, hypotheses, and
   unverified points. Explain a causal mechanism only when evidence supports it.
   An unknown cause may remain unknown; add an investigation plan only when
   useful or requested.
5. Give the conclusion at the strength and scope the evidence supports. Carry
   material limitations into the summary and conclusion, not just the details.

Ground consequential claims internally in available evidence. Helpful links can
make verification or navigation easier, but do not require a claim ledger,
bibliography, or reader-facing source clutter. When evidence is unavailable,
mark the gap instead of fabricating an explanation or a verified conclusion.

## Shape the report for its purpose

Choose sections that serve the reader's question. The following are adaptable
patterns, not required outlines.

| Purpose | Useful structure | What the conclusion must distinguish |
| --- | --- | --- |
| Evaluation or benchmark | Question and result; relevant criteria and comparison conditions; measurements; interpretation and limits | Measured result versus wider generalization; documented expectation versus retrospective judgment |
| Design or decision | Decision or proposal; goals and constraints; options and criteria; tradeoffs and evidence; consequences and open points | Established facts versus assumptions; selected option versus unresolved decision |
| Incident or analysis | Impact and current finding; chronology or observed behavior; evidence; supported causes and unknowns; actions where relevant | Observed events versus causal inference; mitigation versus verified resolution |

Make the answer, proposal, or current finding easy to locate near the start of
the report, together with any limitation that materially changes its meaning.
Respect a supplied format when choosing the opening.

Open a section with its result, purpose, or question as appropriate. Give an
overview table when it helps compare multiple findings, not by default. A
summary may state a finding and a discussion may revisit it to explain meaning
or limits. Keep detailed facts in a canonical location and cross-reference them
rather than duplicating slightly different accounts.

## Make evidence and language legible

**Measurements.** State what a metric means and why it exists. Include units,
numerators and denominators, comparison conditions, aggregation, sample or repeat
counts, and uncertainty where needed for the question and available in the
evidence. Mark missing details accurately. Do not force statistical tests,
repeats, or extra experiments merely to finish the writing. Separate per-request
response latency from total elapsed time and specify the boundary measured.

**Limits.** Distinguish deliberate scope choices, encountered constraints, and
missing verification. Explain what each limits. A fixed corpus may be a planned
scope choice; an accidental confound remains a confound. Do not convert
weaknesses into intentional controls or rationalize their effects.

**Terms and mechanisms.** Define unfamiliar terms before relying on them, with
detail suited to the intended audience. For an unfamiliar concept, explain it
in plain language before introducing its technical label. Keep established
terminology when the intended reader already knows it. Add a glossary only when
lookup helps.
Name the actor, action, and method where known. Explain variant labels such as
`p3/p4`, `v1/v2`, or `config-A/B`: what differs and why, if that reason is known.
Use one name for each entity across prose, tables, diagrams, and any glossary.

**Examples and visuals.** Use meaningful examples grounded in supplied or
verified material; label illustrative examples as such. Add a diagram when it
clarifies relationships, structure, or flow. A visual must convey the same facts
and qualifiers as the text, and its rendering must suit the target format.

## Review and finish

Review in this priority order, fixing the highest-impact issue first:

1. Incorrect, unsupported, or misleading meaning: values, causal claims,
   expectations, conclusions, and material limits.
2. Missing reasoning or reader context: the question, why a measurement exists,
   how the evidence supports the judgment, and necessary definitions.
3. Consistency, navigation, and rendering: body/table/diagram/glossary agreement,
   names and variants, working links and assets, and intended cross-reference
   targets. A link to an existing but wrong section is still a defect.
4. Wording: direct subjects and actions, precise terms, complete explanatory sentences, and
   removal of repetition that adds no distinct purpose.

After revision, compare against the original and the evidence for changed
claims. Use a fresh-reader test when complexity, audience distance, or document
importance warrants it; do not mandate a fixed number of passes or arbitrary
scores. Resolve demonstrated comprehension gaps within scope.

Completion means the requested artifact is delivered with checks and limits
reported accurately. Keep **evidence review**, **reader comprehension**, and
**rendering verification** separate: success in one does not establish the
others. Report what was checked and any material gaps, including unavailable
evidence or an unchecked render. Unresolved points can remain clearly labeled;
do not imply that they support a verified final conclusion.
