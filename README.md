# Customer Churn Analysis, Forecasting and Visualization using Python, SQL, and Tableau

Profit is the primary motivator for any business, and one effective way to maximize profits is by focusing on customer retention. Retaining existing customers should be a key priority for businesses, as a [Forbes study](https://www.forbes.com/councils/forbesbusinesscouncil/2022/12/12/customer-retention-versus-customer-acquisition/) shows that acquiring a new customer can cost 5 to 7 times more than retaining an existing one.

What is Customer Churn?
Customer churn refers to the phenomenon where customers or subscribers stop engaging with a company or service, also known as customer attrition. It is commonly referred to as the loss of clients or customers.

Customer churn analysis helps businesses understand why customers leave by identifying key patterns and risk factors. By analyzing factors like contract length, customer service interactions, and monthly charges, companies can pinpoint dissatisfaction drivers and take proactive measures to improve customer experience. This insight enables businesses to refine their pricing models, enhance customer support, and introduce loyalty programs to retain valuable customers.

Customer churn prediction takes this a step further by using machine learning models to forecast which customers are most likely to leave. By leveraging historical data, predictive models can identify at-risk customers in real time, allowing businesses to intervene with targeted retention strategies, such as personalized offers or improved service plans. This approach helps reduce revenue loss and improves long-term customer satisfaction.

This project analyzes customer churn data and provides insights using **SQL**, **Python**, and **Tableau**. It also includes a **forecasting module** to predict future churn trends.


## 📊 Data

The dataset used in this project is a **telecom customer churn dataset** called **Databel**. This dataset is publicly available on [Kaggle](https://www.kaggle.com/datasets/yichienchong/databel-telecom-customer-churn-dataset). It features detailed customer information and churn data from a telecom company, providing valuable insights for analyzing and forecasting customer retention trends.


## 📌 Prerequisites

Ensure you have the following installed:

- Python 3.x
- Jupyter Notebook
- PostgreSQL
- Kaggle API
- Tableau (to open and analyze `.twb` and `.twbx` files)


## 📥 Installing Dependencies

To install the required Python libraries for this project, create a virtual environment and use the `requirements.txt` file:

### Step 1: Create a Virtual Environment

Create a virtual environment to isolate dependencies for this project:

```bash
python -m venv churn-env
```

### Step 2: Activate the Virtual Environment

**On Windows:**
```bash
.\churn-env\Scripts\activate
```

**On Mac/Linux:**
```bash
source churn-env/bin/activate
```

### Step 3: Install Dependencies
Use the requirements.txt file to install all the required libraries:

```bash
pip install -r requirements.txt
```
This will install the necessary libraries listed in the requirements.txt file.


## 🔑 **Storing Credentials Securely (config.py)**

To keep your credentials secure, make sure to store them in a `config.py` file. Here's how:

1. Create a new file named `config.py` in the root directory.
2. Store sensitive information (such as database credentials, API keys, etc.) in this file:

```python
# config.py

DB_HOST = "your_host"
DB_PORT = "your_port"
DB_NAME = "your_database_name"
DB_USER = "your_username"
DB_PASSWORD = "your_password"

KAGGLE_API_KEY = "your_kaggle_api_key"
```


## 🔧 Step 1: Setting Up the Database

Open `notebooks/Data_Cleaning_and_Preparation.ipynb` and run all the cells to:

- Preprocess the data.
- Create the PostgreSQL database.
- Load the preprocessed data into the database.


## ⚙️ Step 2: Running the Notebooks 

### **SQL-Based Analysis**

Open `notebooks/SQL_Analysis.ipynb` and execute the SQL queries provided in the notebook to analyze churn patterns and extract actionable insights.

The analysis is focused on four main categories: **Customer Demographics Analysis, Service Usage & Plan Analysis, Customer Support Interaction Analysis, and Churn Reason & Category Analysis**. This notebook will:

- Querying the database to extract key insights regarding churn trends.
- Identifying key factors contributing to customer churn based on historical data.
- Providing strategic recommendations to aid in business decision-making. 📈💡 

### **Analysis & Forecasting Churn**

Open and execute `notebooks/Churn_Rate_Analysis_and_Forecasting.ipynb`.

This notebook will:
- Create the database and tables if they don’t exist.
- Load the processed data into the database.
- Perform data analysis, churn forecasting, and provide actionable insights.

  This section is divided into two primary subsections: **Exploratory Data Analysis (EDA)** and **Customer Churn Rate Forecasting**. 📈

   **Exploratory Data Analysis (EDA)**:
  
   A variety of EDA techniques are employed, including:
   - Statistical analysis
   - Outlier detection and exploration
   - Univariate and bivariate analysis

   It concludes by extracting **key insights and actionable solutions** by analyzing various churn drivers through **a broad set of questions**. 📈

   **Customer Churn Rate Forecasting**:
  
   - The data is thoroughly explored to determine the most appropriate model types based on the dataset’s characteristics and the business problem.
   - After preprocessing, the data is fed into a *CatBoost model*, where we analyze feature importance and assess classification results.
   - This provides a robust understanding of churn patterns and future predictions. 📈💡 


## 📊 Step 3: Opening Tableau Workbooks

To view and analyze the data in Tableau:

1. Open **Tableau Desktop/Public**.
2. Navigate to the `tableau/` folder in the project directory.
3. Open the `.twb` or `.twbx` file to explore the dashboards.


## 💡 Step 4: Key Insights and Business Actions

- Our analysis reveals critical factors driving customer churn, highlighting issues in service usage, plan structures, customer support interactions, and churn motivations. Customers with shorter account tenures show lower service usage but still face significant charges, suggesting a potential mismatch between pricing and perceived value. Those with international plans churn slightly less, but high international usage leads to substantial extra charges, which could be a source of dissatisfaction. Moreover, customers on unlimited data plans consume far more but are not necessarily retained better, indicating that value perception, rather than sheer data limits, influences retention. High-churn states may require localized strategies, while low local call usage correlates with high churn, suggesting that less-engaged customers are at risk.

- Customer support interactions strongly impact churn, with a drastic rise in churn for those making multiple service calls. Month-to-month contracts, paper check payments, and direct debit users exhibit the highest churn, especially when combined with multiple service calls, signaling frustration with billing and service experiences. Furthermore, churn reasons reveal that dissatisfaction, competitor offers, and pricing are dominant drivers. Attitude-related churn reaches 100%, indicating that negative service interactions are deal-breakers. Dissatisfaction with product offerings, network reliability, and customer service expertise also contribute significantly, showing gaps in perceived value and support.

- To combat churn, businesses should enhance customer engagement early, improving perceived value for new customers while introducing targeted retention offers for at-risk segments. Addressing high extra international charges, optimizing unlimited data pricing, and improving customer service—especially for high-contact users—are crucial. Offering proactive support and ensuring contract flexibility can reduce churn, while payment incentives can shift customers away from high-risk payment methods. Lastly, deeper analysis into state-wise churn patterns and competitor offerings can help refine localized strategies, ultimately improving customer satisfaction and retention.

**Strategic Business Actions:**

- Improve Customer Support Quality: Train staff, monitor sentiment, and offer proactive escalations.
- Encourage Longer-Term Contracts: Offer discounts and rewards for One-Year and Two-Year plans.
- Promote Digital Payments: Incentivize Credit Card usage to reduce churn risk.
- Personalize Retention Strategies: Identify high-risk customers based on service calls, contract type, and payment method, and offer targeted interventions.
- Monitor Competitor Offerings & Price Sensitivity: Adjust pricing and service features to remain competitive.


### 📩 Connect With Me
If you're interested in discussing this project or opportunities, feel free to connect! 🚀

💼 LinkedIn: [https://www.linkedin.com/in/nedaetebari/]