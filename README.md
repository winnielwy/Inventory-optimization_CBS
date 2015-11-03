# Inventory-optimization_CBS

Capital Bikeshare operates a pay-for-use bicycle rental program across the Washington, D.C Metro Area. Through forecasting of historic monthly bicycles trips, I found that overall system usage is very seasonal and weather dependent. Bicycles that are not needed to meet demand can be transferred to storage to reduce maintenance fees. The main tradeoff is between the cost to rent the warehouse and the repair cost, which my model will examine and produce a recommended monthly bike quantity that should be made available to customers, and determine if it is economical to rent warehouse space and transport bicycles back and forth. 

I used the AR and Winter-Additive Forecasting models to predict the number of members for each membership type and demand by trip length from May 2015 to April 2016 based on historic data from Nov 2010 to March 2015. I also calculated the Manhattan distance between the median bike station and 7 Capital BikeShare warehouses and other related variables. 
After collecting all the data, I set up an optimization model based on total profits with capacity and budget constraints using nonlinear KNITRO (in AMPL) and linear (in Excel Solver) optimization methods. 

The model recommends purchasing bicycles seasonally and selecting warehouse 4, which is the smallest and cheapest (both per square foot and total monthly cost), but has the second longest travel time compared to the other warehouse options.

In 2015, Capital Bikeshare estimates it will have an overall operating deficit of $578,186. By following my recommended inventory strategy and reducing their purchasing expenditure and maintenance expenses, Capital BikeShare could eliminate 44.5% of their operating defici
