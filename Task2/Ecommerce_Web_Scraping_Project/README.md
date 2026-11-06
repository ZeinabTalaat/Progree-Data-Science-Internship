# E-Commerce Product Intelligence
### Automated Web Scraping & Data Extraction Pipeline

## Project Overview

This project implements an automated web scraping pipeline using Python to collect, extract, clean, validate, and export e-commerce product data from [Scraping Sandbox](https://scrapingsandbox.com/), a public demo website designed for web scraping practice.

The pipeline transforms unstructured webpage text into structured datasets containing product information and product variants, making the data ready for further analysis.

## Project Objectives

- Automate product data collection from a public website.
- Extract structured product information from raw webpage content.
- Collect product variants and link them to their corresponding products.
- Perform data quality assessment and cleaning.
- Validate product attributes and business rules.
- Export clean datasets in CSV format.

## Technologies & Libraries

- **Python** – Main programming language.
- **Requests** – HTTP requests and webpage retrieval.
- **BeautifulSoup** – HTML parsing and text extraction.
- **Pandas** – Data manipulation, cleaning, and validation.
- **JSON** – Extracting structured product information embedded in webpage text.
- **Jupyter Notebook** – Development and documentation.

## Pipeline Workflow

1. **Web Scraping:** Retrieve product pages using automated HTTP requests.
2. **Raw Data Collection:** Extract webpage text and save the original content.
3. **Data Extraction:** Locate and parse embedded product data.
4. **Data Structuring:** Organize extracted information into Pandas DataFrames.
5. **Data Quality Assessment:** Inspect missing values, duplicates, and data relationships.
6. **Data Cleaning:** Standardize text, convert data types, and validate numeric fields.
7. **Data Validation:** Verify product identifiers, URLs, prices, ratings, and variant relationships.
8. **Data Export:** Save the final datasets as structured CSV files.

## Dataset Overview

The pipeline successfully collected:

| Metric | Result |
|---|---:|
| Products | 500 |
| Product Variants | 1,685 |
| Unique Vendors | 20 |
| Unique Categories | 15 |
| Extraction Errors | 0 |

### Products Dataset

Contains:
- Product ID and Product Name
- Vendor and Category
- Current Price and Original Price
- Description and SKU
- Availability and Rating
- Review Count and Tags
- Product Creation Date
- Product URL and Scraping Timestamp

### Variants Dataset

Contains:
- Product ID
- Product Name
- Variant Color
- Variant Size
- Variant SKU
- Variant Price
- Variant Availability

## Data Quality & Validation

The final validation confirmed:

- No duplicate product records.
- No duplicate Product IDs or SKUs.
- No missing product names or IDs.
- No invalid product URLs.
- No invalid ratings or negative prices.
- No orphan product variants.
- All collected variants are linked to existing products.

Missing `Original_Price` values were retained because they represent products without a recorded original price, rather than automatically being treated as errors.

## Project Files

| File | Description |
|---|---|
| `Ecommerce_Web_Scraping_Pipeline.ipynb` | Complete scraping and processing workflow |
| `data/raw_ecommerce_data.csv` | Raw webpage text collected from product pages |
| `data/ecommerce_products.csv` | Extracted structured product data |
| `data/ecommerce_variants.csv` | Product variant records |
| `data/clean_ecommerce_products.csv` | Cleaned and validated product dataset |

## Key Outcomes

- Built an automated scraping pipeline for 500 product pages.
- Extracted 1,685 product variants.
- Converted raw webpage content into structured datasets.
- Applied data cleaning and standardization techniques.
- Performed data quality checks and relationship validation.
- Exported reusable CSV datasets for downstream analysis.

## Data Source & Disclaimer

The project uses **Scraping Sandbox**, a demo e-commerce environment created for web scraping practice. The collected records are sample data and should not be interpreted as actual commercial transactions or real store sales.

## Author

**Zeinab Talaat Samaha**

AI Student | Data Science & Data Analysis

GitHub: [ZeinabTalaat](https://github.com/ZeinabTalaat)