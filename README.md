# Financial Data Processing Pipeline

## Overview

A data processing pipeline designed for financial data analysis, specifically for extracting and processing XTB broker statements for Google Sheets integration. This project demonstrates expertise in data extraction, transformation, and visualization techniques essential for financial data analysis.

## Key Features

- **Automated Condition Extraction**: Intelligent parsing of financial data
- **Date Standardization**: Converts various date formats to a consistent standard
- **Advanced DataFrame Processing**: Comprehensive data manipulation capabilities
- **Google Sheets Integration**: Seamless export functionality for collaborative analysis
- **Visualization Support**: Custom styling for financial data visualization
- **Web Automation with Playwright**: Automates the download of currency exchange rate data for streamlined data acquisition

## Installation

### Prerequisites
- Python 3.8+
- pip package manager

### Dependencies
```bash
# Install all required packages
pip install -r requirements.txt
```

**Core Dependencies:**
- pandas (≥2.2.3) - Data manipulation and analysis
- numpy (≥2.2.0) - Numerical computing
- seaborn (≥0.13.2) - Statistical data visualization
- matplotlib (≥3.10.0) - Comprehensive visualization library
- tabulate (≥0.9.0) - Pretty-print tabular data
- playwright (≥1.0.0) - Automated browser testing and web scraping

## Usage Guide

### 1. Data Acquisition

#### Using Playwright to Download Currency Archive

The `playwright_download_currency_archive.py` script automates the download of currency exchange rate data from the NBP Exchange Rates Archive. This script uses Playwright to interact with the website and download the required CSV file.

To run the script, execute the following command:
```bash
python playwright_download_currency_archive.py
```

Ensure that Playwright is installed and set up correctly. This script will download the `archiwum_tab_a_2025.csv` file, which is necessary for the data processing pipeline.

### 2. Data Processing

Execute the main processing script:
```bash
python main.py
```

### 3. Google Sheets Integration

#### Automated Export

Use `GoogleSpreadsheetExporter` to export processed data to Google Sheets. Ensure all dependencies are installed and API credentials are configured for seamless integration.

## Core Components

- **Data Extraction**: Utilizes `MultiConditionExtractor` for parsing financial transaction descriptions using pattern matching and regular expressions.

- **Date Conversion**: Employs `DateConverter` to standardize date formats and perform date-related calculations.

- **Data Processing**: Uses `DataFrameProcessor` for filtering, grouping, and analyzing financial data.

- **Data Export**: Facilitates Google Sheets integration via `GoogleSpreadsheetExporter`, preserving formatting and supporting multiple sheets.

- **Visualization**: Leverages `matplotlib` and `seaborn` for creating financial-specific plots and interactive visualizations.

- **Web Automation**: Uses Playwright for automated browser interactions to download currency exchange rate data.

## Troubleshooting

### Python Environment Issues

#### Windows Command Not Found
If encountering `pip` command not found errors in Windows:
```powershell
# Ensure Python is properly installed
python --version
# Use Python to execute pip
python -m pip install <package>
```

#### macOS/Linux Command Not Found
If Python is not found in zsh:
1. Install Python: `brew install python`
2. Configure zsh: `echo "alias python=/usr/bin/python3" >> ~/.zshrc`
3. Restart terminal

### Common Errors

#### Data Import Issues
- **FileNotFoundError**: Verify the file path is correct and the file exists
- **PermissionError**: Check file permissions
- **UnicodeDecodeError**: Try specifying the encoding: `pd.read_csv('file.csv', encoding='utf-8')`

#### Data Processing Errors
- **KeyError**: Confirm column names match exactly what's in your code
- **TypeError**: Verify data types are compatible with operations
- **ValueError**: Check for missing values or invalid data formats

## License

This project is licensed under the MIT License - see the LICENSE file for details.
