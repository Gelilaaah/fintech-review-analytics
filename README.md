# Customer Experience Analytics for Ethiopian Fintech Applications

## Overview

This project is part of the **10 Academy AI Mastery Program** and focuses on analyzing customer feedback from mobile banking applications in Ethiopia.

The objective is to collect and analyze user reviews from the Google Play Store for three major Ethiopian banks:

- Commercial Bank of Ethiopia (CBE)
- Bank of Abyssinia (BOA)
- Dashen Bank

The project simulates a real business analytics workflow where customer feedback is transformed into actionable insights that can support product improvement, customer retention, and service optimization.

---

# Business Context

As mobile banking adoption continues to grow in Ethiopia, customer reviews provide valuable insight into:

- Application reliability
- User experience
- Feature requests
- Technical issues
- Customer satisfaction

This project aims to build a complete analytics pipeline that extracts, processes, stores, and analyzes review data to support data-driven decision making for banking applications.

---

# Project Objectives

The project is divided into four main stages:

## Task 1 — Data Collection & Preprocessing

- Scrape Google Play Store reviews using Python
- Collect:
  - Review text
  - Ratings
  - Review dates
  - Bank names
  - Source information
- Clean and preprocess the data:
  - Remove duplicates
  - Normalize dates
  - Handle missing values
  - Clean noisy text

### Deliverables

- Cleaned CSV dataset
- Scraping and preprocessing scripts
- GitHub repository with organized commits

---

## Task 2 — Sentiment & Theme Analysis

- Perform sentiment analysis using NLP techniques
- Categorize reviews into:
  - Positive
  - Negative
  - Neutral
- Extract recurring themes and keywords such as:
  - Login issues
  - Transfer delays
  - UI experience
  - OTP problems
  - Feature requests

### Deliverables

- Sentiment-labeled review dataset
- Theme extraction results
- Analytical notebooks and scripts

---

## Task 3 — PostgreSQL Database Integration

- Design a relational database schema
- Create:
  - `banks` table
  - `reviews` table
- Insert cleaned review data into PostgreSQL using Python

### Deliverables

- Structured PostgreSQL database
- Database schema documentation
- Data insertion scripts

---

## Task 4 — Insights & Recommendations

- Analyze customer satisfaction trends
- Identify major complaints and strengths for each bank
- Create stakeholder-focused visualizations
- Provide product and customer experience recommendations

### Deliverables

- Visual dashboards and plots
- Final analytical report
- Bank-specific recommendations

---

# Dataset Information

## Source

Google Play Store reviews collected using the `google-play-scraper` package.

## Required Fields

| Column | Description |
|---|---|
| `review` | User review text |
| `rating` | Star rating (1–5) |
| `date` | Review date |
| `bank` | Bank/app name |
| `source` | Review source |

## Data Requirements

- Minimum of 400 reviews per bank
- Minimum total dataset size: 1,200 reviews

---

# Technologies Used

- Python
- Pandas
- NumPy
- Google Play Scraper
- PostgreSQL
- SQLAlchemy / psycopg2
- Scikit-learn
- NLTK / TextBlob / VADER
- Matplotlib & Seaborn
- Jupyter Notebook

---

# Project Structure

```text
omega-fintech-review-analytics-week-2/
│
├── Scripts/
│   ├── task1_scraper.py
│   ├── task1_cleaner.py
│   └── task2_sentiment_thematic.py
│
├── notebooks/
│   ├── task1_scraping_cleaning.ipynb
│   ├── task2_analysis.ipynb
│   └── data/
│       ├── raw/
│       │   └── reviews_raw.csv
│       └── processed/
│           └── reviews_clean.csv
│
├── reports/
│   ├── Interim_Report.pdf
│   └── Final_Report.pdf
│
├── README.md
└── requirements.txt