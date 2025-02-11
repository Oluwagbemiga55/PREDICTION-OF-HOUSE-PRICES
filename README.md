# House Price Prediction - Regression Analysis

![Image](https://github.com/user-attachments/assets/338b94b6-0b91-4d6d-9d98-085b2f13a51e)

## Overview
This project focuses on analyzing real estate prices using multiple regression analysis. The primary objective is to understand how various factors, such as location, amenities, and accessibility, impact property prices per unit area.

## Dataset
The dataset comprises urban real estate transaction records with the following key variables:

- **Transaction Date**: The date of property sale.
- **House Age**: Age of the property (in years) at the time of sale.
- **Distance to Nearest MRT Station**: The property's distance (in meters) to the closest Mass Rapid Transit station.
- **Number of Convenience Stores**: Number of convenience stores in the vicinity.
- **Latitude**: Geographical coordinate for north-south positioning.
- **Longitude**: Geographical coordinate for east-west positioning.
- **House Price per Unit Area**: The dependent variable representing price per unit area of the property.

## Regression Model
A multiple linear regression model was employed to assess the impact of independent variables on house prices. The regression equation is:

\[
Price = \beta_0 + \beta_1 (Transaction Date) + \beta_2 (House Age) + \beta_3 (Distance to MRT) + \beta_4 (No. of Convenience Stores) + \beta_5 (Latitude) + \beta_6 (Longitude) + \varepsilon
\]

### **Regression Statistics**
| Metric | Value |
|--------|-------|
| **Multiple R** | 0.7223 |
| **R-Squared** | 0.5217 |
| **Adjusted R-Squared** | 0.5146 |
| **Standard Error** | 10.97 |
| **Observations** | 414 |

## ANOVA (Analysis of Variance)
| Source | df | SS | MS | F-Statistic | p-value |
|--------|----|--------|--------|------------|---------|
| **Regression** | 6 | 53453.93 | 8908.99 | 73.99 | 3.81E-62 |
| **Residual** | 407 | 49008.05 | 120.41 | - | - |
| **Total** | 413 | 102461.98 | - | - | - |

## Correlation Analysis
| Variable | Correlation with House Price |
|----------|-----------------------------|
| **Distance to MRT** | -0.65 |
| **Number of Convenience Stores** | +0.48 |
| **Latitude** | +0.35 |
| **Longitude** | -0.28 |
| **House Age** | -0.12 |
| **Transaction Date** | +0.08 |

## T-Test Results
| Variable | Coefficient | Std. Error | t-Statistic | p-value | Significance |
|----------|------------|------------|------------|---------|-------------|
| **Intercept** | 3006.62 | 2501.66 | 1.2019 | 0.2301 | Not Significant |
| **Transaction Date** | 0.00257 | 0.00560 | 0.4594 | 0.6462 | Not Significant |
| **House Age** | -0.0160 | 0.0463 | -0.3457 | 0.7297 | Not Significant |
| **Distance to MRT** | -0.00866 | 0.00045 | -19.089 | 1.78E-58 | Highly Significant |
| **No. of Convenience Stores** | 1.7599 | 0.1893 | 9.2983 | 8.83E-19 | Highly Significant |
| **Latitude** | 53.4403 | 22.5646 | 2.3683 | 0.0183 | Significant |
| **Longitude** | -36.3429 | 20.1499 | -1.8036 | 0.0720 | Not Significant |

## Key Findings
- **Significant Predictors:**
  - Distance to MRT stations (**negative impact**) – most significant factor.
  - Number of convenience stores (**positive impact**) – highly significant.
  - Latitude (**positive impact**) – significant at 5% level.
- **Insignificant Predictors:**
  - House age, transaction date, and longitude do not significantly influence house prices.
- **Model Fit:**
  - The model explains **52.17% of the variance** in house prices (R² = 0.5217).
  - The overall regression model is statistically significant (F = 73.99, p < 0.001).

## Conclusion
The regression analysis highlights that **proximity to MRT stations and availability of convenience stores are the strongest determinants of house prices in urban areas**. The model provides valuable insights for real estate valuation and urban development planning.

## How to Run the Analysis
1. Install dependencies:
   ```bash
   pip install pandas numpy statsmodels matplotlib seaborn
   ```

## Future Enhancements
- Exploring non-linear regression models.
- Incorporating additional real estate factors such as crime rates and school proximity.
- Improving feature selection techniques for better model performance.

 I am open to collaboration od Data Analysis, Statistical Analysis and Visualization related projests.  you can reach me via my E-mail address(oluwagbemiga.oa55@gmail.com)

