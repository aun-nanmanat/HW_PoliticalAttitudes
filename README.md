# Political Attitudes Analysis of the German Population
## Project Overview
Conducted a comprehensive analysis of political attitudes among German citizens using data from the European Social Survey (ESS). Focused on key political variables to understand the ideological landscape and voter behavior.

## Key Variables
- **freehms:** Opinions on the freedom of gay men and lesbians to live as they wish.

- **euftf:** Views on European unification.

- **wrclmch:** Concern about climate change.

- **gincdif:** Agreement on government measures to reduce income differences.

- **imueclt:** Attitude towards the cultural impact of immigration.

- **lrscale:** Self-placement on the left-right political spectrum.

- **impcntr:** Opinion on allowing immigrants from poorer countries.

- **prtvfde2:** Political party voted for in the last national election.

## Analytical Methods
- **Data Preparation:** Cleaned and processed data, handled missing values, and selected relevant variables.

- **Exploratory Data Analysis (EDA):**
  - Characterized voter distribution on the left-right scale across different political parties using boxplots.
    
  - Analyzed opinions on European unification across political affiliations.
    
  - Investigated the relationship between cultural attitudes and immigration perspectives using scatter plots and heatmaps.

- **Correlation Analysis:** Calculated the correlation coefficient between cultural attitudes and immigration perspectives, revealing a strong negative correlation.

- **Principal Component Analysis (PCA):**

  - Reduced dimensionality to identify key components influencing political attitudes.
    
  - Visualized the explained variance and variable loadings to interpret principal components.

- **Logistic Regression:**

  - Built a logistic regression model to predict voting behavior based on political attitudes.

  - Analyzed model performance using confusion matrices, ROC curves, and AUC scores.

## Results and Insights
- **Left-Right Scale:** Demonstrated distinct political orientations among different parties, with Die Linke, Grünen, and SPD on the left, and CDU/CSU, FDP, and AfD on the right.

- **European Unification:** Found consistent mean values indicating shared sentiments across most parties, with the Greens showing a more positive view.

- **Cultural Attitudes and Immigration:** Identified that those who perceive cultural life as enriched by immigrants are more open to allowing more immigrants, while those who feel it is undermined prefer fewer immigrants.

- **PCA Findings:** Highlighted key dimensions such as cultural enrichment and skepticism towards EU unification as influential in political attitudes.

- **Logistic Regression Performance:** Achieved a high AUC score of 0.84, indicating strong model performance in distinguishing between left and non-left voters.

## Visualizations
Created detailed visualizations including boxplots, scatter plots, heatmaps, PCA biplots, and ROC curves to enhance the interpretability of findings.

## Skills Demonstrated: 
- Data cleaning and preparation

- Exploratory Data Analysis (EDA)

- Correlation and PCA

- Logistic regression modeling

- Data visualization with Python (Matplotlib, Seaborn)

- Statistical analysis and interpretation

## Conclusion
This project showcases my ability to handle complex datasets, apply various analytical techniques, and derive meaningful insights from data. It highlights my proficiency in using Python for data analysis and my capability to communicate findings effectively through visualizations.

# Data

This repo contains a subset of the [European Social Survey (ESS)](https://www.europeansocialsurvey.org/) data. The ESS tracks the behaviours, attitudes, and beliefs of individuals across European countries. By now, there are 10 survey waves covering a period from 2002 to 2020. We will work only with the latest wave and restrict ourselves to a subset of the questions concerning some political attitudes among German citizens. 

In particular, we consider the following items 

| Item | Question |
|---|---|
| `freehms` | Gays and lesbians free to live life as they wish | 
| `euftf` | European unification go further or gone too far |
| `wrclmch` | How worried about climate change | 
| `gincdif` | Government should reduce differences in income levels |
| `imueclt` | Country's cultural life undermined or enriched by immigrants |
| `lrscale` | Placement on left right scale | 
| `impcntr` | Allow many/few immigrants from poorer countries outside Europe |
| `prtvfde2` | Party voted for in last national election 2, Germany |

The questions are typically answered via Likert-type scale. 
For example, `lrscale` contains numbers 0 to 10 that encode the individual's self-placement from left (0) to right (10). The variable `prtvfde2` contains numbers that encode the relevant parties in the german political landscape. See
https://ess-search.nsd.no/variable/query/prtvfde2/1

The instructions below focus on `python` but the exercises can be solved in `R` as well, of course.

# Exercises

## Preparation

- Clone this repository to your local machine
- Create a quarto document to write your report in
- Load the data
- Define the missing data (look up the corresponding numbers used for "No Answer", "Refuse Answer", ... in the documentation of each variable!). For now, we do not need to filter out missing data.

## Exploration

In this first task we want to explore the dataset and create some visualisations.

### Task 1a: Characterising voters

Create a boxplot of the `lrscale` variable grouped by party that the individuals voted for (`prtvfde2`).

Try adjusting the colours of the boxplot to match the typical colours of the parties:

| party | colour | 
| --- | --- |
| CDU/CSU (conservative) | black | 
| SPD (social democrat) | red |
| Linke (Left) | purple | 
| Grünen (Green) | green |
| FDP (Liberals) | yellow |
| AfD (right-wing populist) | blue | 

> Tip: This can be done quite neatly in seaborn's `sns.boxplot(...)` by providing the `palette` argument with a dictionary containing the responses and the corresponding colours `{1: "black", ...}`. Also, adjust the tick labels!

Do the same exploratory analysis with a different variable and explain your observations to someone who is unfamiliar with the political landscape in Germany.

### Task 1b: Exploration and visualisation of two variables.

#### Scatterplot 

This analysis aims to explore the variables and their dependencies in the dataset. Let's focus on two variables, say `imueclt` and `impcntr`.

First, produce a scatter plot where each point corresponds to a data point in the `impcntr` - `imueclt` plane. This probably looks pretty uninformative. Why? Explain!
Also try setting the transparency of the data points to a very small value, e.g. `alpha=0.01`. 

#### Heatmap

Let's do a better job by creating a heatmap of the data (or a 2D histogram). 
First, create a nice (pivoted) table which contains the number of responses for each set of values in `imueclt` (index/rows) and `impcntr` (columns). Include this table in your report.

> Tip: you can use pandas' `pivot_table` or a combination of grouping and pivoting (unstacking).

Now, plot this table as a heatmap, using for example, `sns.heatmap(...)`.

Describe your observations! 

#### Correlation

Finally, report the correlation coefficient of the two variables and briefly interpret it.


