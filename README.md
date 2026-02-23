# Paginated REST API Scraper (Python)

A scalable and resumable Python scraper for extracting large datasets from paginated REST APIs.

Designed for production-style data collection with incremental saving, crash recovery, and clean CSV output.

---

## Overview

This project demonstrates how to:

- Collect data from paginated JSON APIs  
- Handle large datasets safely  
- Resume automatically after interruption  
- Save data progressively to avoid memory overload  
- Build reusable scraping pipelines  

It is suitable for large-scale structured data extraction (100k+ records).

---

## Use Cases

This scraper can be adapted for:

- Academic and research datasets  
- University and education directories  
- E-commerce product listings  
- Business directories  
- Open-data portals  
- Financial and market intelligence APIs  
- Any paginated REST API returning JSON  

---

## Requirements

- Python 3.8+

Install dependencies:

```bash
pip install requests pandas
```

---

## Configuration

Update the following variables inside the script:

```python
BASE_URL = "https://example.com/api/endpoint"
TOTAL_PAGES = 1000
records_per_page = 10
SAVE_FILE = "output_data.csv"
```

Adjust the JSON field mapping to match your API structure:

```python
for item in data["data"]:
    rows.append({
        "Field_1": item.get("field_1", ""),
        "Field_2": item.get("field_2", ""),
        "Field_3": item.get("field_3", ""),
    })
```

---

## How It Works

1. Sends paginated requests to the API.  
2. Parses JSON responses.  
3. Extracts required fields.  
4. Appends results to a CSV file.  
5. Automatically resumes from the last saved page if interrupted.  

---

## Running the Script

```bash
python scraper.py
```

The script will:

- Create the output file if it does not exist  
- Append new pages automatically  
- Resume safely after interruption  

---

## Output

The result is a structured CSV file ready for:

- Data analysis  
- Machine learning pipelines  
- BI dashboards  
- Research projects  

---

## Key Features

- Resume logic (crash-safe)  
- Incremental saving  
- Timeout protection  
- Clean progress display  
- Reusable architecture  

---

## Potential Extensions

- Async requests for higher speed  
- Retry/backoff logic  
- Logging system  
- Database storage instead of CSV  
- Dockerization  

---

Professional, reusable, and production-oriented API scraping template.
