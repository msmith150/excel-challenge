# Crowdfunding Campaign Data Analysis

This project involves analyzing a dataset of 1,000 crowdfunding campaigns to uncover trends in the success and failure of campaigns across different categories. The dataset provides detailed information about the campaigns, including financial goals, funding outcomes, backer counts, categories, and more. The analysis aims to provide valuable insights into how crowdfunding success is determined and the factors that contribute to campaign success.

## Background

Crowdfunding platforms like Kickstarter and Indiegogo have gained significant popularity over the years. These platforms allow individuals and organizations to raise funds for various projects, but not all projects are successful. Understanding the trends in successful campaigns can provide valuable insights for campaign creators and backers. This project explores the trends in crowdfunding campaigns based on factors like campaign outcome, funding goals, and backer count.

## Project Overview

The dataset includes detailed information on 1,000 crowdfunding projects, including their categories, funding goals, outcomes, and backer counts. Through this analysis, we aim to uncover key trends and statistics to understand what makes a crowdfunding campaign successful.

### Goals of the Analysis

- **Determine campaign success factors**: Identify patterns in successful vs unsuccessful crowdfunding campaigns.
- **Analyze crowdfunding goals**: Investigate how the funding goal relates to the campaign's success.
- **Understand campaign trends**: Examine how categories and sub-categories affect the success of campaigns.
- **Statistical analysis of backers**: Evaluate the number of backers for both successful and unsuccessful campaigns and analyze the data using statistical metrics.

## Files

The following files are included in the project:

- `sample_projects.xlsx`: Contains the main dataset of 1,000 crowdfunding campaigns.
- `data_analysis_report.docx`: Report summarizing the analysis and findings.
  
## Instructions

### 1. Data Preparation

- **Conditional Formatting**: Apply conditional formatting to fill cells in the 'Outcome' column with different colors based on the campaign outcome (e.g., successful, failed, canceled, or live).
- **Percent Funded Column**: Create a new column that calculates how much money a campaign raised relative to its funding goal.
- **Average Donation Column**: Add a column to calculate the average donation per backer for each campaign.
- **Split Category & Sub-Category**: Create two new columns: `Parent Category` and `Sub-Category`, by splitting the existing `Category` and `Sub-Category` columns.

### 2. Pivot Tables & Charts

- **Category Stats**: Create a pivot table to analyze the success/failure/cancellation status of campaigns in each category. Then, create a stacked-column pivot chart filtered by country.
- **Subcategory Stats**: Create another pivot table to analyze the status of campaigns by sub-category. Follow with a stacked-column pivot chart filtered by country and parent category.
  
### 3. Date Conversion

- **Date Conversion**: Use a formula to convert Unix timestamps in the `launched_at` and `deadline` columns into standard Excel date formats. Create new columns `Date Created Conversion` and `Date Ended Conversion` to store these converted dates.

### 4. Outcome Analysis by Launch Date

- **Outcomes Based on Launch Date**: Create a pivot table showing the outcomes (success/fail/cancel/live) grouped by the `Date Created Conversion`. Filter by parent category and years. Then, create a line chart to visualize this data.

### 5. Goal Analysis

- **Crowdfunding Goal Analysis**: Create a table with goal ranges and analyze the success, failure, and cancellation rates for each goal range. Populate the table using the `COUNTIFS()` formula to count how many projects were successful, failed, or canceled within each goal range. Then, create a line chart to visualize the relationship between goal amount and success/failure rates.

### 6. Statistical Analysis

- **Backer Count Analysis**: Create a new worksheet to analyze the number of backers in successful vs unsuccessful campaigns. Calculate the following statistics for each group:
  - Mean number of backers
  - Median number of backers
  - Minimum and maximum number of backers
  - Variance and standard deviation
  
Use these statistics to assess the variability of backers in successful and unsuccessful campaigns and determine whether the mean or median provides a better summary of the data.

## Insights and Findings

### Conclusions Drawn from the Data

1. **Over 75% of crowdfunding campaigns were US-based.**
2. **The majority of successful crowdfunding campaigns are related to entertainment (e.g., film & video, music, theater).** Furthermore, the majority of all crowdfunding campaigns fell into these categories.
3. **Length of campaign time does not appear to be a predictor of meeting the stated goal.** For example, the highest percentage raised came from a two-day campaign.
4. **Over half (24 out of 46) of all food truck-related crowdfunding campaigns either failed or were canceled.**

### Limitations of the Dataset

1. The “blurb”, “staff pick” and “spotlight” values are not defined and could be helpful.
2. The Launch Date pivot table is too broad to draw any significant conclusions.
3. It appears that the amounts in “goal” and “amount pledged” are in different currencies. One would need to convert to the same currency for an accurate comparison.

### Suggestions for Additional Analysis

1. **Convert the spreadsheet into a Table**: This would allow easier sorting and better visualization of relationships in the data.
2. **Insert a column for campaign length**: By calculating the difference between the `Date Created Conversion` and `Date Ended Conversion` columns, you can add this value to the pivot table to analyze whether campaign length impacts the amount raised.
3. **Add `pledged`, `goal`, and `Percent Funded` values**: Including these in the pivot table will help identify trends and relationships in campaign performance.

### Statistical Analysis of Backers

The analysis of backer counts for successful and unsuccessful campaigns shows that:

- **Mean Backers**: Successful campaigns had an average of 851 backers, while unsuccessful ones had 586 backers.
- **Median Backers**: The median backers for successful campaigns was 201, compared to 115 for unsuccessful campaigns.
- **Standard Deviation**: Successful campaigns had a higher standard deviation, indicating a greater variability in backer counts.

### Variability in Successful vs Unsuccessful Campaigns

Based on the analysis of variability metrics such as variance, standard deviation, and range, **successful campaigns had more variability** in the number of backers compared to unsuccessful campaigns. This makes sense because successful campaigns typically have more backers, with a wider spread of values, while unsuccessful campaigns tend to have fewer and more clustered backers.

## Technologies Used

- **Microsoft Excel**: For data analysis, pivot tables, and charts.
- **Microsoft Word**: For documenting the analysis and creating the report.

## How to Run the Project

1. **Download the Files**: Download the `sample_projects.xlsx` and `data_analysis_report.docx` files.
2. **Open the Excel File**: Open `sample_projects.xlsx` in Microsoft Excel to begin the analysis.
3. **Apply Conditional Formatting and Formulas**: Follow the instructions above to modify the dataset and create new columns.
4. **Create Pivot Tables and Charts**: Generate the required pivot tables and charts for the various analyses.
5. **Write the Report**: Summarize your findings in `data_analysis_report.docx`.

## Conclusion

This project provides a deeper understanding of trends in crowdfunding campaigns. By analyzing key data points such as campaign goals, outcomes, and backer count, we uncover insights into what makes a crowdfunding campaign successful. The goal is to help potential campaign creators make data-driven decisions for future crowdfunding endeavors.
