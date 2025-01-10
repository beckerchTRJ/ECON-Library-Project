
# **Predicting County Graduation Rates Using Library Access and Socioeconomic Data** 📚🎓

This project explores the relationship between public library access, socioeconomic factors, and high school graduation rates across U.S. counties. Using ridge and lasso regression, we identify key predictors that highlight the importance of library resources and socioeconomic conditions in driving educational outcomes.

---

## **Motivation**
Achieving a high school diploma is a critical milestone that significantly impacts long-term economic outcomes and community well-being. Public libraries, as hubs of free educational resources, play an important role in bridging gaps in resource access for underserved communities. This project investigates:
- **How do public libraries influence high school graduation rates?**
- **What role do socioeconomic factors play in this relationship?**

---

## **Data**
We analyzed county-level data from multiple sources:
- **Graduation Rates**: American Community Survey (ACS, 2022).
- **Library Metrics**: Public Libraries Survey (PLS, 2022).
- **Socioeconomic Data**: Small Area Income and Poverty Estimates (SAIPE, 2022).

Key features include:
- **Graduation rate**: High school graduation percentage by county.
- **Library access**: Metrics such as visits, circulation, and staffing per capita.
- **Socioeconomic indicators**: Poverty rate, median income, and income range.

---

## **Methodology**
We employed ridge and lasso regression to:
1. Identify the most relevant predictors of graduation rates.
2. Analyze patterns across all counties, top-performing counties, and bottom-performing counties.
3. Use regularization to handle multicollinearity and prevent overfitting.

---

## **Key Findings**
- **Socioeconomic factors dominate**: Poverty percentage is the strongest negative predictor of graduation rates.
- **Library access matters**: Central libraries and material circulation show a positive relationship with graduation rates.
- **Engagement is key**: Borrowing materials is more impactful than simply visiting the library.
- **Same problem, many reasons**: Under-performing counties may each have unique reasons behind low graduation rates that can be more difficult to model. For example, Lagrange County in Indiana has a high median income and low poverty, but a large percentage of Amish people means graduation rates remain very low.
- **Disparities remain**: The role of libraries is more significant in underserved communities but is overshadowed by broader socioeconomic challenges.

---

## **Project Highlights**
- **Data Analysis**: Aggregated and cleaned data across multiple sources for 3,218 U.S. counties.
- **Modeling**: Applied ridge and lasso regression with 20-fold cross-validation for optimal regularization.
- **Insights for Policymakers**: Highlighted the potential impact of increased library funding and targeted socioeconomic interventions.

---

## **Results**
Key predictors and coefficients:
| Feature                  | Ridge Coefficient | Lasso Coefficient |
|--------------------------|-------------------|-------------------|
| Poverty Percentage       | -2.68            | -3.00            |
| Central Libraries (per capita) | 0.86             | 0.64             |
| Circulation (per capita) | 0.63             | 0.41             |

For a detailed breakdown, check out:
- 📊 [Visualizations and Outputs](results/)
- 📄 [Full Paper](paper/library-graduation-paper.pdf) 
*Some results of paper may be outdated based off of refinements to approach*
---

## **How to Use This Repository**
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/beckerchTRJ/library-graduation-prediction.git
   cd library-graduation-prediction
   ```
2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
3. **Run the Notebook**:
   Navigate to the `notebooks/` folder and open the Jupyter Notebook to explore the analysis.

---

## **Future Directions**
- Investigate **non-linear models** (e.g., decision trees or random forests).
- Incorporate **time-series data** to capture long-term library impacts.
- Study the influence of **school and private libraries** on educational outcomes.

---

## **Acknowledgments**
This project was developed as part of ECON 460: Economic Applications of Machine Learning at the University of Southern California. Thanks to my collaborators:
- **Luke Alati**, **Dung Pham**, **Darian Ahmadizadeh**, and **Natasha Densiyuk**   
And the authors of the datasets:
- **American Community Survey** (ACS)
- **Public Libraries Survey** (PLS)
- **Small Area Income and Poverty Estimates** (SAIPE)

---

## **License**
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
