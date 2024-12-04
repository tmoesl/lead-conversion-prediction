![EdTech Banner](references/lead_conversion_prediction_banner.png)

# Product Recommendation System For Amazon

![Status](https://img.shields.io/badge/-Completed-34A853?style=flat&label=Project&labelColor=23555555)

## Table of Contents

- [Introduction](#introduction)
- [Objective](#objective)
- [Key Business Metrics](#key-business-metrics)
- [Exploratory Data Analysis and Visualization](#exploratory-data-analysis-and-visualization)
- [Machine Learning Models](#machine-learning-models)
- [Data Insights](#data-insights)
- [Models’ Performance](#models-performance)
- [Business Recommendations](#business-recommendations)
- [Repository Structure](#repository-structure)
- [Requirements](#requirements)
- [Installation](#installation)

## Introduction
In the highly competitive EdTech industry, effectively identifying and prioritizing high-potential leads is critical for improving conversion rates and optimizing resource allocation. ExtraaLearn, a startup in this dynamic landscape, leverages machine learning to enhance lead conversion strategies. This project focuses on building predictive models to estimate conversion likelihood, complemented by analyzing behavioral patterns, demographic data, and digital engagement metrics to identify key drivers of success. The dataset includes detailed records of lead interactions across various channels, providing a robust foundation for model development.

## Objective
The primary objective of this project is to develop a robust machine learning framework to predict the likelihood of lead conversion, enabling targeted engagement and optimal resource allocation. 

**Key Objectives**
1. **Predict Lead Conversion**: Build machine learning models to estimate the likelihood of a lead converting into a paying customer, prioritizing high-potential leads.
2. **Extract Actionable Insights**: Identify the key factors driving lead conversions to support data-driven decision-making.
3. **Optimize Resource Allocation**: Design detailed lead profiles and strategies to streamline marketing and sales efforts effectively.

## Key Business Metrics
To evaluate model performance and align with business objectives, the following metrics are tracked:

**Predictive Metrics**
- **Accuracy**: Reflects overall model performance in correctly classifying leads. Higher accuracy indicates better general performance.
- **Precision**: Measures the proportion of true positives among all positive predictions, ensuring reliability in identifying converted leads, while reducing false positives.
- **Recall**: Measures the proportion of true positives among all actual conversions, ensuring reliability in capturing potential leads, while reducing false negatives.
- **F1 Score**: A harmonic mean of precision and recall, balancing the trade-off between these metrics.

**Business Key Performance Indicators (KPIs)**
- **Pages per Session**: Measures the average number of pages viewed during a single session, reflecting user engagement on the website.
- **Bounce Rate**: Indicates the percentage of visitors leaving the website without further interaction, highlighting engagement issues.
- **Lead Form Submissions**: Tracks the number of completed forms, providing insights into profile completion progress and lead generation.
- **Qualified Lead Rate (MQLs)**: Represents the percentage of leads meeting predefined marketing-qualified criteria, evaluating channel effectiveness.
- **Unique Visitors**: Measures the number of distinct individuals visiting the website, assessing the reach of targeted campaigns.
- **Cost per Lead (CPL)**: Reflects the average cost of acquiring a lead, ensuring marketing efficiency and alignment with ROI objectives.

## Exploratory Data Analysis

1. **Data Cleaning and Preprocessing**: Addressed missing values and ensured data integrity for accurate model building.
2. **Descriptive Statistics**: Analyzed lead demographics, engagement metrics, and conversion rates to identify patterns in user behavior and interactions.
3. **Uni/Multivariate Analysis**: Explored individual features and their relationships to uncover key insights on lead conversion and engagement.

## Machine Learning Models

1. **Logistic Regression**: Provides a probabilistic framework to predict lead conversion and identify key drivers.
2. **Decision Tree**: Offers interpretable decision paths while capturing non-linear relationships in the data.
3. **Random Forest**: Combines multiple decision trees for robust predictions and reduced overfitting.

## Data Insights
Data-driven insights offered a deeper understanding of lead characteristics to enhance targeted strategies and inform strategic decision-making in a competitive market.

**Demographic Insights**
- **Current Occupation**: Professionals lead with a 35.5% conversion rate, followed by unemployed individuals at 26.6%, and students at 11.7%. Tailored engagement strategies, particularly for students, can address varying expectations and behaviors.
- **Age**: Converted leads are typically older, with a median age of 54 compared to 49 for non-converted leads, highlighting the potential of targeting older demographics. The overall age range is 18 to 63 years, with a median of 51.

**Behavioral Engagement**
- **Time Spent**: Converted leads spend significantly more time on the website (median: ~13 minutes) compared to non-converted leads (median: ~5 minutes), reinforcing the correlation between extended browsing and conversion likelihood.
- **First Interaction**: Leads interacting through the website convert at 45.6%, far outperforming mobile app interactions (10.5%), underlining the website’s superior engagement potential.
- **Last Activity**: Website-related activities drive the highest conversion rate at 38.5%, followed by email at 30.3%, while phone interactions trail at 21.3%. Prioritizing website engagement is key to enhancing conversions.
- **Profile Completion**: Conversion rates increase with profile completion, from 7.5% (low completion) to 18.9% (medium) and 41.8% (high). Encouraging detailed profile completion presents a clear opportunity to boost conversion rates.

**Lead Channels**
- **Referrals**: Despite their high conversation rate of 67.7%, referrals contribute minimally to total conversions, highlighting an underutilized opportunity. 
- **Marketing Channels**: Print, digital media and educational channels perform modestly, with conversion rates between 28% and 33%.

## Models’ Performance

| Model                | Accuracy | Precision | Recall | F1 Score |
|----------------------|----------|-----------|--------|----------|
| Logistic Regression  | 0.798    | 0.618     | 0.852  | 0.716    |
| Decision Tree        | 0.777    | 0.583     | 0.889  | 0.704    |
| Random Forest        | 0.830    | 0.661     | 0.884  | 0.756    |

All machine learning models demonstrated strong performance in recall, effectively capturing a high percentage of actual conversions. However, they differ significantly in precision and overall balance, with some models offering more well-rounded metrics that better align with the business objective of optimizing lead identification and resource allocation.

1. **Logistic Regression**: This model demonstrates strong recall (0.852), capturing 85.2% of actual conversions, making it effective for identifying high-potential leads. However, its lower precision (0.618) results in 38.2% of predicted conversions being incorrect, introducing some resource inefficiencies.

2. **Decision Tree**: With the highest recall (0.889), this model minimizes missed opportunities by identifying 88.9% of actual conversions. However, its precision (0.583) is the lowest among the models, indicating a higher rate of false positives, which could necessitate additional resource allocation to manage inefficiencies.

3. **Random Forest**: Delivering the highest accuracy (0.830) and precision (0.661), this model achieves a well-rounded performance. Its recall (0.884) is strong and only marginally lower than the decision tree’s recall, highlighting minimal difference in their ability to capture actual conversions. This balance makes the random forest effective for optimizing lead identification while managing resource efficiency, aligning well with the business objective.

<div style="display: flex; gap: 10px;">
    <div style="width: 49%;">
        <img src="reports/figures/model_performance_comparison.png" alt="Model Performance" style="width: 100%;"/>
        <p><b>Figure 1:</b> Model Performance Comparison.</p>
    </div>
    <div style="width: 49%;">
        <img src="reports/figures/rf_feature_importance.png" alt="RF Feature Importance" style="width: 100%;"/>
        <p><b>Figure 2:</b> Random Forest Feature Importance.</p>
    </div>
</div>

### Key Takeaways
- ★ **Key Drivers of Conversion**: Across all models, website engagement time and the initial interaction through the website emerged as key predictors, highlighting the importance of sustained engagement and effective first touchpoints. Tree-based models also identified profile completion, recent activity, and age as significant factors in driving conversions.
- 🏆 **Best Model**: The random forest model, with a recall of 0.884 and precision of 0.661, offers the best overall balance for lead prioritization, optimizing resource allocation with a lower false positive rate.
- ⚠️ **Performance Trade-Off**: The decision tree, while offering higher recall (0.889), presents a higher false positive rate, making it less efficient for resource optimization compared to random forest.

## Business Recommendations
This set of recommendations focuses on improving lead prioritization, refining user interactions, and leveraging data-driven insights to maximize conversions and business outcomes.

1. **Enhance Website Engagement**
    - Improve user experience to encourage longer visits and more page views.
    - Simplify navigation and ensure the website is mobile-responsive and fast-loading for seamless engagement.
    - Introduce interactive features like live chat and personalized recommendations to boost engagement.
    - Track pages per session and bounce rate to measure user engagement and identify areas for improvement.
2. **Promote Profile Completion**
    - Implement gamification, progress indicators, or incentives to motivate users to complete their profiles.
    - Simplify the completion process by reducing required fields and providing clear guidance on its value.
    - Highlight the benefits of a completed profile to improve participation rates.
    - Measure success using lead form submissions to track profile completion progress.
3. **Optimize Interaction Channels**
    - Prioritize website and email interactions due to their higher conversion rates (38.5% and 30.3%).
    - Enhance mobile app functionality and engagement strategies to increase its effectiveness.
    - Focus phone-based outreach on personalized follow-ups for high-value leads.
    - Monitor the qualified lead rate (MQLs) to evaluate channel effectiveness.
4. **Targeted Marketing**
    - Customize campaigns for professionals and unemployed individuals using platforms like LinkedIn and professional networks.
    - Address lower student conversion rates by offering discounts, flexible payment plans, or course bundles integrated with institutional curricula.
    - Use demographic insights to craft messaging that resonates with specific segments.
    - Prioritize channels with proven conversion potential, as print media and educational platforms showed minimal impact in both EDA and predictive modeling.
    - Measure the impact of campaigns by analyzing traffic from targeted user segments using the unique visitors metric.
5. **Leverage Referral Programs**
    - Expand referral programs to capitalize on their high conversion effectiveness (67.7%) despite their limited contribution to overall conversions.
    - Promote referrals through social media integration, personalized email campaigns, and attractive incentives.
    - Enable seamless sharing of referral links via popular social platforms.
    - Track referral success by monitoring lead form submissions attributed to referrals.
6. **Continuous Model Improvement**
    - Regularly update and fine-tune predictive models to maintain high accuracy and adapt to changing user behaviors.
    - Use feature importance insights to refine lead nurturing strategies.
    - Align model outputs with marketing and sales goals to optimize resource allocation and maximize conversions.
    - Monitor cost per lead (CPL) to ensure alignment with ROI objectives.

## Repository Structure
```
├── LICENSE            <- Project's open-source license details.
├── README.md          <- Top-level README for developers.
│
├── requirements.txt   <- Python dependencies for replicating the environment.
├── environment.yml    <- Conda environment configuration with dependencies.
│
├── data
│   ├── processed      <- The final, processed data sets for modeling.
│   └── raw            <- The original, immutable data.
│
├── models             <- The final, trained and tuned classification model.
│
├── notebooks          <- Jupyter notebooks for data exploration and analysis.
│
├── references         <- Documentation, data dictionaries, and manuals.
│
├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
│   └── figures        <- Graphics and figures for reports.
│
├── src                <- Source code for the project.
```

## Requirements

`Python 3.11.6` or higher is required. Download the latest version here: [python.org](https://www.python.org)

## Installation

#### 1. Clone the Repository

```bash
git clone https://github.com/tmoesl/lead-conversion-prediction.git
```

#### 2. Navigate to the Project Directory
```bash
cd lead-conversion-prediction
```

#### 3. Create a Virtual Environment and Install the Required Dependencies

Using `conda`:
```bash
conda env create -f environment.yml
conda activate lead-conversion-prediction-env
```

Using `venv`:
```bash
python3.12.3 -m venv lead-conversion-prediction-env
source lead-conversion-prediction-env/bin/activate  # On Windows: .\lead-conversion-prediction-env\Scripts\activate
pip install -r requirements.txt
```
---