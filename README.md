# dessert-sales-profit-dashboard

# 🍰 Dessert Profit & Loss Analysis Dashboard (Excel Project)

## 📌 Project Purpose

This project is created to analyze whether giving **50% discount on desserts**
to loyal customers will result in **profit or loss** for restaurants.

The entire analysis is done using **one Excel workbook** containing
multiple sheets, formulas, pivot tables, slicers, and interactive charts.

This dashboard helps understand:
- Customer loyalty
- Discount impact
- Restaurant performance
- Monthly profit trends
- Business profitability

---

## 📁 Workbook Structure (8 Sheets)

This Excel file contains the following sheets:

| Sheet Name | Purpose |
|------------|----------|
| Customers | Customer details and total orders |
| Restaurants | Restaurant master data |
| Desserts | Dessert cost and selling details |
| Orders | Transaction data and calculations |
| Dashboard | Main interactive dashboard |
| Total_Profit_Restaurant | Restaurant-wise profit |
| Discount_Eligible | Discount-wise profit |
| Monthly_Profit | Month-wise profit |

---

## 🗂️ 1️⃣ Customers Sheet

Contains:
- Customer_ID
- Customer_Name
- Total_Orders

Purpose:
Used to identify loyal customers (1000+ orders).

---

## 🗂️ 2️⃣ Restaurants Sheet

Contains:
- Restaurant_ID
- Restaurant_Name
- Location

Purpose:
Used for restaurant-wise analysis.

---

## 🗂️ 3️⃣ Desserts Sheet

Contains:
- Dessert_ID
- Dessert_Name
- Selling_Price
- Cost_Price

Purpose:
Used to calculate profit and cost.

---

## 🗂️ 4️⃣ Orders Sheet (Main Working Sheet)

This is the most important sheet.

Contains:
- Order_ID
- Order_Date
- Customer_ID
- Restaurant_ID
- Dessert_ID
- Quantity
- Cost_Per_Item

And 3 calculated columns:

| Column | Name | Purpose |
|--------|------|---------|
| H | Discount_Eligible | Check loyalty |
| I | Discounted_Price | Apply discount |
| J | Profit | Calculate profit |

---

## 🧮 Formulas Used (Step-by-Step Explanation)

---

### ✅ Formula 1: Discount_Eligible (Column H)

```excel
=IF(VLOOKUP(C2,Customers!A:E,5,FALSE)>=1000,"YES","NO")
````

### Purpose:

Checks whether customer has placed **1000+ orders**.

### How It Works:

1. `C2` → Takes Customer_ID from Orders sheet
2. `VLOOKUP` → Searches customer in Customers sheet
3. `5` → Fetches Total_Orders column
4. `>=1000` → Checks loyalty
5. `IF` → Returns YES or NO

### Result:

* YES → Eligible for discount
* NO → No discount

---

### ✅ Formula 2: Discounted_Price (Column I)

```excel
=IF(H2="YES",G2*0.5,G2)
```

### Purpose:

Applies 50% discount only to eligible customers.

### How It Works:

1. Checks Discount_Eligible column
2. If YES → Half price
3. If NO → Full price

### Result:

* Loyal customers get discount
* Others pay full price

---

### ✅ Formula 3: Profit (Column J)

```excel
=(I2 - VLOOKUP(E2,Desserts!A:D,4,FALSE)) * F2
```

### Purpose:

Calculates profit per order after discount.

### How It Works:

1. `I2` → Selling price after discount
2. `E2` → Dessert_ID
3. `VLOOKUP` → Fetches cost price
4. `I2 - Cost` → Profit per item
5. `* F2` → Multiply by quantity

### Result:

Shows real profit or loss.

---

## 🗂️ 5️⃣ Dashboard Sheet

This is the main interactive dashboard.

### Pivot Table Structure:

Rows:

* Customer_ID
* Restaurant_ID
* Discount_Eligible

Values:

* Sum of Profit
* Sum of Quantity
* Count of Order_ID

---

### Slicers Used:

* Discount_Eligible
* Dessert_ID
* Restaurant_ID
* Customer_ID

Purpose:
Filter and analyze data easily.

---

### Charts:

All charts are connected to pivot tables:

* Restaurant Performance
* Profit Comparison
* Discount Impact
* Sales Trends
* Quantity Analysis

Charts change automatically when slicers are used.

---

## 🗂️ 6️⃣ Total_Profit_Restaurant Sheet(Bar Chart)

### Pivot Table:

Rows:

* Restaurant_ID

Values:

* Sum of Profit

Purpose:
Identify most profitable restaurant.

---

## 🗂️ 7️⃣ Discount_Eligible Sheet(Column Chart)

### Pivot Table:

Rows:

* Discount_Eligible

Values:

* Sum of Profit

Purpose:
Compare profit from:

* Discount customers
* Non-discount customers

---

## 🗂️ 8️⃣ Monthly_Profit Sheet(Line Chart)

### Pivot Table:

Rows:

* Order_Date (Grouped by Month)

Values:

* Sum of Profit

Purpose:
Analyze monthly trends.

---

## 📊 How to Use the Dashboard

### Step 1: Open Excel File

Open the workbook.

---

### Step 2: Go to Dashboard Sheet

Open "Dashboard" tab.

---

### Step 3: Use Slicers

Click slicers to filter by:

* Customer
* Restaurant
* Dessert
* Discount

---

### Step 4: Observe Charts

See changes in:

* Profit
* Quantity
* Orders
* Revenue

---

### Step 5: Make Decision

Check whether:

✔ Discount increases sales
✔ Discount increases profit
✔ Discount causes loss

---

## 💡 Business Insights

This dashboard helps answer:

* Are loyal customers profitable?
* Which restaurant earns most?
* Does discount help business?
* Which month is best?
* Which dessert performs well?

---

## 🛠️ Tools Used

* Microsoft Excel
* VLOOKUP
* IF Formula
* Pivot Tables
* Pivot Charts
* Slicers
* Data Validation

---

## 🎯 Learning Outcome

From this project, I learned:

* Business data analysis
* Conditional logic
* Dashboard creation
* Profit calculation
* Data visualization
* Decision support system

---

## 👤 Author

**Muttukuru Madhavi**

## 📬 Contact

For feedback or queries, feel free to connect.


