# Project: How do review characteristics affect the emotional tone in skincare product reviews?
**Author:** Amber Ni | **Date:** 05-02-2025 | **Course:** Intro to Data Science

## Project Description
This project analyzes **Sephora skincare product reviews**, focusing on sentiment analysis and thematic insights across user groups with the main research question - how specific review characteristics shape the emotional tone of skincare product reviews on online beauty platforms like Sephora. It employs a range of **natural language processing (NLP)**, **machine learning**, and **statistical techniques**, following a structured workflow, **including**:
1. **Document sampling** – selected a subset of 10,000 reviews across skin types and product categories.  
2. **Text preprocessing** – tokenization, stopword removal, and lemmatization to clean raw review texts.  
3. **Descriptive analysis** – visualized word frequencies using word clouds, term frequency–inverse document frequency (TF-IDF), and Log-Ratio term differences. 
4. **Sentiment analysis** – applied AFINN lexicon to assign each review a sentiment score.
5. **Topic modeling** – used Latent Dirichlet Allocation (LDA) to identify key discussion topics in reviews.
6. **Regression analysis** – assessed how sentiment is influenced by review length, topics, skin type of the reviewer, social media mentions, and product price.

The repository **includes**: 
1. R Markdown `.rmd`: Contains the full analysis pipeline, including data loading, preprocessing, descriptive analysis, visualization, sentiment analysis, topic modeling, and regression. The code is well-documented to ensure reproducibility and transparency.
2. Output codes `.html`:  The knitted output of the R Markdown file, showing the complete analysis with embedded plots, tables, and markdown explanations.
3. Project Report `.pdf`: A concise and visually structured summary of key findings, figures, and insights.
4. Output dataset `.csv`: Processed data used for regression modeling, including all variables used for the regression analysis.

This project aims to decode the factors that drive positive sentiment, reveal emerging skincare trends, and understand how elements such as product characteristics, personal skin concerns, and social media influence shape consumer opinions. By doing so, this project hopes to demonstrate how review analysis benefits brands in optimizing their product development, marketing strategies and consumer support.

## How to Use This Repository

If you'd like to **run the analysis** on your own laptop, follow these steps:
  1. Download the dataset `[Import Dataset]reviews_0-250.csv` from https://drive.google.com/file/d/1_2w39UanQFyokL21zkdlauNGjxgV0a3y/view?usp=sharing. 
  2. Open RMarkdown `Sephora Sentiment Project Report_AN.Rmd`.
  3. Change working directory according to your local path - `setwd("~/path/to/your/local/directory")`.
  4. Access the dataset according to where you put you data in - `reviews <- read_csv("~/path/to/your/data")`.
  5. Run all to execute the entire analysis.

## Data Source 

This dataset `[Import Dataset]reviews_0-250.csv` contains **reviews from Sephora**, along with **other information** such as product name, skin type of the reviewer, ratings, etc. 

The dataset contains **602,130 observations** and **19 variables**.

## Variables Used

The primary variable of interest is the **sentiment score** expressed in each review, which captures the overall polarity and strength of sentiment (positive or negative) within the review text. This variable is used both descriptively and as the dependent variable in regression analysis to examine what features influence sentiment expression.
The explanatory variables include **a set of review- and reviewer-level characteristics** that may influence sentiment expression. See variable table below.

<img width="1047" alt="Screenshot 2025-06-24 at 3 30 42 PM" src="https://github.com/user-attachments/assets/11558926-ca99-45e9-a406-561b990c3ad3" />

## Key Analysis and Findings

This project **explores the factors associated with sentiment score in skincare product reviews by running a linear regression analysis**. The dependent variable was the normalized sentiment score of each review. The main independent variable was the review’s most dominant topic, as identified through LDA topic modeling. I also included several control variables to account for other influences on sentiment: product price, reviewer skin type, review length, and whether the review referenced social media platforms or influencers (e.g.,
TikTok, YouTube). 

The analysis found that **longer reviews** tend to be associated with **lower ratings**, while reviews focused on **“Texture, Fragrance & Makeup”** are significantly linked to **higher ratings**, which aligns with our descriptive findings previously. In contrast, product price, reviewer skin type, and mentions of social media **showed no
significant impact** on review ratings.

<img width="802" alt="Screenshot 2025-06-24 at 3 31 29 PM" src="https://github.com/user-attachments/assets/5c622c7d-7a09-4ec6-8547-7cbdb420d87b" />

## Limitation

1. The dataset is heavily skewed, with over 80% of reviews being positive, limiting the ability to analyze negative sentiment.
2. Only one year of data is included, preventing analysis of trends or changes over time.
3. Temporal effects (e.g., product seasonality, marketing campaigns) are not accounted for in the analysis.
4. Sentiment scores are derived from the AFINN lexicon, which may not capture context, sarcasm, or nuanced expressions.
5. Many reviews are short and share overlapping vocabulary, making it challenging for topic modeling to generate distinct, interpretable themes.
6. Reviewer-level data (e.g., demographics, purchase history) is unavailable, limiting the ability to control for individual heterogeneity.

