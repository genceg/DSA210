# The Impact of the development of a country on Happiness

## **Project Overview**
This project explores the relationship between the **development of a country** and **happiness scores** across countries. The HDI consists of three key components:  
- **Life Expectancy at Birth** (Health)  
- **Expected Years of Schooling** (Education)  
- **Gross National Income (GNI) per Capita** (Economic Well-being)  

By analyzing these factors, we aim to determine whether countries with higher scores in these categories tend to have higher happiness levels.

##  Hypotheses
1. **Null Hypothesis (H₀):** Development of a country do not significantly influence happiness scores.  
2. **H₁—HDI:** Countries with higher **Human Development Index** scores report higher average happiness.
3. **H₂—Comfort Index:** Countries with climates closer to an ideal 22 °C (“comfort index”) report higher happiness than those with more extreme average temperatures.  
4. **H₃—Sports Success:** Countries with higher **average FIFA ranking points** report higher happiness due to greater national pride.  
5. **H₄—Physical Activity:** Countries with higher **physical activity participation rates** report higher happiness, reflecting better health and social well-being.  
6. **H₅—Internet Use:** Countries with higher **Internet use** report higher happiness through improved connectivity and information access.  
7. **H₆—Income Inequality:** Countries in the **low-inequality** category (Gini < 30) report higher happiness than medium (30–40) and high (> 40) inequality countries.

## Methods
1. **Data Processing**  
   - Load & filter each dataset for years 2014–2024  
   - Compute **ComfortIndex**, **RollingFIFA**, **ActivePct**, **InternetGrowth**, **GiniCat**  
   - Merge all on `Country` & `Year`  
2. **Exploratory Data Analysis**  
   - Histograms & boxplots of each transformed variable  
   - Correlation heatmap across all predictors & happiness  
   - PCA to uncover latent dimensions of development  
3. **Hypothesis Testing**  
    Test each hypothesis like:  
  **H₀**: [Factor] does not significantly influence happiness scores.  
  **H₁**: [Factor] has a significant positive relationship with happiness scores.  
  - **H₀/H₁ for HDI**: Life Expectancy, Education, and GNI per Capita collectively have no effect vs. a positive effect on happiness.  
  - **H₀/H₁ for ComfortIndex**: ComfortIndex is unrelated vs. positively related to happiness.  
  - **H₀/H₁ for FIFA rankings**: FIFA rankings have no effect vs. a positive effect on happiness.  
  - **H₀/H₁ for ActivePct**: Physical activity rate is unrelated vs. positively related to happiness.  
  - **H₀/H₁ for Internet use**: Internet use has no effect vs. a positive effect on happiness.  
  - **H₀/H₁ for Gini**: Income‐inequality category has no effect vs. significant differences in happiness. 

4. **Data Visualization**
- **Histograms & Box Plots** → Examine the distributions of transformed variables (ComfortIndex, RollingFIFA, ActivePct, InternetGrowth, HDI) and compare happiness across categories (e.g., GiniCat, HDI quartiles, climate zones).  
- **Scatter Plots** → Plot each continuous predictor (HDI, ComfortIndex, RollingFIFA, ActivePct, InternetGrowth) against happiness scores, including fitted trend lines.  
- **Correlation Heatmap** → Display a heatmap of pairwise correlation coefficients among all predictors and happiness to identify multicollinearity and strongest associations.  
- **World Heatmaps** → Map geographic variations in both key predictors (e.g., HDI, ComfortIndex) and happiness scores to highlight regional patterns.  

5. **Conclusion**
According to the p-tests, all of the p-scores for each hyptohesis is less than 0.05, which means that for each case (HDI, Comfort Index, FIFA Rankings, Physical Actvities, Internet Usage, Income Inequality), the null hypothesis (H₀) is rejected. In short, H₁,H₂,H₃,H₄,H₅, and H₆ are valid.
