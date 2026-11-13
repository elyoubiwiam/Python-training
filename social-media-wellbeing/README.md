# Social Media and Student Wellbeing

A data analysis project looking at how students' social media habits relate to their sleep, stress, mental health and grades.

I made this project to study data analysis with Python, as my portfolio project for Codecademy's Learn Python for Data Science path. My background is in cyberpsychology, so I looked at the results from that angle.

**Notebook:** [Social_Media_Wellbeing_Analysis.ipynb](Social_Media_Wellbeing_Analysis.ipynb)

## Questions

1. How much time do students spend on social media, and which platforms do they use most?
2. Is heavier daily use linked to less sleep, more stress, lower mental health and lower grades?
3. Does using social media late at night affect sleep?
4. How does social comparison relate to stress and mental health?
5. Which platforms are most often linked to a harmful or a beneficial overall impact?

## Data

**Source:** "Impact of Social Media on Life" by harishyadav0506, published on Kaggle: [Impact of Social Media on Life on Kaggle](https://www.kaggle.com/datasets/harishyadav0506/impact-of-social-media-on-life)

The dataset has 4,500 students and 16 columns, including age, gender, academic level, main platform, daily usage, sleep, stress, mental health index, GPA and overall impact. I used it for study purposes only and do not own the data. The data file is not stored in this repo. The notebook downloads it from Kaggle.

## What I did

- **Inspected** the data: data types, missing values, duplicates and value ranges.
- **Cleaned** it: removed duplicates, tidied text, filled 46 missing stress values and 85 missing GPA values with the median, and checked for impossible values.
- **Prepared** it: added new columns (usage groups, weekend hours, a low sleep flag) and used two merges (a lookup table for social comparison and a platform summary table).
- **Analysed** it: groupby, pivot tables, crosstabs, correlations and charts with matplotlib.

## Key findings

- **Heavy use and wellbeing:** heavy users (over 6 hours a day) sleep about 2 hours less, report more than double the stress and score 25 points lower on mental health than light users (under 3 hours).
- **Late-night use:** 65% of late-night users sleep under 7 hours, compared with 42% of other students.
- **Social comparison:** how often students compare themselves to others made almost no difference to stress. This goes against social comparison theory, but the data only measures how often students compare, not who they compare with or how it makes them feel.
- **Platforms:** platform made little difference. How long students spend online mattered more than which app they use.
- **Data quality:** the links are much stronger than in most published research (a correlation of -0.85 between daily use and mental health), which suggests the dataset may be synthetic.

## Tools

Python, pandas, matplotlib, Jupyter Notebook

## How to run it

1. Install [Anaconda](https://www.anaconda.com/download), which includes Python, pandas, matplotlib and Jupyter.
2. Install kagglehub by running `pip install kagglehub`.
3. Download this folder, open the notebook in Jupyter and choose **Run > Run All Cells**. The first run downloads the dataset from Kaggle.

## Limitations

- The data is self-reported and only covers students.
- The results show correlations, not causes.
- I compared group averages and correlations only. I did not test whether the differences are statistically significant.
