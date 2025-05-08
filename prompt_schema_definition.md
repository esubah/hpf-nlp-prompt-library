# 🧾 Prompt Schema Definition

This document defines the structure of each prompt record used in the HPFN NLP Prompt Library.

Each prompt is stored in JSON or CSV format and follows the structure below:

| Field | Type | Description |
|-------|------|-------------|
| `prompt` | string | The user's natural language query. Example: "Show average revenue by service category." |
| `intent_description` | string | Functional category describing the purpose of the query. Examples: GroupBy Aggregation, Join, Filter |
| `python_code` | string | The expected Python (Pandas) code that accurately fulfills the prompt's intent. |
| `expected_code` | string | (Optional) Alias of `python_code` for consistency with LLM evaluation standards. |
| `expected_output` | string | A short human-readable description of the expected output. Example: "Grouped average by category" |
| `output_type` | string | The result format: 'DataFrame', 'Value', or 'Plot'. Helps with UI rendering and validation. |
| `category` | string | Optional category label, e.g., 'Join', 'Derived Column', 'Date Grouping', etc. |
| `complexity_level` | string | (Optional) Marks complexity of the prompt: 'Simple', 'Intermediate', 'Nested'. |
| `model_generated_code` | string | (Optional, runtime) Code output by LLM for comparison against expected. |
| `test_status` | string | (Optional, runtime) Testing result: 'Pass', 'Fail', or 'Inconclusive'. |
| `error_notes` | string | (Optional, runtime) Captures any errors or mismatch notes during evaluation. |

This schema supports downstream use in testing pipelines, fine-tuning datasets, evaluation dashboards, and prompt chaining systems.