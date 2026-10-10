# SelectiCore v69.1 — Question-bank repair report

## Changes made

- Fixed generator-template defects found in Mathematical Reasoning: removed-square area, adding items to every box, algebraic rectangle area, whole-number ratio splits, alternating sequences, row-position values, perimeter changes, student-count percentage calculations, and remainder wording/options.
- Corrected inconsistent Thinking Skills templates: switch activation order, strict-inequality logic, conditional reasoning and question wording where constraints did not match the answer choices.
- Rebuilt the 100-item static Reading sample from passage-linked generated questions. The sample now contains 100 unique question stems across 9 passages; every question has a passage, four options and a valid answer index.
- Corrected the static 400-item sample bank's answer-index/duplicate-option structural issues and added writing rubric criteria to static writing prompts.
- Added `black-swan.html` with 26 original advanced-topic lessons across Thinking Skills, Mathematical Reasoning, Reading and Writing. Each lesson includes four step scenes, a worked example, a multiple-choice question, answer feedback and optional browser narration.
- Added `learn-topic.html` and `strategy-detail.html` so Learn topics and Core Strategy cards can open their own topic/strategy lesson URLs.
- Added navigation links to the Black Swan Lab and lesson pages, and updated Test Centre rendering so a single Reading question displays its passage.

## Checks run on this build

- 4,200 generated Mathematical Reasoning questions (120 generated 35-question tests) were checked against independent calculations for the audited arithmetic/template families: **0 mismatches detected**.
- 4,800 generated Thinking Skills questions (120 generated 40-question tests) were checked against their stated constraints and answer keys: **0 mismatches detected**.
- 120 generated tests for each of the four subjects were run through the generator/quality gate: **0 generation errors**.
- Generated Reading tests contained 17 groups and 38 answer parts; a sample Reading test had 38 distinct question stems and valid answer indices.
- The static 400-item bank had **0 answer-index or duplicate-option structural errors** after repair.
- Inline JavaScript syntax checks passed for the HTML pages.

## Important limitation

These checks are substantial automated and pattern-based validation, not proof that every possible generated variant in the full 16,000-test range has been manually reviewed by an expert. Writing responses are practice-reviewed by automated heuristics, not by a human marker. The bank is original SelectiCore practice content and is not official NSW Department of Education material. Before relying on it as a production exam-preparation product, continue content review with a qualified educator.

## Black Swan Lab — exhaustive item-by-item audit (2026-10-10)

The `black-swan.html` lesson array was extracted and every quiz item was checked individually for whether its answer follows from the wording, whether the explanation supports the key, and whether another listed option could reasonably also be correct.

- **26 quiz questions audited:** 8 Thinking Skills, 8 Mathematical Reasoning, 6 Reading, 4 Writing.
- **24 items retained as written; 2 items had ambiguous wording and were revised** (Reading #18, Writing #25).
- After revision, **26/26 answer keys were judged defensible** in this audit; all 26 include an explanation.
- Structural checks: every item has exactly 4 options, a valid answer index, four lesson steps, a non-empty explanation, and no duplicate options. **0 structural errors**.
- Correct answer keys in display order: **1 A, 2 B, 3 B, 4 B, 5 B, 6 B, 7 B, 8 C, 9 A, 10 C, 11 A, 12 C, 13 B, 14 B, 15 C, 16 B, 17 B, 18 C, 19 B, 20 B, 21 C, 22 A, 23 B, 24 B, 25 C, 26 B**.
- Reading #18 now states each text's position explicitly so the question about when rules are justified follows from the passage summaries. Writing #25 now asks about first-person *limited point of view* and clearly contrasts the narrator's own thoughts with another character's private thoughts.

This is an exhaustive review of the **26 built-in Black Swan quiz items**, not a claim that all writing responses are objectively gradable or that a qualified external educator has certified the material. The lessons are original extension practice, not official NSW exam questions.

## v69.2 addition — Four-test School Readiness Assessment
- Added a discoverable School Estimator entry point on the landing page, dashboard, Readiness page and Test Centre.
- Added a full four-section timed assessment using the existing generated NSW-style mock sequence: Reading (45 min; 17 groups), Mathematical Reasoning (40 min; 35 questions), Thinking Skills (40 min; 40 questions), and Writing (30 min; 1 response).
- On completion, the page reports each section and a simple equal-weight practice average. Writing uses SelectiCore's automated practice rubric and is clearly labelled as not an official examiner mark.
- The school-target text is deliberately cautious. Practice percentages are not official NSW scaled scores, no current school cut-offs are embedded, and the tool does not claim to predict admission or identify a guaranteed/most-likely school.
- Validation: 22 HTML files checked; 0 inline JavaScript syntax errors; 0 missing local href targets. Generated full-mock structure checked for four subjects in the correct order and expected section times.
