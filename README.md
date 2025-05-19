# Lending-Club-Loan-Analysis-Borrower-Segments-Risk-Trends
This project analyzes Lending Club loan data using clustering, time series, and geospatial methods to uncover patterns in interest rates, volumes, and default risk. Tableau visualizations support strategic insights on borrower segments, regional trends, and risk management.

# Lending Club Loan Analysis: Borrower Segments & Risk Trends

This project explores borrower behavior and loan outcomes using Lending Club data. By applying clustering, time series, and geospatial analysis, it uncovers patterns in interest rates, loan volumes, and default risk. Tableau visualizations support strategic recommendations for borrower segmentation, regional trends, and portfolio risk management.

---

## Project Objectives

- Identify borrower segments using KMeans clustering
- Analyze interest rate differences by loan status
- Track changes in loan volume over time
- Explore regional loan patterns across U.S. states
- Provide actionable recommendations for risk management

---

## Key Insights

- **Conservative borrowers** are more likely to fully repay or remain current on loans.
- **Stretched borrowers** have a higher likelihood of default.
- **Fully Paid loans** are declining in recent years, while **Current loans** are rising.
- **Alaska** has the highest average loan amount; **Hawaii** the lowest.
- Seasonal and regional patterns can inform funding strategies.

---

## Analytical Methods

- **KMeans clustering** (Python - scikit-learn)
- **Data cleaning and transformation** (pandas)
- **Time series and geospatial prep** (Python & Excel)
- **Interactive visualizations** (Tableau Public)

---

## Files Included

| File | Description |
|------|-------------|
| `lending_club_loans_sample.csv` | Cleaned Lending Club loan data |
| `lending_club_clustered.xlsx` | Data prepared for cluster visualization |
| `lending_club_time_geo_ready.xlsx` | Data for time series and map visualizations |
| `Storyboard` | Tableau workbook with all visualizations and storyboards |
| `README.md` | This documentation file |

---

## Visualizations

You can view the full interactive dashboard on Tableau Public:  
🔗 [View Dashboard on Tableau Public](https://public.tableau.com/app/profile/jacques.van.rensburg/viz/LendingClubLoanAnalysisBorrowerSegmentsRiskTrends/Storyboard?publish=yes) 

---

## Tools Used

- **Python** (pandas, scikit-learn, datetime)
- **Jupyter Notebook**
- **Tableau Public**
- **Excel** (for light formatting)

---

## Future Recommendations

- Incorporate **credit scores** and **payment history** for deeper risk insights
- Use **logistic regression** to predict loan default probability
- Monitor **seasonal** and **regional** trends to align lending strategy
- Tailor loan offers based on **cluster profiles**

---

## Limitations

- Credit scores and employment history were not included
- The dataset reflects a single time snapshot
- KMeans clustering assumes fixed, equally spaced clusters
- Dataset only includes **approved** Lending Club applicants

---

## Contact

**Author:** Jacques van Rensburg  
If you have questions or suggestions, feel free to reach out via GitHub.

---
