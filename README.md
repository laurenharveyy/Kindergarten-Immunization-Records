# Kindergarten-Immunization-Records

### Question 1: Which counties have the highest vaccination rates among students? The lowest?
1. Create a pivot table using the Student Data File. Make the row County and the Value a SUM of nDTP (number of students reporting DTP vaccination)<br> !['nDTP Pivot Table','Pivot Table for Sum of DTP Vaccinations'](/nDTPtable.png)
2. Copy and paste the results into another sheet
3. Create another pivot table using the Student Data File. Make the row County and the Value a SUM of n (number of students enrolled at each school) <br> !['County Number Pivot Table','Pivot Table for Students Enrolled in Each County'](/CountyNumberPivotTable.png)
4. Copy and paste just the SUM of n into the sheet next to the nDTP data. Make sure each value is aligned with the appropriate county. Create a new column and title in DTP_Rate. In the first row, input the equation =B2/C2. Use autofill or the dragging feature to extend this formula to all cells in the column.
5. Convert the resulting values in DTP_Rate into percentages using the "123" feature in the toolbar
6. Sort the percentages from largest to smallest (Z --> A) to get the counties with the highest vaccination rates. Your answer should be Colusa County (97.95%), Glenn COunty (97.76%), and Kings County (97.53%).
7. Sort the percentages from smallest to largest (A --> Z) to get the counties with the lowest vaccination rates. Your answer should be Nevada County (79.26%), Tuolumne County (83.56%), and Humboldt County (84.68%).

### Question 2: Which counties had the highest infant case rate (per 1,000)?
1. Refer to the Infant Dataset and navigate to the column titled "Case_Rate"
2. Click the drop down arrow and filter the values from Z --> A to sort the case rates from highest to lowest. Your answer should be Madera County (6.1), Imperial County (5.3), and Butte County (5.1).
