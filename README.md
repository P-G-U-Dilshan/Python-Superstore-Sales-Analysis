# Superstore Sales & Profitability Analysis (Python)

> **Note:** You can view a summary of this project's findings on my [**LinkedIn Post**](https://www.linkedin.com/posts/pgudilshan_data-analysis-project-using-python-activity-7386260793136340992-KYsa?utm_source=share&utm_medium=member_desktop&rcm=ACoAAF-q3BUBsl-DjW0ndOchJC_uNQMSfqYydL0).

This project is an end-to-end Exploratory Data Analysis (EDA) of the popular "Superstore" dataset. The primary goal is to use Python (Pandas, Matplotlib, and Seaborn) to clean the data, analyze sales/profit trends, and identify key drivers of profitability.

---

## 🛠️ Tools Used

* **Python**
* **Pandas:** For data loading, cleaning, and manipulation.
* **Matplotlib & Seaborn:** For data visualization.
* **Jupyter Notebook:** As the development environment.

---

## 📊 Analysis Process

1.  **Data Loading & Cleaning:**
    * Loaded the `.csv` file, handling a `UnicodeDecodeError` by specifying the correct encoding (`latin1`).
    * Converted `Order Date` and `Ship Date` columns from `object` (text) to `datetime` types for time-based analysis.
    * Checked for and confirmed there were no missing values (`.isnull().sum()`) or duplicate rows (`.duplicated().sum()`).

2.  **Exploratory Data Analysis (EDA):**
    * Used `.describe()` to get a high-level statistical summary, which revealed potential issues like negative profits (losses).
    * Sorted the data to identify the top 10 most profitable and top 10 most unprofitable orders.
    * Used `.groupby()` to aggregate total profit by `Sub-Category` to understand overall performance.

---

## 💡 Key Findings & Insights

1.  **The Discount-Loss Connection:** The analysis showed a powerful and direct link between high discounts and massive losses. The top 10 most unprofitable orders all had discounts ranging from **50% to 80%**.

2.  **The "Problem Child" Category:** `Tables` was identified as the most unprofitable sub-category overall, losing the company a total of **-$17,725**.

3.  **The "Champions":** `Copiers`, `Phones`, and `Accessories` were the top 3 most profitable sub-categories, with `Copiers` alone generating **+$55,617** in profit.

4.  **The "Binders Paradox":** The `Binders` sub-category was a fascinating case. It appeared in *both* the top 10 most profitable orders *and* the top 10 most unprofitable orders.
    * **With 0% Discount:** A `Binders` order generated **+$4,946** in profit.
    * **With 80% Discount:** A `Binders` order generated **-$3,701** in profit.
    This clearly shows that the discount strategy, not the product itself, is the deciding factor.

---

## 📈 Visualization

### Total Profit by Sub-Category

The analysis includes a bar chart (which can be viewed in the `.ipynb` notebook file) that visualizes the aggregated profit for every sub-category. This clearly shows the champions (like `Copiers`) and the problem areas (like `Tables`).

---

## 🏁 Conclusion

This analysis reveals that while the Superstore has highly profitable product lines, its overall profit is significantly damaged by an aggressive and inconsistent discount strategy.

**Recommendation:** A full review of the discount policy for `Tables`, `Bookcases`, and `Binders` is highly recommended to stop the significant losses.
