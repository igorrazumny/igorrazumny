# 🧪 openai_data_quality_audit

A simple, end-to-end GenAI-powered data quality auditor built with OpenAI's GPT-4o.

This script evaluates row-level quality of structured healthcare manufacturing data and provides:
- A quality score
- Issue detection
- Suggested improvements
- One-line summary for each record

## ✅ Use Case
Designed for healthcare/life sciences professionals and teams looking to:
- Improve recipe/documentation data reliability
- Detect quality issues in structured manufacturing logs
- Showcase how GenAI can audit operational data at scale

## 🔍 Example Prompt Sent to GPT-4o
```
Evaluate the data quality of the following healthcare manufacturing record:

{"step": "Mixing", "temperature": 85, "duration": "10m", ...}

1. Rate the data quality from 1 (poor) to 5 (excellent).
2. List any detected issues (e.g., missing values, format mismatches).
3. Suggest improvements if needed.
4. Provide a one-sentence summary for this record.
```

## 📦 How to Run
```bash
# Install dependencies
pip install openai pandas

# Set your API key (use .env or secure environment setup)
export OPENAI_API_KEY=your-key-here

# Ensure sample data exists
mkdir -p data
cp sample.csv data/mock_batch_data.csv  # replace with real data

# Run the script
python openai_data_quality_audit.ipynb  # or open in Jupyter
```

## 📁 Output
A CSV file `audit_results.csv` with an additional `LLM_Review` column containing GPT responses.

## 🛡️ Notes
- Data is processed securely via OpenAI API
- The project demonstrates capabilities of GPT-4o; further guardrails and filtering may be added for production

## 📘 License
MIT License — feel free to adapt for internal projects

## 👤 Author
[Igor Razumny](https://github.com/igorrazumny) · AI Cloud Consulting (Razum GmbH)
