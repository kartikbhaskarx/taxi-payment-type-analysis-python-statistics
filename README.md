# 🚕  Taxi Payment Type Revenue Analysis

_A taxi payment analytics project focused on understanding the relationship between payment type, fare amount, trip distance, and customer payment behavior._

---

## 📋 Table of Contents

- <a href="#overview">Overview</a>
- <a href="#business-problem">Business Problem</a>
- <a href="#dataset">Dataset</a>
- <a href="#tools--technologies">Tools & Technologies</a>
- <a href="#data-cleaning--preparation">Data Cleaning & Preparation</a>
- <a href="#exploratory-data-analysis-eda">Exploratory Data Analysis (EDA)</a>
- <a href="#research-questions--key-findings">Research Questions & Key Findings</a>
- <a href="#how-to-run-this-project">How to Run This Project</a>
- <a href="#project-report">Project Report</a>
- <a href="#author">Author</a>

---

<h2><a class="anchor" id="overview"></a>Overview</h2>

This project analyzes NYC taxi trip data to understand whether payment type is associated with differences in fare amount and trip characteristics.

The analysis focuses on card and cash transactions, comparing fare amount, trip distance, passenger count, and trip duration to identify observable payment and revenue patterns.

---

<h2><a class="anchor" id="business-problem"></a>Business Problem</h2>

Taxi drivers need to understand whether payment methods are associated with different fare amounts in order to identify potential opportunities to improve revenue.

---

<h2><a class="anchor" id="dataset"></a>Dataset</h2>

The project uses NYC Taxi Trip records containing trip, payment, fare, distance, passenger, and time-related information.

Relevant fields used for the analysis include:

| Field | Description |
|---|---|
| `payment_type` | Payment method used for the trip |
| `fare_amount` | Fare amount charged for the trip |
| `trip_distance` | Trip distance in miles |
| `passenger_count` | Number of passengers |
| `tpep_pickup_datetime` | Trip pickup timestamp |
| `tpep_dropoff_datetime` | Trip drop-off timestamp |

The original dataset contains more than 6.4 million trip records.

---

<h2><a class="anchor" id="tools--technologies"></a>Tools & Technologies</h2>

- Python (Pandas, NumPy, Matplotlib, Seaborn, SciPy)
- Jupyter Notebook
- Statistical Hypothesis Testing
- GitHub

---

<h2><a class="anchor" id="data-cleaning--preparation"></a>Data Cleaning & Preparation</h2>

The taxi trip dataset is cleaned and prepared for comparative analysis.

Key processing includes:

- Converting pickup and drop-off timestamps to datetime
- Creating trip duration in minutes
- Selecting relevant analytical fields
- Handling missing payment type and passenger count values
- Removing duplicate records
- Restricting the analysis to card and cash transactions
- Filtering invalid passenger counts
- Removing non-positive fare, distance, and duration values
- Removing extreme outliers using the IQR method

The analysis dataset is then used to compare card and cash payment behavior.

---

<h2><a class="anchor" id="exploratory-data-analysis-eda"></a>Exploratory Data Analysis (EDA)</h2>

The exploratory analysis focused on payment preferences, fare amounts, trip distance, passenger count, and the relationship between payment type and trip characteristics.

### Key observations

**Payment Type & Fare Patterns:**

- Card payments account for approximately 67.5% of analyzed transactions, compared with 32.5% for cash.
- Card trips show a higher average fare amount than cash trips.
- Card trips also show a slightly higher average trip distance than cash trips.

**Passenger & Trip Patterns:**

- Single-passenger trips represent the largest share of both card and cash transactions.
- Transaction proportions generally decrease as passenger count increases.
- Fare differences should be considered alongside trip distance and duration when comparing payment groups.

---

<h2><a class="anchor" id="research-questions--key-findings"></a>Research Questions & Key Findings</h2>

1. **Payment Preference:** Card payments account for approximately 67.5% of analyzed transactions, compared with 32.5% for cash.

2. **Fare Difference:** Card transactions show a higher observed average fare than cash transactions.

3. **Trip Distance:** Card transactions show a slightly higher average trip distance than cash transactions.

4. **Passenger Behavior:** Single-passenger trips represent the largest proportion of both card and cash transactions.

5. **Hypothesis Testing:** Welch's independent two-sample t-test produced a t-statistic of approximately 170.38 with a p-value effectively equal to 0, indicating a statistically significant difference in observed average fares.

6. **Business Insight:** Payment type is associated with differences in observed fare amount, making it a useful variable for further revenue analysis.

---

<h2><a class="anchor" id="how-to-run-this-project"></a>How to Run This Project</h2>

### 1. Clone the repository

```bash
git clone <repository-url>

cd taxi-payment-type-statistical-analysis
```

### 2. Install dependencies 
```bash
pip install pandas numpy matplotlib seaborn scipy jupyter
```

### 3. Run the analysis

Open the analysis notebook:

[Taxi Payment Type Revenue Analysis](./notebook/taxi_payment_type_revenue_analysis.ipynb)

Run the notebook cells sequentially to reproduce the data cleaning, exploratory analysis, visualizations, and hypothesis testing.

---

<h2 id="project-report">Project Report</h2>

The project reports are available in the `report/` directory:

[Customer Churn Analysis Report](./report/Taxi_Payment_Type_Revenue_Analysis_Report.pdf)

[Maximizing Revenue Report](./report/maximizing_revenue_report.pptx)

---

<h2 id="author">Author</h2>

**Kartik Bhaskar**

Data Analyst

**Email:** <a href="mailto:karthikbhaskarx@gmail.com">karthikbhaskarx@gmail.com</a>
