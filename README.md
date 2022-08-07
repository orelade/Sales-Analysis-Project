# Sales-Analysis-Project
This is the analysis of business sales data to derive insights on sales performance.
In this project i created a data model,dax measures and columns to derive a sales insights report.
--------------------------------------------------------------------------------------------------
Orders = 'Master Sales FY'[OrderQuantity]*(RELATED(Products[ProductPrice]))
---------------------------------------------------------------------------------------------
Cost = 'Master Sales FY'[OrderQuantity]*(RELATED(Products[ProductCost]))
-------------------------------------------------------------------------
profit = 'Master Sales FY'[Orders]-'Master Sales FY'[Cost]
---------------------------------------------------------------------
Total sales amount = SUM('Master Sales FY'[Orders])
--------------------------------------------------------
Total returns Amount = SUM(Returns[Returns])
-----------------------------------------------
Total profit = SUM('Master Sales FY'[profit])
-----------------------------------------------
Total order quantity = SUM('Master Sales FY'[OrderQuantity])
-------------------------------------------------------------
Total cost = sum('Master Sales FY'[Cost])
---------------------------------------------
Revenue = 'Measures (4)'[Total sales amount]-[Total returns Amount]
---------------------------------------------------------------------
average returns = AVERAGE(Returns[Returns])
---------------------------------------------
Average orders = AVERAGE('Master Sales FY'[Orders])
-----------------------------------------------------
Returns = Returns[ReturnQuantity]*(RELATED(Products[ProductPrice]))
--------------------------------------------------------------------
