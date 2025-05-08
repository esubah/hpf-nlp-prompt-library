# 📚 HPFN NLP Prompt Library – v1.0

![Version](https://img.shields.io/badge/version-v1.0-blue)
![License](https://img.shields.io/badge/license-HPFN_Private-green)
![Model](https://img.shields.io/badge/Model-Compatible-GPT_3.5_/_4-orange)
![Status](https://img.shields.io/badge/tests-Validated_%2F_Reviewed-success)

This prompt library contains structured natural language queries for training, validating, and benchmarking NLP-powered query tools using Python (Pandas) and tabular datasets.

## 📁 Files Included

- `prompt_library.json`: JSON format used for fine-tuning, RAG, and retrieval interfaces
- `prompt_library.csv`: Human-readable flat version for browsing and test planning
- `prompt_schema_definition.md`: Explains each field in the JSON schema

## 🔑 Prompt Schema

Each prompt contains:
- `prompt`: A natural language query (e.g., "Show average sales by region")
- `intent_description`: Functional intent (e.g., GroupBy Aggregation, Join)
- `expected_code`: Python code expected to be generated
- `expected_output`: Description of the result/output type
- `output_type`: DataFrame, Value, or Plot
- `category`: Functional category
- `python_code`: Alias of expected_code

## 🚀 Usage Examples

Prompt:
> "List all sellers flagged for fraud with more than 3 violations."

Expected Code:
```python
df[(df['fraud_flag'] == 1) & (df['policy_violation_count'] > 3)]
```

## 🧪 Use Cases
- LLM few-shot prompting
- Prompt evaluation and scoring
- Instruction fine-tuning dataset generation
- Streamlit app test automation

## 🗂️ Version
This is version `v1.0` (May 2025). Future versions may add complexity scores, output types, or multi-table logic.
