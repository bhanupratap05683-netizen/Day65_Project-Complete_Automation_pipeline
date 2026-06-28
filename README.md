# Financial Data Automation Pipeline

## Overview
An end-to-end Python pipeline engineered to automate the extraction, processing, and distribution of financial market data. Designed to eliminate manual reporting latency and spreadsheet risk, this tool generates professional-grade Excel reports from live API data and automatically distributes them via secure SMTP.

## Technical Architecture
* **Data Extraction:** REST API integration via the `requests` library.
* **Transformation & Analytics:** `pandas` deployed for JSON parsing, temporal sorting, and financial metric calculations (daily return percentages).
* **Reporting:** `openpyxl`/`pandas` engine utilized to generate structured `.xlsx` outputs.
* **Distribution:** `smtplib` and `email.message` libraries configured for automated, secure SSL email delivery with MIME attachments.

## Key Features
* **Zero-Touch Execution:** Runs the full extraction-to-delivery lifecycle with a single command.
* **Secure Credentialing:** Utilizes environment variables (`os.environ`) to ensure API keys and SMTP passwords are never exposed in the source code.
* **Scalable Data Handling:** Replaces volatile spreadsheet processing with robust DataFrame architecture.

## Installation & Usage
1. Clone the repository.
2. Install dependencies: `pip install pandas requests openpyxl`
3. Configure environment variables for your email client (`EMAIL_USER`, `EMAIL_PASS`).
4. Execute the pipeline: `python pipeline.py`
