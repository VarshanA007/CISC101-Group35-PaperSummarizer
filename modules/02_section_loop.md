# Module 2: Section Loop
**Change Log:**
- [05/12/2025]: Added `summary_level`  to support "short" vs "detailed" output modes per New Requirement A.

## Purpose
Iterate through every section provided by the user to generate the core content of the summary.

## Inputs
- Validated Section List (from Module 1)
- `summary_level` variable (User input: "short" or "detailed". Default = "short")

## Process Logic
For each section in the Validated Section List:

1. **Context Check**: Isolate the text specific to this section.
2. **Apply Summary Level**:
   - **IF** `summary_level` == "short":
     - Generate a concise 1–2 sentence summary of the section.
   - **IF** `summary_level` == "detailed":
     - Generate a short paragraph summary (approx. 3-4 sentences).
     - Generate a bulleted list of 3–5 key points extracted from the section.

3. **Output Generation**:
   - Format the output for the section.
   - Add the result to the Master Summary Table.

## Constraints
- Do not summarize content from other sections.
- Maintain the original order of the sections.
