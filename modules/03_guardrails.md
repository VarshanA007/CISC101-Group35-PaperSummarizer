# Module 3: Guardrails
**Change Log:**
- [05/12/2025]: Added `evidence_mode` for strict hallucination control and  warning messages for short/missing sections per New Requirement B.

## Purpose
Ensure accuracy, prevent hallucinations, and flag low-quality input data.

## Inputs
- Draft Summaries (from Module 2)
- Raw Section Text
- `evidence_mode` variable (User input: "strict" or "standard". Default = "strict")

## Process Logic

### 1. Strict Evidence Enforcement
- **IF** `evidence_mode` == "strict":
  - Verify that every claim, equation, and result in the summary exists in the source text.
  - **Action**: If a specific claim cannot be verified in the text, remove it.
  - **Action**: If the text provides insufficient information to summarize a section, replace the summary with: *"The source text does not provide enough detail to summarize this section in strict evidence mode."*

### 2. Section Validity Checks & Warnings
Scan all sections for length and content validity. Apply the following rules:
- **IF** Section is MISSING or EMPTY:
  - Output Warning: *"Section skipped: no usable text was provided."*
- **IF** Section word count < 50 words:
  - Output Warning: *"Section very short: summary may be incomplete."*

### 3. Chunking
- If a section exceeds token limits, break it into overlapping chunks, summarize individually, and merge results.

## Output
- Validated Summaries
- A list of Flags/Warnings triggered during the process.
