# LoanTap-Case-Study
 ### Problem Definition:
   The objective of LoanTap is to determine whether a credit line should be extended to an individual based on their attributes. The key challenge is to minimize the risk of non-performing assets (NPAs) by flagging potential defaulters, while ensuring loans are disbursed to as many eligible customers as possible to maximize interest earnings.

### Final Inferences 

1. **Dataset Overview**:
   - The dataset consists of **396,030 records**, with **27 features**, including the target variable `loan_status`.
   - Distribution of the target variable:
     - **80% of loans** are classified as "Fully Paid" (class 0).
     - **20% of loans** are classified as "Charged Off" (class 1), indicating defaults.<br><br>

2. **Class Imbalance and Data Preparation**:
   - The dataset shows a significant class imbalance, which was addressed using **SMOTE (Synthetic Minority Oversampling Technique)**. This approach effectively balanced the dataset.<br><br>

3. **Loan Amount Analysis**:
   - The median loan amount is slightly **higher** for "Charged Off" loans, suggesting that larger loan amounts carry a higher risk of default.<br><br>

4. **Impact of Loan Term**:
   - Loans with a **60-month term** have a higher probability of default compared to 36-month loans, indicating longer repayment periods are riskier.<br><br>

5. **Interest Rate Analysis**:
   - The mean and median interest rates are **higher** for defaulted loans, reflecting the higher risk profile of these borrowers.<br><br>

6. **Loan Grades and Sub-Grades**:
   - Lower loan grades (**E, F, and G**) show significantly higher default probabilities, with the **G grade** having the highest risk.
   - Sub-grades exhibit a similar trend, where lower sub-grades are associated with a higher likelihood of default.<br><br>

7. **Employment Length Analysis**:
   - Employment length is a strong indicator of creditworthiness, and longer employment tenure correlates with better loan repayment behavior.<br><br>

8. **Home Ownership Status**:
   - Borrowers who **rent** show a higher probability of default, while those with mortgages or who own homes have a lower default risk.
   - This suggests that home ownership is an indicator of financial stability.<br><br>

9. **Annual Income**:
   - The median annual income is slightly higher for borrowers who have fully paid their loans. However, high-income borrowers are also present among defaulters, indicating income alone may not be a reliable predictor.<br><br>

10. **Loan Purpose Analysis**:
    - The most common loan purposes are **debt consolidation** and **credit card refinancing**.
    - Borrowers seeking loans for **small business purposes** exhibit a higher probability of default, indicating higher risk in this segment.<br><br>

11. **Debt-to-Income (DTI) Ratio and Credit Utilization**:
    - The **DTI ratio** is higher for defaulters, suggesting higher financial burdens relative to income.
    - **Revolving credit utilization** rates are also higher for defaulters, indicating potential over-leverage and financial strain.<br><br>

12. **Public Records and Bankruptcy**:
    - An increase in the number of **derogatory public records** (e.g., bankruptcies) strongly correlates with a higher likelihood of default.<br><br>

13. **Handling Missing Data and Outliers**:
    - Missing values were imputed using median values, and outliers were handled through **capping** and **log transformation**. This approach preserved the data integrity and minimized information loss.<br><br>

14. **Model Evaluation and Key Features**:
    - Logistic Regression was used as the primary model. Important predictive features include:
      - **Loan Grade**
      - **Interest Rate**
      - **Debt-to-Income Ratio**
      - **Home Ownership Status**
      - **Zip code**<br><br>

15. **ROC-AUC Performance**:
    - The model achieved a **ROC-AUC score of 0.91**, indicating strong discriminatory power. This high score suggests the model is effective in distinguishing between fully paid and defaulted loans.<br><br>

###  Actionable Insights & Recommendations

1. **Focus on Precision for Profit Maximization**:
   - As an NBFC, LoanTap should prioritize **precision** over recall. High precision reduces false positives (incorrectly predicting defaults), ensuring more eligible borrowers receive loans and maximizing interest revenue.<br><br>

2. **Adopt a Balanced Approach with Threshold Adjustment**:
   - Consider adjusting the prediction threshold based on risk tolerance. This balanced approach helps control the trade-off between approving more loans and minimizing default risks, essential for optimizing NBFC profitability.<br><br>

3. **Strengthen Verification Processes**:
   - Review the income verification process, as verified borrowers showed higher default rates. Enhanced due diligence may help reduce discrepancies and identify high-risk borrowers.<br><br>

4. **Implement Stricter Lending Policies for Renters**:
   - Borrowers who rent have a higher likelihood of default. Stricter lending criteria or additional collateral requirements could mitigate this risk.<br><br>

5. **Monitor High DTI Borrowers and Offer Financial Support**:
   - High DTI borrowers should be monitored closely. Consider offering debt counseling or consolidation options to alleviate financial strain.<br><br>

6. **Leverage Public Record Data for Risk Assessment**:
   - Incorporate the number of derogatory public records as a key factor in credit risk evaluation, as it is a strong indicator of default risk.<br><br>

7. **Adjust Loan Terms Based on Risk**:
   - Limit approvals for **60-month term loans** or adjust interest rates for longer terms to compensate for the higher risk.<br><br>

8. **Continuous Model Monitoring and Updating**:
   - To maintain model effectiveness, LoanTap should implement continuous monitoring through a performance dashboard, periodic retraining, and drift detection to adapt to new data and business changes. Additionally, incorporating a feedback loop with the credit risk team and adjusting prediction thresholds based on business goals will enhance the model’s alignment with real-world needs and improve decision-making accuracy.<br><br>

9. **Utilize High ROC-AUC Score in Credit Decision-Making**:
   - The high ROC-AUC score indicates strong model reliability. Use this performance metric to justify model-driven decisions and enhance credit approval strategies.

