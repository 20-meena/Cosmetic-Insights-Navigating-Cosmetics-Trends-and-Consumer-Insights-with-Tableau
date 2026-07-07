# Cosmetic Insights: Navigating Cosmetics Trends and Consumer Insights with Tableau

## Prepare the Data for Visualization

### Description

Before creating visualizations in Tableau, the Cosmetics dataset was cleaned and transformed to ensure data quality, consistency, and accurate analysis. This preparation process involved handling missing values, removing duplicate records, standardizing text fields, and assigning appropriate data types to each column.

### 1. Data Cleaning

#### Handling Missing Values

- Checked for missing (null) values in **Price**, **Rank**, **Brand**, and **Category** columns.
- Removed or filtered incomplete product records that could affect analysis.
- Replaced missing values in **Skin Type** columns with appropriate logical values (`0` or `False`) to maintain consistency.

#### Removing Duplicates

- Verified the dataset for duplicate product entries.
- Removed duplicate records to ensure each cosmetic product appears only once.

#### Standardizing Text Fields

- Cleaned inconsistent **Brand** names by removing unnecessary spaces and correcting formatting.
- Standardized **Category** labels to maintain consistency (e.g., *"Moisturizer"* instead of *"moisturizers"*).
- Applied proper case formatting across categorical fields for improved readability and uniformity.

---

### 2. Data Transformation

#### Correcting Data Types

The following data type conversions were performed to prepare the dataset for visualization:

| Field | Data Type |
|--------|-----------|
| Price | Number (Decimal) |
| Rank | Number |
| Skin Type Columns | Boolean / String |
| Brand | Dimension (Text) |
| Category | Dimension (Text) |

These transformations ensure that Tableau correctly interprets numerical measures and categorical dimensions, enabling accurate calculations, filtering, and interactive visualizations.

---

## Demo Videos

- **Demo Video 1:**  
  https://drive.google.com/file/d/1jqx0Z0Vwmi-dWbFgNSd57s_eiC1nx0Eo/view?usp=sharing

- **Demo Video 2:**  
  https://drive.google.com/file/d/1qlw5X4HfIOa4GQDg82msn9ZG1xitihM0/view?usp=sharing

- **Demo Video 3:**  
  https://drive.google.com/file/d/1RoZPsodbJxTMysQLzF0YBbyGZBcR0-xy/view?usp=sharing
