# Company-Data-Automation-Project

1. Overview
This project automates the analysis of company revenues and the enrichment of contact information using a combination of APIs, web scraping, and data processing techniques. It processes input data from an Excel file, fetches revenue information from multiple sources, assigns tiers based on revenue, and retrieves contact details such as emails and LinkedIn profiles.

The automation is implemented in a Jupyter Notebook and outputs results to an Excel file and a JSON summary.

2. Features
a) Revenue Estimation (Part A): Fetches and parses annual revenue data for companies using AI models, web searches, financial APIs, and manual fallback data. Assigns tiers like "Super Platinum", "Platinum", "Diamond", or "Gold" based on revenue thresholds.

b) Contact Enrichment (Part B): Searches for LinkedIn profiles, designations, and work emails using domain-based email hunters and web searches.
Multi-source data fetching with fallbacks to ensure reliability.
Rate limiting and error handling for API calls.
Output generation in Excel and JSON formats.

3. Requirements

a) Python 3.x
b) Jupyter Notebook
c) Required libraries (installed via pip):
serpapi
openpyxl
requests
yfinance
pandas
google-generativeai

d) API Keys:
SerpAPI (for web searches)
Hunter.io (for email discovery)
Google Gemini (for AI-powered queries)

4. Usage
a) Prepare the input Excel file (e.g., "input.xlsx") with the required sheets and data format.
b) Open the Jupyter Notebook (CompanyAutomation.ipynb).
c) Run all cells to process the data.

The script will:
Fetch and estimate revenues for companies.
Enrich contact information.
Save outputs to "output_assignment_enhanced.xlsx" and "automation_solution.json".


5. Data Sources and Methods
a) Revenue Sources: Manual database, Google Gemini AI, SerpAPI web searches, Yahoo Finance.
b) Contact Sources: SerpAPI for LinkedIn, Hunter.io for emails.
c) Fallback mechanisms ensure data is retrieved even if primary sources fail.
d) Revenue parsing uses regex patterns to extract figures from text snippets.

7. Output
a) Excel File: Contains two sheets - "Companies_Output" (with revenues and tiers) and "Contacts_Output" (with enriched details like designations, LinkedIn URLs, and emails).
b) JSON File: Summarizes the automation workflow, APIs used, and manual fallbacks.
c) Summary statistics printed to console (e.g., number of companies/contacts processed and data found).

8. Limitations
a) Dependent on API availability and rate limits.
b) Revenue data may not always be up-to-date or accurate for private companies.
c) Email and LinkedIn discovery relies on public data and may not always succeed.
d) Manual revenue data is provided as a fallback for specific cases.

License
This project is licensed under the MIT License. See the LICENSE file for details.



Input Excel file with sheets: "Company" (company names and regions) and "Contacts" (contact details).
