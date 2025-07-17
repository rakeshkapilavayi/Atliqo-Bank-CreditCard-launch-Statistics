## AtliQo Bank Credit Card Launch

### Table of Contents

* [Business Problem](#business-problem)
* [Project Objective](#project-objective)
* [Phase 1: Data-Driven Target Market Identification](#phase-1-data-driven-target-market-identification)
* [Phase 2: Pilot Launch & Validation](#phase-2-pilot-launch--validation)
* [Data Description](#data-description)

  * [Customer Table](#customer-table)
  * [Credit Score Table](#credit-score-table)
  * [Transactions Table](#transactions-table)
* [Key Insights: From EDA](#key-insights-from-eda)
* [Tools & Tech Stack Used](#tools--tech-stack-used)
* [How to Run the Notebook](#how-to-run-the-notebook)
* [Files and Structure](#files-and-structure)

---

### Business Problem

AtliQo Bank, a new player in the Indian banking sector, is preparing to launch its first credit card product. In a highly saturated and competitive market, the bank seeks to differentiate itself by precisely targeting the right customer segment using historical customer, transaction, and credit profile data.

The core challenge lies in identifying the most promising customer group whose financial behavior and credit readiness align with the bank’s risk and profitability expectations. By understanding key customer attributes—such as income levels, credit scores, transaction trends, and spending behavior—AtliQo Bank intends to craft a personalized credit card offering.

---

### Project Objective

To identify a high-potential customer segment suitable for the launch of a new credit card by analyzing customer demographics, financial behavior, and credit attributes using a two-phase approach.

---

### Phase 1: Data-Driven Target Market Identification

* **Data Cleaning:** Handling missing values and ensuring consistency.
* **Distribution Analysis:** Evaluating normality and skewness of financial indicators.
* **EDA (Exploratory Data Analysis):** Understanding behavioral and financial trends.
* **Outlier Treatment:** Addressing extreme values to improve model accuracy.
* **Visualization:** Summarizing insights to identify patterns and segment profiles.

---

### Phase 2: Pilot Launch & Validation

* **Trial Campaign:** Roll out the credit card to the identified segment on a small scale.
* **Hypothesis Testing:** Validate business assumptions and test response rates and credit performance statistically.

---

### Data Description

#### Customer Table

* `cust_id`: A unique identifier assigned to each customer.
* `name`: Full name of the customer.
* `gender`: Gender identity of the customer (Male or Female).
* `age`: Age of the customer, expressed in completed years.
* `location`: Geographic location where the customer resides.
* `occupation`: Primary profession or employment type (e.g., Business Owner, Consultant, Freelancer).
* `annual_income`: Reported yearly income of the customer (in standard currency units).
* `marital_status`: Current marital status (Married or Single).

#### Credit Score Table

* `cust_id`: Unique identifier assigned to each customer.
* `credit_score`: Numerical score representing the customer's creditworthiness.
* `credit_utilisation`: Ratio of credit used relative to the total credit limit.
* `outstanding_debt`: Total unpaid debt currently owed by the customer (in monetary units).
* `credit_inquiries_last_6_months`: Number of times the customer’s credit report was pulled in the last 6 months.
* `credit_limit`: Maximum credit amount allotted to the customer (in monetary units).

#### Transactions Table

* `tran_id`: Unique identifier for each transaction record.
* `cust_id`: Identifier linking the transaction to a specific customer.
* `tran_date`: Date on which the transaction was executed.
* `tran_amount`: Monetary value of the transaction.
* `platform`: E-commerce platform where the transaction occurred (e.g., Flipkart, Amazon, Shopify, Alibaba).
* `product_category`: Category of the purchased product (e.g., Electronics, Fashion & Apparel, Sports).
* `payment_type`: Mode of payment used for the transaction (e.g., PhonePe, Credit Card, GPay, Net Banking).

---

### Key Insights: From EDA

#### Insights for the Age Group 18–25

* **Customer Base Share:** Individuals aged 18–25 account for \~24.6% of the total customer base.
* **Income & Financial Background:**

  * Average annual income is below \$50,000, indicating limited earning capacity.
  * Limited credit history with low credit scores and modest credit limits.
* **Spending & Card Behavior:**

  * Credit card usage is relatively low compared to older groups, likely due to lower income and limited prior credit experience.
* **Top Spending Categories:**

  * Electronics
  * Fashion & Apparel
  * Beauty & Personal Care

These categories suggest high interest in lifestyle and aspirational spending despite limited financial leverage.

---

### Tools & Tech Stack Used

* **Programming Language:** Python
* **Environment:** Jupyter Notebook
* **Database:** MySQL (loaded via SQLAlchemy)

#### Libraries & Frameworks:

* NumPy, Pandas – Data operations
* Matplotlib, Seaborn – Visualizations
* SQLAlchemy – SQL + Python integration

#### Statistical & Analytical Techniques:

* Exploratory Data Analysis
* Distribution & Skewness Analysis
* Outlier Detection
* Hypothesis Testing

---

### How to Run the Notebook

1. Ensure you have the following files:

   * `.env` file with database credentials.
   * Required Python libraries installed: `pandas`, `sqlalchemy`, `matplotlib`, `seaborn`, etc.

2. Open `AtliQo Bank CreditCard Launch.ipynb` in Jupyter Notebook.

3. Run the notebook cells sequentially to generate insights and visualizations.

---

### Files and Structure

* `README.md` – Project overview and documentation.
* `AtliQo Bank CreditCard Launch.ipynb` – Main analysis notebook.
* `.gitignore` – Ensures sensitive files like `.env` are not committed to Git.
