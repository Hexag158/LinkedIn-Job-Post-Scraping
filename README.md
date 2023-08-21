# LinkedIn Job Posting Scraper
## Background

I was looking to improve my coding skills in Python and found that scraping the web is one of the skills that might be necessary if I want to pursue Data Science
I felt the best place to start was LinkedIn job postings, so this is my start at this project.


## Important notice

The use of robots or other automated means to access LinkedIn without the express permission of LinkedIn is STRICTLY PROHIBITED.  
[More details here](https://www.linkedin.com/robots.txt)

LinkedIn may BLOCK you from searching if you are scraping too much data as you don't have permission to do it.

## Overview

###  LinkedIn.ipynb - Job Scraper by Selenium
Overview: This script scrapes LinkedIn job data.  Using a selenium web driver for Chrome it launches a headless browser and then scrapes all the relevant job details.

Prerequisites: Python installed and environment established with packages from *requirements.txt* installed using 

```
pip install -r requirements.txt
```

1) [Download your appropriate chromedriver](https://chromedriver.chromium.org/downloads) and save it to this repository.

2) Create a new file called *.env* with your login credentials, also saved to this repository.
```
LINKEDIN_USERNAME=email.address@mail.com
LINKEDIN_PASSWORD=password
```

3) Adjust your search criteria for what you want to search for in the .ipynb file
```
# Accepts a list of search keywords to analyze for
search_keywords = ['Data Engineer']

# Accepts one location.. if spaces in the name use '%20'
search_location = "Ha%20Noi"

4) Run "All Cells" on .ipynb  
    a) In the *log* directory, a *.log* file is created that captures the progress of the data scraping and reports any errors  
    b) in the *output* directory, a *.csv* fils is created for this date.  
    NOTE: Script deletes any *.csv* files that have the same date, so as written you can only run this script once per day.
```
### loaddb.ipynb - load CSV file to the local database
Overview: This script loads your CSV files in the *output* directory to the database

1) Modify the code to your liking (including your database information)

3) Run "All Cells" on this .ipynb
