1. Dataset Overview:
Loaded Titanic dataset (891 rows, 12 columns).Checked first few rows, data types, unique values, and non-null counts. Dataset contains both categorical (Sex, Embarked, Pclass) and numerical (Age, Fare, SibSp, Parch) features.

2. Summary Statistics:
PassengerId, Survived, Pclass, Age, SibSp, Parch, Fare → numeric.
Age: mean around 30, but ~20% values are missing.
Fare: median around 14.45, distribution is right-skewed (few very high fares).
SibSp and Parch: mostly 0–1, but some outliers with larger numbers.

3. Missing Values:
Cabin: ~77% missing → unusable without heavy preprocessing.
Age: ~20% missing → can be imputed using median, mean, or predictive models.
Embarked: very few missing → can be imputed with most common port (“S”).

4. Value Counts (Categorical Features):
Sex: ~65% male, 35% female. Pclass: 3rd class most common. Embarked: Mostly “S” (Southampton).
Survived: ~38% survived, 62% did not.

5. Distributions (Histograms & Boxplots): Age: Bell-shaped but slightly skewed; children and older passengers present.
Fare: Strong right skew (few very expensive tickets).
SibSp & Parch: Most values are 0, some outliers with large family sizes.

6. Relationships Between Features (Scatter & Correlation):
Correlation heatmap shows:
Fare negatively correlated with Pclass (-0.55) → higher-class tickets are more expensive. SibSp positively correlated with Parch (+0.41) → families traveling together. Weak correlations between survival and numeric features directly, meaning categorical + interactions matter more. Scatter plots reveal some clusters by class/fare.

7. Outliers (IQR Method): Fare has many outliers (rich passengers, luxury tickets). Age has few outliers (elderly passengers). SibSp and Parch show extreme outliers (very large families).

8. Key Inferences: Cabin column is not reliable (too many missing values). Age and Embarked require imputation before modeling. Fare is skewed → log transformation may help for ML models. Class and Gender are strong predictors (to be verified in survival plots).
Outliers exist in Fare, SibSp, and Parch but reflect real-world cases, not errors.
