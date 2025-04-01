# Sources

For this analysis, we are using the data set of Telco. The data provides us a good base to work on customer churn and understand behaviour of customers.  

# **Project Goals and Tasks**

Customer behavior and cancellations are closely linked. Churn, defined here as service cancellations, can result from various factors. Identifying these reasons can reveal opportunities to enhance the product, improve user experience, or even re-engage former customers.

The objectives of this analysis include:

- Highlighting key insights to understand churn.
- Developing a dashboard to track and visualize shifts in customer behavior.

Why are these objectives important? 

- Stakeholders need a dashboard where they can quickly see changes in customer preferences.
- Most stakeholders look at data on a high level, usually observing trends short and long term.
- Ensuring the data is presented with clear storytelling to guide conclusions.
- The dashboard serves as an addition to the exploratory analysis and allows stakeholder to understand the data insights in detail.
- Analyzing churn factors to identify features that influence retention or cancellations.

# **Description of Approach**

**Exploratory data analysis** - to visualize the current numbers, customer groups, and feature usage. To provide a dashboard with an overview, I will use Tableau. As it allows the users to further explore the data.

**Correlation analysis** examines the linear relationships between variables. Using Python, I created a heatmap visualization of customer-related features to identify patterns. Additionally, to assess whether specific features are correlated with cancellations. The primary goal is understanding how these features influence churn.

**Behavioral Pattern Analysis** allows us to focus on a group of customers. With Python, I am separating our customers from those who have canceled the service. 

# **Results**

## **Exploratory data analysis**

In our dataset, we have noticed specific groups of customers. Firstly, we are missing key information such as the subscription start date, cancellation date, and detailed product usage prior to the cancellation. Those limitations allow us to observe the data only within a few breakdowns, such as tenure, contract type, and feature usage. Tenure is the metric that allows the best overview of the customers.  

For the analysis, I split the customers into 6 groups from 0-6 months until 7+ years customers. Therefore, we can observe whether older and newer customers have different behaviour, in terms of feature usage, average spending, and total revenue.

Dashboard in [Tableau](https://public.tableau.com/app/profile/tsveti.dichevska/viz/CustomerChurnAnalysis_17431919748760/CustomerChurnAnalysis)

## **Correlation analysis**

Correlation of features used by the customers. In this heatmap, we can find the following insights: 

![my_plot.png](https://github.com/cvii-d/telco_churn/blob/main/my_plot.png)

### Churn Correlations

**Dependents**: There is a moderate negative correlation (−0.15) with churn, suggesting customers with dependents are less likely to churn.

**Tenure**: A stronger negative correlation (−0.35) indicates that customers with longer tenure are less likely to churn.

**MonthlyCharges**: A weak positive correlation (0.19) suggests that higher monthly charges slightly increase the likelihood of churn.

**TotalCharges**: A weak negative correlation (−0.20) implies that customers who have paid more over time are less likely to churn.

**InternetService**: A weak positive correlation (0.16) suggests that the type of internet service may influence churn behavior.

### Other Notable Findings

**MonthlyCharges and InternetService**: These two features have a very strong positive correlation (0.91), indicating that internet service type significantly impacts monthly charges.

**TotalCharges and Tenure**: There is a strong positive correlation (0.83), which makes sense as longer tenure leads to higher accumulated charges.

**StreamingTV and StreamingMovies**: These features exhibit a strong positive correlation (0.63), suggesting customers who use one streaming service are likely to use the other.

**OnlineSecurity and DeviceProtection**: A moderate positive correlation (0.48) shows some overlap in customers opting for these services.

## **Behavioral Pattern Analysis**

Overall, there are 4 key features that stand out for customers with cancellations: 

- 69% of customers with cancellations have used Fiber optics
- 78% have not used Online security
- 65% have not used Device protection
- 77% have not used Tech support.

From our correlation analysis, we can conclude that all those features do correlate with cancellations. 

# Conclusion

Observing the data, there is a clear pattern that the monthly charges, tenure, and certain optional features may influence whether customers stay. 

As certain groups of customers, who have stayed longer, seem to be less affected, it can be concluded that well-integrated users are more likely to stay. Whereas newer customers may have more challenges connecting with the product. 

Additionally, I can recommend extending the research with more data, related to the amount of time customers spent using the product, their user experience, interactions with customer service, and overall satisfaction.

As a result, there are opportunities the company can explore:

- Experiment with different pricing on a specific target group, eg. offer discounts for young singles.
- Provide freemium services for a limited time - test whether people are interested in them.
- Align marketing spending to target customers who are more likely to stay longer, such as seniors, people with partners, or those who use streaming for TV and movies.
