
**Churn Prediction for Fundraising Organization**

**Project Overview**  
This project involves building a churn prediction model for a fundraising organization. The organization provided a dataset on March 2, 2020, and the model is intended to predict which donors are most likely to churn by October 25, 2020. The results of this prediction will inform a targeted campaign to retain donors. The effectiveness of the campaign will be assessed over the following year.

**Objectives**  
1. **Create a Basetable:** Combine multiple tables provided by the organization to create a unified dataset that can be used for modeling.
2. **Develop Predictive Models:** Use different machine learning algorithms, including Artificial Neural Networks (ANN), Random Forest, and Logistic Regression, to predict donor churn.
3. **Compare Model Performance:** Assess and compare the performance of the models, particularly in terms of their ability to identify the top 20% of donors most likely to churn.

**Data Description**  
The data is split across multiple tables:

- **Extrel:** Contains information about all donors, including unique identifiers, activity codes, start and end dates of relationships, and activity descriptions.
- **Nameaddr:** Contains socio-demographic information such as titles, postcodes, and preferred mailing language.
- **Payhistory:** Records payment history for each donor, including payment amounts, dates, payment types, and payment statuses.
- **Communication:** Logs all communication between donors and the organization, including contact dates, media types, and the direction of communication (incoming or outgoing).

**Key Variables**  
- **Independent Variables:**
  - **Frequency:** Number of donations during the independent period.
  - **Recency:** Time (in days) since the last donation.
  - **Monetary Value:** Total and average donation amount per donor.
  - **Paytype:** Indicators for whether a donor has used different payment methods.
  - **Languagecode:** Preferred mailing language of the donor.
  - **Complaints (CLASCODE):** Whether the donor has ever filed a complaint.
  - **Communication Direction (CONTDIREC):** Whether any communication was incoming.
  
- **Dependent Variable:**
  - **Churn:** Defined for both partial churn (decreased activity) and complete churn (no activity).

**Methodology**

**1. Data Preparation**  
- **Time Windows:** 
  - Independent period: Up to March 2, 2020.
  - Dependent period: From March 3, 2020, to October 25, 2020.
- **Subsetting:** Donors who started their relationship before or on the end of the independent period and have not ended their relationship before the start of the dependent period were retained.
- **Feature Engineering:** Created features such as frequency, recency, total/average donations, payment types, preferred mailing language, and communication indicators.
- **Imputation:** Missing values were replaced with zero, and an additional variable was created to flag where imputation was performed.

**2. Model Building**  
- **Algorithms Used:**
  - **Logistic Regression:** A baseline model to predict the probability of churn.
  - **Random Forest:** An ensemble method that builds multiple decision trees and merges them to get a more accurate and stable prediction.
  - **Artificial Neural Networks (ANN):** A deep learning model that captures complex patterns in the data.

**3. Model Evaluation**  
- **Performance Metrics:** The models were evaluated based on their ability to identify the top 20% of donors most likely to churn, focusing on precision and recall.
- **Comparison:** The performance of the models was compared to select the best approach for the fundraising campaign.

**Results**  
The results of the models were compared, and the most effective model was selected based on its predictive power and ability to correctly identify donors at risk of churning. The selected model will be used to guide the upcoming retention campaign.

**How to Use**  
1. **Data Preprocessing:** Ensure that the data is cleaned, and the basetable is prepared according to the specified time windows and criteria.
2. **Model Training:** Train the models (Logistic Regression, Random Forest, and ANN) using the provided scripts.
3. **Model Evaluation:** Compare the models based on the specified performance metrics.
4. **Scoring:** Use the best-performing model to score the current customer base.
5. **Campaign Execution:** Implement a targeted campaign based on the scores to retain high-risk donors.

**Dependencies**  
- Python 3.x
- Pandas
- NumPy
- Scikit-learn
- Keras/TensorFlow (for ANN)
- Matplotlib/Seaborn (for visualization)

**Conclusion**  
This project provides a comprehensive approach to predicting donor churn using multiple machine learning algorithms. The insights derived from this analysis will help the fundraising organization better allocate resources and focus on retaining the most valuable donors.

---

This version uses **bold** text to highlight key sections and is organized for clarity. It should maintain its formatting when copied and pasted.
