[Module 1: Intake & Setup]

Clean up and normalize section names.

Identify missing, empty, or very short sections.

Extract text belonging to each section. ⬇

[Module 2: Section Loop]

For every section provided:

Summarize only what appears in that section.

Stay within the length requirements (80–120 words).

Add the result to the summary table. ⬇

[Module 3: Guardrails]

Flag short or missing sections.

Strictly enforce no hallucinations or extra fluff.

Break up very long sections into overlapping chunks, summarize them, then merge carefully. ⬇

[Module 5: Citation Extractor]

Detect citations inside each section.

Record citation, short excerpt, and section location.

Do not invent citations. ⬇

[Module 6: Equation Explainer]

Detect equations or symbolic expressions.

Explain them in simple language.

Identify variables accurately, avoid invented details. ⬇

[Module 4: Rendering & Refinement]

Assemble all parts of the final output in the required order.

Generate section summaries, expert summary, and basic summary.

Add contributions, limitations, and glossary.

Perform final checks to ensure summaries match the section list correctly. ⬇

END → Deliver structured output

Overall summary (150–200 words).

Section table (name, word count, summary, flags).

Expert + basic summaries.

3–5 contributions.

3–5 limitations/assumptions.

Glossary of 5–10 terms.

Final checks & warnings.