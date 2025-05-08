# 📚 HPFN NLP Prompt Library – v1.1

![Version](https://img.shields.io/badge/version-v1.1-blue)
![License](https://img.shields.io/badge/license-HPFN_Private-green)
![Model](https://img.shields.io/badge/Model-Compatible-GPT_3.5_/_4-orange)
![Status](https://img.shields.io/badge/tests-Validated_%2F_Reviewed-success)

This prompt library contains structured natural language queries for training, validating, and benchmarking NLP-powered query tools using Python (Pandas) and tabular datasets.

---

## 📁 Files Included

- `prompt_library.json`: JSON format with prompts, tags, and structure for fine-tuning, testing, and retrieval.
- `prompt_library.csv`: Human-readable flat version of the library with complexity levels and functional categories.
- `prompt_schema_definition.md`: Explains each field and how to use the schema in evaluation workflows.

---

## 🔑 Prompt Schema

Each prompt now includes:
- `prompt`: A natural language query
- `intent_description`: Action the query is asking for (e.g., GroupBy, Filter)
- `expected_code` / `python_code`: Expected Pandas code logic
- `expected_output`: Human description of result
- `output_type`: DataFrame, Value, or Plot
- `complexity_level`: One of `Simple`, `Intermediate`, or `Nested`
- `category`: Functional category for test filtering and routing

---

## 🚀 Example Prompt Entry

Prompt:
> "Show average discount by fulfillment model."

Expected Code:
```python
df.groupby("fulfillment_model")["discount"].mean()
```

Tags:
- Complexity: Simple
- Category: GroupBy

---

## 🧪 Use Cases
- Test-driven prompt evaluation
- Training LLMs on consistent query-to-code mappings
- Benchmarking NLP tools for accuracy and structure
- Instruction fine-tuning and retrieval pipelines

---

## 🗂️ Version Notes

**v1.1 (May 2025) Updates:**
- ✅ Added `complexity_level` to all prompts
- ✅ Added `category` for classification and routing
- ✅ Aligned with testing workflows (Step A3 complete)

---