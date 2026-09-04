# Exploratory Data Analysis (EDA)

## 1. Overview

This project focuses on exploring an e-commerce dataset to understand customer purchasing behaviour, order values, product performance, order patterns, and marketing activity.

The analysis involved examining numerical and categorical variables, identifying unusual values, studying trends over time, and exploring relationships between variables using Python.

### Tools Used

- Python
- Pandas
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## 2. Numerical Distribution Analysis

### Total Order Value

The distribution of `Total_Price` was right-skewed. Most orders had relatively lower total values, while a smaller number of orders had much higher values.

This suggests that the dataset contains many smaller-value orders alongside fewer high-value orders.

![Total Price Distribution](images/Total_price.png)

### Unit Price

`Unit_Price` was relatively evenly distributed across its range, with no single price range dominating the dataset.

This suggests that orders were spread across products with different price levels rather than being concentrated around one particular price range.

### Quantity

The `Quantity` variable ranged from 1 to 5 items per order. The frequencies were relatively similar across the different quantities, with no strong preference for one quantity.

This indicates that customers made both smaller and relatively larger quantity purchases.

### Items in Cart

`Items_In_Cart` showed an approximately bell-shaped distribution. The most common cart size was around 5 items, while very small and very large cart sizes were less frequent.

This suggests that customers generally tend to have a moderate number of items in their carts.

![Items in Cart Distribution](images/items_in_cart.png)

---

## 3. Categorical Analysis

### Payment Method

Online payment was the most frequently used payment method, followed closely by cash. Debit Card, Credit Card, and Gift Card were used at relatively similar frequencies.

This indicates that customers use a variety of payment methods, with online payment being slightly more popular.

![Payment Method](images/payment_method.png)

### Order Status

Order statuses were relatively evenly distributed. Cancelled orders were the most frequent at 250, while Delivered orders were the least frequent at 231.

The relatively high number of cancelled and returned orders may be worth monitoring, although the dataset does not provide the reasons for these outcomes.

![Order Status](images/order_status.png)

### Referral Source

Instagram was the most common referral source with 259 orders, followed by Email with 250. Referral was the least common source with 222 orders.

This shows that customers came through a range of referral channels, with Instagram having a slight lead.

![Referral Source](images/referral_source.png)

### Coupon Code

Coupon usage was fairly balanced. `FREESHIP` was the most frequently used coupon code with 313 orders, while `SAVE10` was the least used with 286 orders. There were also 309 orders with no coupon.

The relatively small differences suggest that no single coupon code overwhelmingly dominated usage.

### Product

The number of orders across products was relatively balanced. Printer had the highest number of orders at 181, while Phone had the lowest at 156.

This suggests that demand was distributed across the different products rather than being concentrated on one product.

![Product Order Count](images/product_order.png)

---

## 4. Trends Over Time

Monthly order counts, total order values, and average order values were examined from January 2023 to June 2025.

Order activity and order values fluctuated from month to month rather than following a consistent upward or downward pattern.

June 2024 recorded the highest monthly total order value at **68,068.54**, while April 2023 recorded the lowest at **27,751.71**.

These fluctuations could be further investigated using additional business information such as promotions, product availability, or marketing activities.

![Monthly Order Count](images/monthly_order_count.png)

![Monthly Total Order Value](images/monthly_total_order_value.png)

---

## 5. Correlation Analysis

Correlation analysis was used to examine the strength and direction of relationships between the numerical variables.

The strongest positive relationship was between `Unit_Price` and `Total_Price`, with a correlation of **0.717**. `Quantity` also had a positive relationship with `Total_Price`, with a correlation of **0.615**.

There was also a positive relationship between `Quantity` and `Items_In_Cart` at **0.650**.

In contrast, `Quantity` and `Unit_Price` had almost no relationship (**0.015**), while `Unit_Price` and `Items_In_Cart` also showed almost no relationship (**0.001**).

These results suggest that unit price and quantity are important factors associated with total order value. However, correlation indicates association and does not prove that one variable causes another.

The correlation analysis was supported by a correlation matrix and scatter plots in the Jupyter Notebook.

---

## 6. Business Comparisons

### Product and Total Order Value

Chair had the highest combined total order value at **195,620.11**, closely followed by Printer at **195,612.61**. Phone had the lowest at **151,722.39**.

This provides an indication of which products are associated with higher overall order values and can support decisions around inventory and promotional planning.

![Product vs Total Order Value](images/product_total_order_value.png)

### Order Status and Total Order Value

Cancelled orders had the highest combined total order value at **276,396.21**, followed by Pending orders at **256,328.15**. Delivered orders had the lowest at **242,600.32**.

However, these values represent the total value attached to orders in each status. They should not be interpreted as actual revenue or losses because the dataset does not contain sufficient payment or refund information.

### Referral Source and Total Order Value

Orders attributed to Instagram had the highest combined total order value at **275,285.45**, while Referral had the lowest at **226,815.58**.

This suggests that Instagram is an important channel within the dataset and may be worth monitoring as part of the business's marketing activities. However, the analysis does not establish that Instagram caused the higher order value.

![Referral Source vs Total Order Value](images/referral_source_total_order_value.png)

---

## 7. Outlier Investigation

The IQR method identified **8 potential high outliers** in `Total_Price` and **0 potential low outliers**.

The potential high outliers were investigated rather than automatically removed. The eight orders all had a `Quantity` of 5 and relatively high unit prices. Their high total values were therefore consistent with the relationship:

`Total_Price = Quantity × Unit_Price`

Based on this investigation, the observations were considered valid-looking records and were retained in the dataset.

This demonstrates that an outlier is not automatically a data error and should be investigated before deciding whether to remove it.

---

## 8. Key Business Insights

1. Most orders were relatively low-value, while a smaller number of high-value orders created a right-skewed distribution.
2. Chair and Printer had the highest combined total order values, while Phone had the lowest.
3. Monthly order values fluctuated considerably, with June 2024 recording the highest total order value during the period analysed.
4. Order statuses were fairly balanced, although Cancelled was the most common status.
5. Instagram was the leading referral source by both order count and combined total order value.
6. Unit Price had the strongest positive correlation with Total Price, followed by Quantity.
7. Customer cart sizes were generally concentrated around moderate values, with 5 items being the most common cart size.
8. The identified high-value outliers were investigated and retained because they appeared to be legitimate observations rather than data errors.

---

## 9. Conclusion

The EDA provided a clearer understanding of customer purchasing behaviour, order values, product performance, marketing sources, and order patterns.

The analysis also demonstrated the importance of investigating unusual values and considering business context before making conclusions.

Overall, the dataset showed varied customer purchasing behaviour, fluctuating order values, and several areas that could be explored further by the business.

---

## Project Files

- `EDA.ipynb` – Jupyter Notebook containing the complete analysis
- `Cleaned_Data.csv` – Cleaned dataset used for the analysis
- `images/` – Selected visualizations from the analysis
