# AI Security Alert Triage Assistant

A practical AI tool that automatically triages security alerts using Google Gemini, simulating the work of a Tier-1 SOC analyst.

**Author:** Maryam Fagbo

---

## Project Overview

Security Operations Centers (SOCs) receive a large number of alerts every day. Manually reviewing each one is time-consuming and often leads to alert fatigue. This project demonstrates how Large Language Models can assist analysts by performing first-level triage automatically and consistently.

## Problem Statement

- High volume of security alerts
- Limited time for Tier-1 analysts
- Need for fast, consistent initial assessment
- Risk of missing important alerts due to alert fatigue

## Solution

The tool reads sample security alerts and sends each one to Google Gemini with a carefully designed role-based prompt. The model returns a structured JSON response containing:

- Severity level
- Clear summary
- Likely attack type
- Recommended next action
- Confidence score

The results are then saved into a clean CSV report using Pandas.

## Features

- Role-based prompting (“You are a Tier-1 SOC analyst”)
- Forced structured JSON output
- Handles multiple alert types (failed login, malware, phishing, privilege escalation, etc.)
- Error handling for failed API calls
- Automatic CSV report generation
- Completely free to run (Google Colab + Gemini free tier)

## Technologies Used

- Python
- Google Gemini API (`google-genai`)
- Pandas
- Google Colab

## Project Structure
ai-security-alert-triage/

├── README.md

├── requirements.txt

├── triage_assistant.py

├── sample_output/

│   └── security_alert_triage_report.csv

└── notebook/

└── AI_Security_Alert_Triage.ipynbText
## How to Run

### Option 1: Google Colab (Recommended)

1. Open the notebook in Google Colab
2. Add your Gemini API key in Colab Secrets with the name `GEMINI_API_KEY`
3. Run all cells in order

### Option 2: Locally

```bash
pip install -r requirements.txt
python triage_assistant.pySample Alerts Covered
```
**Failed login attempts:**

Malware detection
Suspicious outbound IP (possible C2)
Phishing attempt
Unusual API activity
Privilege escalation

**Learning Outcomes:**

Prompt engineering for structured output
Working with the modern Google GenAI SDK
Building practical AI applications for cybersecurity
Handling API responses and errors
Generating professional reports with Pandas
Understanding real-world SOC triage workflows

**Limitations:**

Uses synthetic sample alerts (not connected to a real SIEM)
Subject to Gemini free-tier rate limits
Designed as a learning and portfolio project

**Future Improvements:**

Integrate with real SIEM / SOAR platforms
Add more sophisticated severity scoring
Support multiple LLM providers
Build a simple web dashboard (Streamlit)
Add feedback loop for continuous improvement

**Acknowledgements:**

Google Gemini API
Inspired by real SOC automation practices

Maryam Fagbo
