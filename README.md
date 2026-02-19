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

Python 3.8+

Install dependencies:

```bash
pip install requests pandas
