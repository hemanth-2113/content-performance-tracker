# Content Performance Tracker

Content Performance Tracker is a small Python tool that helps content marketers turn campaign data into a clear weekly performance report.

It reads content performance data from a CSV file, calculates key marketing metrics, identifies the best-performing content, and saves the results as a Markdown report.

## What it tracks

The tool calculates:

- Total page views
- Total leads
- Total conversions
- Average conversion rate
- Best-performing content by conversions
- Best-performing content by conversion rate

## Technology

This project is built with:

- Python 3.10 or later
- pandas for reading and analyzing CSV data

It does not connect directly to Google Analytics, Google Ads, or any other marketing platform. The user provides the performance data through a CSV file.

## Project structure

```text
content-performance-tracker/
├── README.md
├── requirements.txt
├── tracker.py
├── sample-content-data.csv
└── .gitignore

```

## CSV format

The CSV file must contain these columns:

| Column | Description |
|---|---|
| `title` | Name of the article or content asset |
| `channel` | Where the content was distributed |
| `page_views` | Number of page views |
| `leads` | Number of leads generated |
| `conversions` | Number of completed conversions |

## Installation

Clone the repository:

```bash
git clone https://github.com/thegirlcoderr/content-performance-tracker.git
cd content-performance-tracker
```

Create a virtual environment:

```bash
python -m venv venv
```

Activate it on macOS or Linux:

```bash
source venv/bin/activate
```

Install the required package:

```bash
pip install -r requirements.txt
```

## Run the tracker

Run the tool with the sample data:

```bash
python tracker.py sample-content-data.csv
```

The tool creates a report named:

```text
content-performance-report.md
```

## Example use case

A content marketer adds weekly article performance data to the CSV file and runs the tracker.

The report summarizes overall performance and highlights the content that generated the most conversions.

## Limitations

- The tool only accepts CSV files.
- It does not pull data directly from analytics platforms.
- It does not store data in a database.
- It creates a Markdown report instead of a live dashboard.
