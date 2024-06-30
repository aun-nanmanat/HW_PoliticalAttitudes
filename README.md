# Political Attitudes Analysis of the German Population
## Project Overview
Conducted a comprehensive analysis of political attitudes among German citizens using data from the European Social Survey (ESS). Focused on key political variables to understand the ideological landscape and voter behavior.

## Data

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
