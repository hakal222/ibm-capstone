# IBM Granite Medical Analysis with LLM 

This project processes a Clinical Text Classification dataset (`mtsamples.csv`) using IBM's Granite 8B instruct LLM model via Replicate API, and generates structured output:
- Analytical Result
- Insight & Findings
- Recommendations

---

## Features

- Uses `replicate.run` to query IBM Granite 3.3-8B Instruct
- Builds dynamic prompt from 5 columns of clinical data
- Processes **500 rows** from a medical CSV dataset
- Saves result into `llm_output` column

---

##  Getting Started

###  Requirements

- Python 3 in Google Colab
- [Replicate API Token](https://replicate.com/account/api-tokens)
- replicate-google-colab-example/1.0 User-Agent

###   Set API Token
Set your Replicate token in environment variable:


```python
os.environ["REPLICATE_API_TOKEN"] = "your_token"
```

###  Input File
Make sure you have a file named mtsamples.csv with the following columns:
- description
- medical_specialty
- sample_name
- transcription
- keywords
You can find open datasets like mtsamples.com to generate your own

### Output
The output file will be:
```
mtsamples_llm_output.csv
```

With a new column:
```
llm_output: Generated response in format:

- Analytical Result:
- Insight & Findings:
- Recommendations:
```
