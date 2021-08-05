# Kindergarten-Immunization-Records

### Question 1: Which counties had the highest DTP vaccination rates among students between the 2000-2001 and 2015-2016 school year? The lowest?
1. Create a pivot table using the Student Data File. Make the row County and the Value a SUM of "nDTP" (number of students reporting DTP vaccinations)<br> !['nDTP Pivot Table','Pivot Table for Sum of DTP Vaccinations'](/nDTPtable.png)
2. Copy and paste the results into another sheet
3. Create another pivot table using the Student Data File. Make the row County and the Value a SUM of n (number of students enrolled at each school) <br> !['County Number Pivot Table','Pivot Table for Students Enrolled in Each County'](/CountyNumberPivotTable.png)
4. Copy and paste just the SUM of n into the sheet next to the nDTP data. Make sure each value is aligned with the appropriate county. Create a new column and title in DTP_Rate. In the first row, input the equation =B2/C2. Use autofill or the dragging feature to extend this formula to all cells in the column.
5. Convert the resulting values in DTP_Rate into percentages using the "123" feature in the toolbar
6. Sort the percentages from largest to smallest (Z --> A) to get the counties with the highest vaccination rates. Your answer should be Colusa County (97.95%), Glenn County (97.76%), and Kings County (97.53%).
7. Sort the percentages from smallest to largest (A --> Z) to get the counties with the lowest vaccination rates. Your answer should be Nevada County (79.26%), Tuolumne County (83.56%), and Humboldt County (84.68%).

### Question 2: Did Public or Private Schools have a higher rate of exemptions including Personal Belief Exemption and Permanent Medical Exemption)?
1. Refer to the dataset titled "Student Data"
2. Create a new pivot table. Set the row as "schoolType" and the value as a SUM of "n" (number of students). This will give you the number of students enrolled at private and public schools, respectively.
3. Copy and paste the results into a new sheet.
4. Create another pivot table. Set the row as "schoolType" and the value as a SUM of "nPBE" (number of Personal Belief Exemptions). This will give you the number of students with Personal Belief Exemptions at private and public schools, respectively. 
5. Copy and paste the numbers next to the data from n.
6. Create another pivot table. Set the row as "schoolType" and the Value as a SUM of "nPME" (number of Permanent Medical Exemptions). This will give you the number of students with Personal Medical Exemptions at private and public schools, respecitvely.
7. Copy and paste the numbers next to the data from nPBE.
8. In the sheet with school type, n, nPBE, and nPME, create a new column titled "Exemption_Rate." 
9. In "Exemption_Rate," add together nPBE and nPME and divide by n. Extent this equation to both cells in the column.
10. Convert your answer to a percentage. You should have an exemption rate of 3.23% at private schools and 1.81% at public schools.
11. The answer: Private schools have a higher exemption rate.
![Schooltypeexemptions',Vaccine Exemptions by School Type'](/Schooltypeexemptions.png)

### Question 3: What Percent of Exemptions were Personal Belief Exemptions by School Type (Public vs. Private School?)
1. In the same sheet with the data for School Exemptions by School Type, create a new column in G titled "Percent_PBE."
2. In cell G2, insert the equation "=C2/(C2+D2)." This will divide the number of PBEs by the total number of exemptions (PBE + PME).
3. Press enter and extend the equation to cell G3.
4. For your answer, you should get that 93.21% of exemptions were PBEs at private schools, and 91.38% of exemptions were PBEs at public schools.
!['PBEschooltype','PBE by School Type'](/PBEschooltype.png)

### New Question: Which counties had the greatest percent increase in DTP vaccinations between the 2000-2001 and 2015-2016 school years? Greatest percent decrease?
1. Create a pivot table using the Student Data File. Make the row "County" and the Value a SUM of "nDTP" (number of students reporting DTP vaccinations). Create a filter for year and only include 2000 (for the 2000-2001 school year).
2. Copy and paste the values into a new sheet in a column titled "DTP_2000"
3. Go back to the same pivot table. Change the filter to only include the year 2015 (for the 2015-2016 school year). 
4. Copy and paste the values into the same sheet. Name the column "DTP_2015."
5. Create a pivot table. Make the row "County" and the Value a SUM of "n" (number of students enrolled in each county). Create a filter for year and only select 2000 (for the 2000-2001 school year).
6. Copy and past the values. Name the column "n2000."
7. Go back to the same pivot table. Change the filter to only include the year 2015 (for the 2015-2016 school year).
8. Copy and paste the values into the same sheet. Name the columnn "n2015."
9. Notice that values in "n2015" are missing for Alpine County. Insert N/A in order to indicate null values. 
10. Your Google Sheet should look like this: !['DTPratesheet',DTP Numbers for Rate Calculation'](/DTPratesheet.png) <br> Notice that column D is left blank. This is intentional, because this is where we will make rate calculations.
11. Once you have your sheet, calculate the DTP vaccination rate for the 2000-2001 school year by dividing DTP vaccinations by the number of enrolled students. Name Column D ""Rate2000." In cell D2, insert the equation "=(B2/C2)*100." We will multiply by 100 in order to calculate the rate per 100 students. 
12. Press enter and extend the equation to all cells in the column.
13. Title Column G "RATE2015." In cell G2, insert the equation "(E2/F2)*100." Extend this equation to all cells in the column. This will give you the number of vaccination students per 100 for the 2015-2016 school year.
14. Your Sheet should look like this: !['DTPratesheet2',Sheet with DTP Rate Calculations'](/DTPratesheet2.png)
15. Now, we will calculate the percent change of the rates. Create a new column under H, and title it "PERCENT_CHANGE."
16. In cell H2, insert the equation "=(G2-D2)/D2." Extend this equation to all other cells in the column.
17. Highlight Column H and use the "123" feature to convert all values to percentages.
18. Sort Column H from Z --> A. This will place the highest positive percent change values at the top. (Note: Alpine County will appear in row A. This is due to the fact that, with its null values, the equation will come back with an error message.)
19. Ommitting Alpine County, the counties with the greatest percent increase are Sierra County (26.92%), Alameda County (2.33%), and Inyo County (2.33%)
20. Now sort Column H from A --> Z. This will place the counties with the lowest negative percentages (largest percent decrease) at the top. Your answer for the counties with the greatest percent decrease should be Trinity County (-14.21%), Nevada County (-11.71%), and Shasta County (-11.26%).

### Question 3: Which counties had the highest infant pertussis case rates (per 1,000) between 2014 and 2015?
1. Refer to the Infant Dataset and navigate to the column titled "Case_Rate"
2. Click the drop down arrow and filter the values from Z --> A to sort the case rates from highest to lowest. Your answer should be Madera County (6.1), Imperial County (5.3), and Butte County (5.1). <br> ![Infant Case Rate','Pertussis Case Rates Among Infants in California Counties'](/infantcaserate.png)

### Question 4: What was the median case rate among Counties for each year between 2010 and 2014?
1. Refer to the dataset titled "PertusisRates2010_2015"
2. Filter the cases for 2010 from Z --> A so that California is in the first row. 
3. Create a new row beneath the dataset titled "Median"
4. In your new row, go to column C. In that column, insert the equation =MEDIAN (C3:C60). This will calculate the median case rate among the counties, exempting the state of California.
5. Repeat the appropriate equation in each column with case rates.
6. Your answer should be 20.555 for 2010, 5.58 for 2011, 2.07 for 2012, 4.10 for 2013, and 17.28 for 2014. Notice that the median case rate is significantly higher in 2010 and 2014 -- the years the outbreaks occurred. 

### Question 5: Which counties had the greatest percent increase in pertussis cases between 2010 and 2014? The greatest percent decrease?
1. Refer to the dataset titled "pertusisRates2010_2015"
2. Create a new column in M titled "Percent_Change"
3. In cell M2, insert the equation "=(J2-B2)/B2)"
4. Press enter, and use autofill or the drag feature to extend the equation to all appropriate cells in the column
5. Highlight the column and select the "123" feature to convert the values to percentages
6. Filter the answers from Z --> A to get the counties with the greatest percent increase. These should be percentages with positive values. Notice that Alpine, Modoc, Sierra, and Trinity Counties have error messages due to 0 or missing values. For the counties with values, your answer should be Yolo County (752.94%), Napa County (444.0%), and Lassen County (400%).
7. Now filter the answers from A --> Z to get the counties with the greatest percent decrease. These should be percentages with negative values. Colusa, Inyo, Mariposa, and Mono Counties all have -100% due to the fact that they have 0 reported cases in 2014. We will need to further investigate whether this is due to missing data or an actual lack of cases. Among the counties with reported cases in both 2010 and 2014, those that experienced the greatet percent decrease are Merced County (-93.13%), San Luis Obispo County (-88.14%), and Del Norte County (-87.50%).
