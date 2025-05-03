# Project: How do review characteristics affect the emotional tone in skincare product reviews?
**Author:** Amber Ni | **Date:** 05-02-2025 | **Course:** Text As Data: Computational Linguistics

## Project Description
This project analyzes **Sephora skincare product reviews**, focusing on sentiment analysis and thematic insights across user groups with the main research question - how specific review characteristics shape the
emotional tone of skincare product reviews on online beauty platforms like Sephora. It employs a range of **natural language processing (NLP)** and statistical techniques, following a structured workflow, **including**:
1. **Document sampling** – selected a subset of 10,000 reviews across skin types and product categories.  
2. **Text preprocessing** – tokenization, stopword removal, and lemmatization to clean raw review text.  
3. **Exploratory analysis** – visualized word frequencies using word clouds, term frequency–inverse document frequency (TF-IDF), and Log-Ratio term differences. 
4. **Sentiment analysis** – applied AFINN lexicon to assign each review a sentiment score.
5. **Topic modeling** – used Latent Dirichlet Allocation (LDA) to identify key discussion topics in reviews.
6. **Regression analysis** – assessed how sentiment is influenced by review length, topics, skin type of the reviewer, social media mentions, and product price.

The repository **includes**: 
1. R Markdown `.rmd`: Contains the full analysis pipeline, including data loading, preprocessing, visualization, sentiment analysis, topic modeling, and regression. The code is well-documented to ensure reproducibility and transparency.
2. Output codes `.html`:  The knitted output of the R Markdown file, showing the complete analysis with embedded plots, tables, and markdown explanations.
3. Project Report `.pdf`: A concise and visually structured summary of key findings, figures, and insights.
4. Output dataset `.csv`: Processed data used for regression modeling, including all variables used for the regression analysis.

## How to Use This Repository

If you'd like to **run the analysis** on your own laptop, follow these steps:
  1. Download the dataset `[Import Dataset]reviews_0-250.csv` from https://drive.google.com/file/d/1_2w39UanQFyokL21zkdlauNGjxgV0a3y/view?usp=sharing. 
  2. Open RMarkdown `PPOL6801 FinalProject Codes.Rmd`.
  3. Change working directory according to your local path - `setwd("~/path/to/your/local/directory")`.
  4. Access the dataset according to where you put you data in - `reviews <- read_csv("~/path/to/your/data")`.
  5. Run all to execute the entire analysis.

## Data Source 

This dataset `[Import Dataset]reviews_0-250.csv` contains **reviews from Sephora**, along with **other information** such as product name, skin type of the reviewer, ratings, etc. 

The dataset contains **602,130 observations** and **19 variables**.





