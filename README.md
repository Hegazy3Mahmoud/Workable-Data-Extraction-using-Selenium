# Workable-Data-Extraction-using-Selenium


## Overview
This script automates the process of logging into Workable, navigating to the Reports section, applying date filters, and exporting CSV reports using Selenium WebDriver.

## Features
- Automates Workable login using provided credentials.
- Handles scrolling and clicking elements dynamically.
- Navigates to the "Reports" section.
- Selects the "Team Productivity" report.
- Applies date filters for a specific date range.
- Exports CSV reports for the selected date range.
- Handles potential reCAPTCHA and EU cookie pop-ups.

## Prerequisites
### Install Dependencies
Ensure you have the following installed:
- Python 3.x
- Google Chrome Browser
- ChromeDriver (compatible with your Chrome version)
- Selenium
- gspread (for future Google Sheets integration)
- Google authentication libraries

To install dependencies, run:
```sh
pip install selenium gspread google-auth google-auth-oauthlib google-auth-httplib2 oauth2client
```

### Setup
1. Download ChromeDriver and place it in the project folder.
2. Replace `username` and `password` variables with your Workable credentials.
3. Update the ChromeDriver path in the script if needed.

## Code Explanation
### 1. **Login Automation**
The script opens the Workable login page, enters the credentials, and handles optional elements like scrolling and cookie pop-ups.

### 2. **Handling reCAPTCHA (If Needed)**
It attempts to detect and click the reCAPTCHA checkbox if it appears.

### 3. **Navigating to Reports Section**
After login, it navigates to the "Reports" section and selects the "Team Productivity" report.

### 4. **Applying Date Filters**
The script selects a specific date range (yesterday's data in the current version) and applies the filter.

### 5. **Exporting CSV**
Once the date range is applied, the script clicks the "Export CSV" button to download the data.

### 6. **(Commented Section) Automating Multiple Date Exports**
The commented section contains a loop that iterates through multiple dates, exporting daily reports from October 1, 2024, to January 19, 2025. Uncomment this section to download multiple reports automatically.


