# OpenFoodFacts Web Scraping

Web scraping and domain analysis project for the OpenFoodFacts food products dataset.

## Project Overview

This repository contains a Jupyter notebook that scrapes product data from the OpenFoodFacts search endpoint, cleans and enriches the result, and answers a set of analysis questions with charts and summary statistics.

The notebook focuses on:

- collecting 1000+ product records from the public OpenFoodFacts endpoint
- preprocessing nutrition and category fields
- removing duplicates and cleaning missing values
- analyzing product brands, categories, nutrition grades, and country coverage
- exploring relationships such as sugar vs calories

## Repository Contents

- `Task2_OpenFoodFacts_WebScraping.ipynb` - main notebook with scraping, cleaning, and analysis
- `data/openfoodfacts_products.csv` - scraped dataset saved by the notebook
- `README.md` - project overview and run instructions

## Data Source

- Website: https://world.openfoodfacts.org/
- Scraping endpoint: https://world.openfoodfacts.org/cgi/search.pl
- Domain: food products and nutrition labels

## Analysis Questions

The notebook answers these questions:

1. How many products were scraped and how many unique brands exist?
2. What are the top 10 product categories by count?
3. What is the distribution of nutrition grades?
4. How do sugar levels vary by nutrition grade?
5. Which countries appear most frequently?
6. Is there a correlation between sugar and calories?

## How To Run

1. Open `Task2_OpenFoodFacts_WebScraping.ipynb` in Jupyter Notebook, JupyterLab, or VS Code.
2. Make sure the `data/` folder stays in the project root.
3. Run the notebook cells from top to bottom.

The notebook will scrape fresh data if `data/openfoodfacts_products.csv` does not already exist or if the cached file has fewer than the minimum required rows.

## Requirements

The notebook uses common Python data analysis and web scraping libraries:

- pandas
- numpy
- requests
- seaborn
- matplotlib

If your environment does not already have them, install them with:

```bash
pip install pandas numpy requests seaborn matplotlib
```

## Notes

- The notebook uses a cached CSV file to avoid repeated scraping when possible.
- The code includes retry logic and short delays to reduce the chance of request failures.
- If the site layout or API response changes, the scraping step may need to be updated.

## Result

This project demonstrates end-to-end web scraping, cleaning, exploratory analysis, and visualization on a real public dataset.