
# Sales Analysis Dashboard

## Overview
This dashboard provides insights into sales, products, and customer trends, leveraging multiple data sources and transformation steps to present a comprehensive view of the business.

## Data Sources
1. **DIM_Calendar**: Provides date-related attributes, sourced from `DIM_Calendar.csv`.
2. **DIM_Customers**: Contains customer-related details, sourced from `DIM_Customers.csv`.
3. **DIM_Products**: Details about various products, sourced from `DIM_Products.csv`.
4. **FACT_InternetSales**: Sales data related to products and customers, sourced from `FACT_InternetSales.csv`.
5. **SalesBudget**: Budgeted sales amounts for different dates, sourced from `SalesBudget.xlsx`.

## Data Transformation Steps
1. **DIM_Calendar**: 
   - Columns selected: DateKey, Date, Day, Month, MonthShort, MonthNo, Quarter, Year.
   - Filter applied: Data from the year 2019 onwards.
   
2. **DIM_Customers**: 
   - Columns selected: CustomerKey, First Name, Last Name, Full Name, Gender, DateFirstPurchase, Customer City.
   - Additional data join: Joined with a geography table for city details.
   
3. **DIM_Products**: 
   - Columns selected: ProductKey, Product Name, Product Category, Product Color, Product Size, Product Line, Product Model Name, Product Description, Product Status.
   - Additional data join: Joined with product subcategory and category tables.
   
4. **FACT_InternetSales**: 
   - Columns selected: ProductKey, OrderDateKey, DueDateKey, ShipDateKey, CustomerKey, SalesOrderNumber, SalesAmount.
   - Filter applied: Data from the last two years.

## Update Frequency
The data in this dashboard is static and won't be updated frequently.

---

