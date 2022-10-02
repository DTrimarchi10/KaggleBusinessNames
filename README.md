# Business Names Analysis (EDA)

Dataset: https://www.kaggle.com/datasets/peopledatalabssf/free-7-million-company-dataset

Derive insights about Business Names. 

# Outline

This readme summarizes the work completed in the analysis of a large Business Names Dataset. The sections contained herein include the following:

* [Abstract](#Abstract)
* [Results Summary](#Results-Summary)
* [Recommendations & Future Work](#Recommendations-and-Future-Work)
* [Files and Descriptions](#Files-and-Descriptions)
* [EDA](#EDA)
  * [Number of Words](#Number-of-Words)
  * [Common Words](#Common-Words)

-------

    
# Abstract

This project comprises a quick analysis of a Kaggle Dataset of Business Names. For this analysis, I ignored inter-relationships between fields that do not involve the Business Name in favor of focusing specifically on the words contained in company names. The bulk of the dataset comprises of worldwide business names along with their industries and number of employees.

**Question/Problem:** What insights can we gain about Company Names?

**Infomation Generated:**
- **Number of words** in a company name (stopwords removed).
- Word count vs Company Size.
- Word count vs Country.
- Lists of **Most Common Words** in company names for the top 20 industries --Shown in Bar Charts and Word Clouds.
- **Heat Map** of common words that are shared across more than one industry.
- **Head Map** of common words that are unique to an industry.

**Process:** First, a quick understanding of the data fields and missing data was performed. Since the dataset is very large, incomplete records were dropped. The Busines Names themselves were tokenized and cleaned for further analysis to generate associated charts. Details regarding data selection can be seen in the associated jupyter notebook.

-------

# Results Summary

Word count analysis showed that **as company size increases, the number of words in the company name decreases**. This makes sense anecdotally because, as companies become massive, they are more well-known and do not require extra descriptive words. They are known by a only 1 or 2 words or acronyms (ex. Google, Apple, GE, Honeywell).

**China has the highest average word count** for company names followed by several other Asian countries. Scandinavian countries were on the shorter side. This is likely due to differences in language structure, but further analysis would need to be completed in order to confirm this to be true. 

**Many words in business names are common**. Some of these words are common across a few industries while others are specific to a particular industry. Because of this, given an company name, **presence of "common words" could be used to predict the business industry**. 

-------


# Recommendations and Future Work

It is possible to perform stemming analysis on the company names to draw further connections between related words. This would require a focus on specific language of origin. Furthermore, the degree of relationship between words in company names could be mapped using a trained word vector library (something like GloVe pre-trained word vectors in English). Peforming this kind of analysis could be used to provide a degree of similarity measure between various business names. 

-------

# Files and Descriptions
    

<details><summary>USE DROPDOWN</summary>

**All Python work is contained in the following files**:
* **[Business Names.ipynb](Business%20Names.ipynb)**
  * A jupyter notebook containing code which reads the kaggle csv file and performs basic data cleaning. This notebook also contains all of the exploratory data analysis of the company business names (word counts and common word charts).
  
**Data Files**
* **./dataset/companies_sorted.csv**
  * This is the Kaggle raw dataset. It is not included in the github repository.
* **./dataset/companies_sorted_subset_cleaned.csv**
  * Contains the downselected, cleaned and tokenized data from the original Kaggle dataset. It is not included in the github repository.
  
**Output Files**
* **[./industry_words/](./industry_words/)**
  * This directory contains csv files for each of the top 20 industries. Each csv file contains a list of the top 100 most common words in company names along with their frequency and frequency % of companies within the industry.
* **[./charts_industry_word_bar/](./charts_industry_word_bar/)**
  * This directory contains bar charts showing the most common words for each industry.
* **[./charts_industry_word_cloud/](./charts_industry_word_cloud/)**
  * This directory contains word cloud charts showing the most common words for each industry. More words can be seen than in the bar charts.
* **[./charts/](./charts/)**
  * This directory contains all other generated charts and heatmaps for this analysis.

</details>

-------
# EDA

## Number of Words

#### Number of words vs Company Size
<details><summary>NUMBER OF WORDS VS COMPANY SIZE</summary>

<img src="./charts/Word Count vs Company Size.png" width=80%>

<img src="./charts/Word Count vs Company Size scatter.png" width=80%>

</details>

#### Number of words by Country
<details><summary>NUMBER OF WORDS BY COUNTRY</summary>

<img src="./charts/Num Words by Country.png" width=100%>

</details>

-------


## Common Words


#### Common Words in Each Industry

<details><summary>COMMON WORDS BY INDUSTRY</summary>

Bar Chart          |  Word Cloud
:-------------------------:|:-------------------------:
architecture & planning
<img src="./charts_industry_word_bar/architecture & planning bar chart.png" width=100%> | <img src="./charts_industry_word_clouds/architecture & planning word cloud.png" width=100%>
automotive
<img src="./charts_industry_word_bar/automotive bar chart.png" width=100%> | <img src="./charts_industry_word_clouds/automotive word cloud.png" width=100%>
computer software
<img src="./charts_industry_word_bar/computer software bar chart.png" width=100%> | <img src="./charts_industry_word_clouds/computer software word cloud.png" width=100%>
construction
<img src="./charts_industry_word_bar/construction bar chart.png" width=100%> | <img src="./charts_industry_word_clouds/construction word cloud.png" width=100%>
design
<img src="./charts_industry_word_bar/design bar chart.png" width=100%> | <img src="./charts_industry_word_clouds/design word cloud.png" width=100%>
education management
<img src="./charts_industry_word_bar/education management bar chart.png" width=100%> | <img src="./charts_industry_word_clouds/education management word cloud.png" width=100%>
financial services
<img src="./charts_industry_word_bar/financial services bar chart.png" width=100%> | <img src="./charts_industry_word_clouds/financial services word cloud.png" width=100%>
food & beverages
<img src="./charts_industry_word_bar/food & beverages bar chart.png" width=100%> | <img src="./charts_industry_word_clouds/food & beverages word cloud.png" width=100%>
health, wellness and fitness
<img src="./charts_industry_word_bar/health, wellness and fitness bar chart.png" width=100%> | <img src="./charts_industry_word_clouds/health, wellness and fitness word cloud.png" width=100%>
hospital & health care
<img src="./charts_industry_word_bar/hospital & health care bar chart.png" width=100%> | <img src="./charts_industry_word_clouds/hospital & health care word cloud.png" width=100%>
information technology and services
<img src="./charts_industry_word_bar/information technology and services bar chart.png" width=100%> | <img src="./charts_industry_word_clouds/information technology and services word cloud.png" width=100%>
internet
<img src="./charts_industry_word_bar/internet bar chart.png" width=100%> | <img src="./charts_industry_word_clouds/internet word cloud.png" width=100%>
law practice
<img src="./charts_industry_word_bar/law practice bar chart.png" width=100%> | <img src="./charts_industry_word_clouds/law practice word cloud.png" width=100%>
management consulting
<img src="./charts_industry_word_bar/management consulting bar chart.png" width=100%> | <img src="./charts_industry_word_clouds/management consulting word cloud.png" width=100%>
marketing and advertising
<img src="./charts_industry_word_bar/marketing and advertising bar chart.png" width=100%> | <img src="./charts_industry_word_clouds/marketing and advertising word cloud.png" width=100%>
non-profit organization management
<img src="./charts_industry_word_bar/non-profit organization management bar chart.png" width=100%> | <img src="./charts_industry_word_clouds/non-profit organization management word cloud.png" width=100%>
professional training & coaching
<img src="./charts_industry_word_bar/professional training & coaching bar chart.png" width=100%> | <img src="./charts_industry_word_clouds/professional training & coaching word cloud.png" width=100%>
real estate
<img src="./charts_industry_word_bar/real estate bar chart.png" width=100%> | <img src="./charts_industry_word_clouds/real estate word cloud.png" width=100%>
retail
<img src="./charts_industry_word_bar/retail bar chart.png" width=100%> | <img src="./charts_industry_word_clouds/retail word cloud.png" width=100%>
staffing and recruiting
<img src="./charts_industry_word_bar/staffing and recruiting bar chart.png" width=100%> | <img src="./charts_industry_word_clouds/staffing and recruiting word cloud.png" width=100%>

</details>

-------


#### Heatmap Common Words in Multiple Industries

Examples: 
* "group" is common across many industries.
* "consulting" is most common in management consulting, but also common in computer software, financial services, information technology and services, marketing and advertising, professional training and coaching, and staffing and recruiting.
* "design" is most common in the design industry (naturally), but also common in architecture and planning, internet, and marketing and advertising.

<img src="./charts/Common Business Name Words across Industries.png" width=80%>

#### Heatmap Common Words Unique to an Industry

Examples:
* "care" and "medical" are only common in hospital and health care.
* "law", "llp", "pc", "firm" are only common in law practice.
* "foundation" is only common in non-profit orgs. 
* "studio" is only common in the design industry.

<img src="./charts/Common Business Name Words Unique in their Industry.png" width=80%>


```python

```
