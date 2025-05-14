# 📊 Remote Work Marketing Analytics Project

This project explores the effectiveness of different marketing channels in acquiring customers by analyzing a dataset with marketing spend, channel types, and new customer counts. Through a multi-phase data analytics workflow, we identify the most cost-efficient channels and visualize key insights.

---

## 🧠 Objective

To evaluate marketing performance by:
- Calculating Customer Acquisition Cost (CAC)
- Analyzing cost-efficiency across marketing channels
- Building predictive models for customer acquisition
- Presenting insights via interactive and visual dashboards

---

## 🚀 Phases of the Project

### 📌 Phase 1: Data Understanding & Cleaning
- Loaded the dataset using pandas.
- Checked for nulls, duplicates, and data types.
- Added a new column: `CAC = Marketing Spend / New Customers`.

### 📌 Phase 2: Exploratory Data Analysis (EDA)
- Descriptive statistics for each column.
- Analyzed channel-wise average spend, customer acquisition, and CAC.
- Created comparative bar plots to highlight efficiency.

### 📌 Phase 3: Feature Engineering
- Engineered a **Performance Score** to rank marketing channels:
Performance Score = 1 - (Channel_CAC / Max_CAC)
- Higher score indicates better cost efficiency.
- Created new columns: `Channel_CAC`, `Performance_Score`.

### 📌 Phase 4: Modeling
- Built a **Linear Regression model** to predict `New_Customers` from `Marketing_Spend` and `Marketing_Channel`.
- Used scikit-learn’s `Pipeline` and `OneHotEncoder`.
- Evaluation:
- **MSE** and **R²** used to assess performance.
- Baseline model performs well but has room for optimization.

### 📌 Phase 5: Dashboard & Reporting (Jupyter Notebook)
- Developed an in-notebook dashboard using matplotlib and seaborn.
- Created summary statistics and visuals to support conclusions.

#### 📈 Visual Outputs:
1. **Average CAC by Channel (Bar Plot)**  
 ![Bar Plot](docs/barplot.png) *(Replace with actual image in GitHub or export from notebook)*  
 Shows the average CAC per marketing channel. Helps identify efficient performers.

2. **Marketing Spend vs. New Customers (Scatter Plot)**  
 ![Scatter Plot](docs/scatterplot.png)  
 Reveals that spend doesn’t guarantee acquisition—channel strategy matters.

3. **CAC vs Performance Score (Heatmap)**  
 ![Heatmap](docs/heatmap.png)  
 Displays both cost and performance rankings per channel in one view.

4. **Performance Summary Table**  
 | Channel           | Total Spend | New Customers | CAC    | Score |
 |-------------------|-------------|----------------|--------|--------|
 | Social Media      | $15,000     | 300            | $50.00 | 1.00   |
 | Email Marketing   | $9,000      | 200            | $45.00 | 0.92   |
 | Paid Search       | $18,000     | 150            | $120.00| 0.35   |
 *(Values are examples — replace with actual)*

---

### 📌 Phase 6: Documentation & Packaging
- Project is modular and organized.
- README explains each phase.
- Dashboard and visuals are notebook-compatible.
- Ready for deployment, sharing, or showcasing.

---

## 💡 Key Insights

- **Email Marketing** and **Social Media** had the lowest CACs and highest performance scores.
- Simply increasing spend is not a guarantee of acquiring more customers.
- Modeling shows that customer acquisition can be reasonably predicted using spend and channel data.
- Data-driven decisions can significantly reduce acquisition costs.

---

## 🧪 Tech Stack

- **Language:** Python 3.9+
- **Libraries:** pandas, seaborn, matplotlib, scikit-learn, ipywidgets
- **Environment:** Jupyter Notebook
- **Optional Dashboard:** Streamlit
