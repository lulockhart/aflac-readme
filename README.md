# Aflac Social Sentiment Analysis Project

This project analyzes public sentiment toward Aflac using data collected from Reddit, Twitter, and Trustpilot. It combines web scraping, data cleaning, sentiment classification, and TF-IDF-based keyword extraction to identify when and why public opinion shifts. The goal is to uncover communication opportunities, reveal platform-specific misunderstandings, and provide actionable insights for improving Aflac’s brand perception and customer engagement.

## Getting Started

These instructions will help you replicate the analysis on your local machine.

1. Download and extract the full project folder (or clone the repo if using Git).
2. Place the cleaned data files in the root folder:
   - `the_reddit_data.xlsx`
   - `the_twitter_data.xlsx`
   - `the_trustpilotdata.xlsx`
3. Launch Jupyter Notebook and open the notebooks in the order described below.

### Prerequisites

You will need the following software and libraries installed:

1. Python 3.9+
2. Jupyter Notebook or JupyterLab
3. Required Python libraries:
   - pandas
   - numpy
   - matplotlib
   - seaborn
   - sklearn
   - nltk
   - textblob
   - openpyxl
   - TF-IDF

Note: All imports use `import` or `from` statements. Do not include `pip install` or `!pip` commands in production scripts.

### Break Down into End-to-End Workflow

1. **Data Collection**
   - `Reddit_Scrape.ipynb` – Scrapes Reddit posts related to Aflac using Pushshift or PRAW.
   - `Twitter_Scrape.ipynb` – Uses Twitter scraping (e.g. snscrape) to gather recent Aflac mentions.
   - `TrustPilot_Scrape.ipynb` – Extracts Aflac reviews from Trustpilot using web scraping with BeautifulSoup and Selenium.

2. **Data Cleaning**
   - `Reddit_Data_Cleaning.ipynb` and `Continued_Reddit_Cleaning.ipynb` – Processes and filters raw Reddit comments.
   - `aflac_twitter_data_cleaning.ipynb` – Cleans and standardizes Twitter dataset.
   - `data_cleaning.ipynb` – Consolidates and finalizes all cleaned outputs.
   - Output files used for analysis:
     - `the_reddit_data.xlsx`
     - `the_twitter_data.xlsx`
     - `the_trustpilotdata.xlsx`

3. **Sentiment Analysis and TF-IDF**
   - `Sentiment_Analysis_and_TDIDF.ipynb` – Assigns polarity and subjectivity scores to each text entry using TextBlob. Extracts platform-specific TF-IDF keyword scores for further interpretation.

4. **Preparation for Tableau**
   - `xlsx_for_tablaeu.ipynb` – Formats the final dataset to support visualization in Tableau, including metadata fields like weekday, month, and hour.

## Deployment

This project is not intended for deployment. It is an academic and exploratory analysis for research and reporting purposes.

## Versioning

Version 1.0

## Authors

**Luke Lockhart**  
**Chloe Cramer**  
**Elli Reel**

## Acknowledgments

* Special thanks to our instructor, Kristina Bigsby, and our closest sponsors Danny Smallwood, Jeremy Tobias, and Derek Bialoncik for guidance and feedback throughout this project.
* Inspiration drawn from Aflac’s real-world branding and customer experience case studies.
* Tools used: Python, Jupyter Notebook, Tableau, Reddit API, Twitter scraping tools, Selenium.
