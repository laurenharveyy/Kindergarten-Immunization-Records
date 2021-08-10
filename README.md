# Kindergarten-Immunization-Records

## Story 
Data shows a correlation between Counties with low vaccination rates and high exemption rates — particularly Personal Belief Exemptions (given for religious or philosophical reasons) and Permanent Medical Exemptions (given for medical conditions). Particularly, Trinity County, Nevada County, and Shasta County had the greatest percent decrease in Diphtheria, Pertussis, and Tetanus (DTP) vaccinations among incoming Kindergarten students between the 2000-2001 and 2015-2016 school years. Additionally, these counties had 236%, 188%, and 500% increases in Personal Belief Exemptions and Permanent Medical Exemptions, respectively. However, following the passing of Senate Bill 277, California students are no longer to use Personal Belief Exemptions; as a result, 2016 was the last year that incoming Kindergarteners were able to register with them. According to data from the California Department of Public Health, this has lead to a 500% increase in Personal Medical Exemptions in California. 

Therefore, my story will focus on exemption trends in California counties over time. Specifically, it will compare pre-2016 exemptions with the most recent data in order to see how legislation has changed vaccination and exemption patterns.

***Sources***

1. Dr. Ninez Ponce from the California Health Interview Survey can speak to vaccination and overall public health trends in the state of California. 

Email: nponce@ucla.edu <br>
Phone Number: (310) 794-2691

2. Leah Russin from Vaccinate California works directly with vaccine initiatives in the state and can provide more insight into what is driving vaccine hesitancy and what is being done to combat it. 

Email(s): press@vaccinatecalifornia.org, info@vaccinatecalifornia.org

## Data Analysis

### Question 1: Which counties had the highest DTP vaccination rates among students between the 2000-2001 and 2015-2016 school year? The lowest?
1. Create a pivot table using the Student Data File. Make the row County and the Value a SUM of "nDTP" (number of students reporting DTP vaccinations)<br> !['nDTPcounty','Pivot Table for Sum of DTP Vaccinations by County'](/nDTPcounty.png)
2. Copy and paste the results into another sheet
3. Create another pivot table using the Student Data File. Make the row County and the Value a SUM of n (number of students enrolled at each school) <br> !['ncounty','Pivot Table for Students Enrolled in Each County'](/ncounty.png)
4. Copy and paste just the SUM of n into the sheet next to the nDTP data. Make sure each value is aligned with the appropriate county. Create a new column under D and title it "DTP_Rate." Your sheet should look like this: <br> !['DTPcountyratesheet',DTP vaccination rates by county sheet'](/DTPcountyratesheet.png) 
5. In cell D2, input the equation "=B2/C2." This will divide the number of students vaccinated against DTP by the total number of students enrolled in each county. Use autofill or the dragging feature to extend this formula to all cells in the column.
6. Convert the resulting values in DTP_Rate into percentages using the "123" feature in the toolbar
7. Sort the percentages from largest to smallest (Z --> A) to get the counties with the highest vaccination rates. Your answer should be Colusa County (97.95%), Glenn County (97.76%), and Kings County (97.53%).
8. Sort the percentages from smallest to largest (A --> Z) to get the counties with the lowest vaccination rates. Your answer should be Nevada County (79.26%), Tuolumne County (83.56%), and Humboldt County (84.68%).

### Question 2: Did Public or Private Schools have a higher rate of exemptions including Personal Belief Exemption and Permanent Medical Exemption)?
1. Refer to the dataset titled "Student Data"
2. Create a new pivot table. Set the row as "schoolType" and the value as a SUM of "n" (number of students). This will give you the number of students enrolled at private and public schools, respectively. <br> !['schooltypeenrollmentpivottable','Pivot table of enrollment by school type'](/schooltypenrollmentpivottable.png)
3. Copy and paste the results into a new sheet.
4. Create another pivot table. Set the row as "schoolType" and the value as a SUM of "nPBE" (number of Personal Belief Exemptions). This will give you the number of students with Personal Belief Exemptions at private and public schools, respectively. <br> !['schooltypePBEpivottable','Pivot table of number of students with PBE by school type'](/schooltypePBEpivottable.png)
5. Copy and paste the numbers next to the data from n.
6. Create another pivot table. Set the row as "schoolType" and the Value as a SUM of "nPME" (number of Permanent Medical Exemptions). This will give you the number of students with Personal Medical Exemptions at private and public schools, respecitvely. <br> ![schooltypePMEpivottable','Pivot table of number of students with PME by school type'](/schooltypePMEpivottable.png)
7. Copy and paste the numbers next to the data from nPBE.
8. In the sheet with school type, n, nPBE, and nPME, create a new column titled "Exemption_Rate." Your sheet should look like this: <br> !['schooltypeexemptionsheet1','Screenshot of Exemption Sheet Format'](/schooltypeexemptionsheet3.png)
9. In cell F2 (in the "Exemption_Rate" column) insert the equation "(C2+B2)/D2)." In other words, you will add together the number of PMEs and PBEs and divide this total by the total number of students enrolled (this calculation is for private school students). 
10. Extend this equation to cell F3 to calculate for public schools as well.
11. Highlight the column and use the "123" feature to convert your values to percentages. 
12. You should have an exemption rate of 3.23% at private schools and 1.81% at public schools.
13. The answer: Private schools have a higher exemption rate. <br> ![Schooltypeexemptions',Vaccine Exemptions by School Type'](/Schooltypeexemptions.png)

### Question 3: What Percent of Exemptions were Personal Belief Exemptions by School Type (Public vs. Private School?)
1. In the same sheet with the data for School Exemptions by School Type, create a new column in G titled "Percent_PBE."
2. In cell G2, insert the equation "=C2/(C2+D2)." This will divide the number of PBEs by the total number of exemptions (PBE + PME).
3. Press enter and extend the equation to cell G3.
4. For your answer, you should get that 93.21% of exemptions were PBEs at private schools, and 91.38% of exemptions were PBEs at public schools.
!['PBEschooltype','PBE by School Type'](/PBEschooltype.png)

### Question 4: Which counties had the greatest percent increase in DTP vaccinations between the 2000-2001 and 2015-2016 school years? Greatest percent decrease?
1. Create a pivot table using the Student Data File. Make the row "County" and the Value a SUM of "nDTP" (number of students reporting DTP vaccinations). Filter by year and clear all values. Only select 2000. (for the 2000-2001 school year). <br> !['countynDTPtable','DTP vaccinations by county for the 2000-2001 school year'](/countynDTPtable.png)
2. Copy and paste the values into a new sheet in a column titled "DTP_2000"
3. Go back to the same pivot table. Change the filter to only include the year 2015 (for the 2015-2016 school year). <br> !['countynDTPtable2015','DTP vaccinations by county for the 2-15-2016 school year'](/countynDTPtable2015.png)
4. Copy and paste the values into the same sheet. Name the column "DTP_2015."
5. Create a pivot table. Make the row "County" and the Value a SUM of "n" (number of students enrolled in each county). Create a filter for year and only select 2000 (for the 2000-2001 school year). <br> !['countyenrollmenttable2000','Enrollment by county for the 2000-2001 school year'](/countyenrollmenttable2000.png)
6. Copy and past the values. Name the column "n2000."
7. Go back to the same pivot table. Change the filter to only include the year 2015 (for the 2015-2016 school year). <br> !['countyenrollmenttable2015','Enrollment by county for the 2015-2016 school year'](/countyenrollmenttable2015.png)
8. Copy and paste the values into the same sheet. Name the columnn "n2015."
9. Notice that values in "n2015" are missing for Alpine County. Insert N/A in order to indicate null values. 
10. Your Google Sheet should look like this: !['DTPratesheet',DTP Numbers for Rate Calculation'](/DTPratesheet.png) <br> *Notice that column D is left blank. This is intentional, because this is where we will make rate calculations.*
11. Once you have your sheet, calculate the DTP vaccination rate for the 2000-2001 school year by dividing DTP vaccinations by the number of enrolled students. Name Column D ""Rate2000." In cell D2, insert the equation "=(B2/C2)*100." We will multiply by 100 in order to calculate the rate per 100 students for the 2000-2001 school year. 
12. Press enter and extend the equation to all cells in the column.
13. Title Column G "RATE2015." In cell G2, insert the equation "(E2/F2)*100." Extend this equation to all cells in the column. This will give you the number of vaccination students per 100 for the 2015-2016 school year.
14. Your Sheet should look like this: !['DTPratesheet2',Sheet with DTP Rate Calculations'](/DTPratesheet2.png)
15. Now, we will calculate the percent change of the rates. Create a new column under H, and title it "PERCENT_CHANGE."
16. In cell H2, insert the equation "=(G2-D2)/D2." Extend this equation to all other cells in the column.
17. Highlight Column H and use the "123" feature to convert all values to percentages.
18. Sort Column H from Z --> A. This will place the highest positive percent change values at the top. (Note: Alpine County will appear in row A. This is due to the fact that, with its null values, the equation will come back with an error message.)
19. Ommitting Alpine County, the counties with the greatest percent increase are Sierra County (26.92%), Alameda County (2.33%), and Inyo County (2.33%). ![DTPpercentincrease','Counties with greatest percent increase in DTP vaccinations'](/DTPpercentincrease.png)
20. Now sort Column H from A --> Z. This will place the counties with the lowest negative percentages (largest percent decrease) at the top. Your answer for the counties with the greatest percent decrease should be Trinity County (-14.21%), Nevada County (-11.71%), and Shasta County (-11.26%). !['DTPpercentdecrease','Counties with greatest percvent decrease in DTP vaccinations'](/DTPpercentdecrease.png)

### Question 5: Of the counties with the greatest percent decrease in DTP vaccinations among students (Ttrinity, Nevada, and Shasta), what was the percentchange in vaccine exemptions?
1. Create a pivot table in "Student Data." Set the row as "County" and the value as "nPBE" for the number of students with Personal Belief Exemptions for each county.
2. Create a filter for County and select only Trinity, Nevada, and Shasta.
3. Create a filter for year and choose 2000 (for the 2000-2001 school year). <br> !['Personal Belief Exemptions 2000','Pivot table of personal belief exemptions for the 2000-2001 school year'](/PBE2000.png)
4. Copy and paste your results into a new sheet. <br> 
5. Return to the same pivot table. Modify the filter to only include 2015 (for the 2015-2016 schoool year). <br> !['Personal Belief Exemptions 2015','Pivot table of personal belief exemptions for the 2015-2016 school year'](/PBE2015.png)
6. Copy and paste your results into a new column in the same sheet where you pasted your previous results. 
7. Create a new pivot table. Set the row as "County" and the value as "nPME" for the number of students with Permanent Medical Exsemptions for each county.
8. Create a filter for County and select only Trinity, Nevada, and Shasta.
9. Create a filter for year and choose 2000 (for the 2000-2001 school year). <br> ![Permanent Medical Exemptions 2000','Pivot table of permanent medical exemptions for the 2000-2001 school year'](/PME20001.png)
10. Copy and paste your results into a new column in the same sheet where you pasted your previous results.
11. Return to the same pivot table. Modify the filter to only include 2015 (for the 2015-2016 school year). <br> ![Permanent Medical Exemptions 2015','Pivot table fo permanent medical exemptions for the 2015-2016 school year'](/PME20151.png)
12. Create a new pivot table. Set the row as "County" and the value as "n" for the number of students enrolled in each county.
13. Create a filter for County and select only Trinity, Nevada, and Shasta.
14. Create a filter for year and choose 2000 (for the 2000-2001 school year). <br> ![Enrolled students 2000','Students enrolled in each county for the 2000-2001 school year](/n2000.png)
15. Copy and paste your results into a new column in the same sheet as the previous steps.
16. Return to the same pivot table. Change the year filter to 2015 (for the 2015-2016 school year). <br> ![Enrolled students 2015','Students enrolled in each county for the 2015-2016 school year'](/n2015.png)
17. Copy and paste your results into a new column in the same sheet as the previous steps.
18. Your sheet should look like this: <br> !['Percent Change in Exemptions Sheet','Sheet layout before calculations for the percent change in vaccine exemptions'](/exemptionchangesheet.png) <br>  *Notice the empty columns. This is purposeful for the sake of necesary calculations.*
19. In Column D, create a new column called "Total2000." 
20. In cell D2, insert the equation "=B2+C2" in order to add together the total number of PBE and PME for Nevada County during the 2000-2001 school year.
21. Extend this equation to all cells in the column.
22. In Column I, create a new column titled "Total2015"
23. In cell I2, insert the equation "=G2+H2" in order to add together the total number of PBE and PME for Nevada County during the 2015-2016 school year.
24. Title Column F "Rate2000."
25. In cell F2, insert the equation "=(D2/E2)*100." Ths will give you the rate of exemptions per 100 students in Nevada County for the 2000-2001 school year.
26. Extend the equation to all cells in the column.
27. Title column K "Rate 2015."
28. In cell K2, insert the equation "=(I2/J2*100." This will give you the rate of exemptions per 100 students in Nevada County for the 2015-2016 school year.
29. Extend the equation to all cells in the column.
30. Title Column L "PCT_CHG." 
31. In cell L2, insert the equation "=(K2-F2)/F2." This will calculate the percent change in exemptins for Nevada County between the 2000-2001 and 2015-2016 school years. 
32. Extend the equation to all cells in the column.
33. Use the "123" function to change the values to percentages.
34. Your sheet should look like this: <br> !['Final Results Percent Change Exemptions','Sheet that documents the final results for the calculations in the percent change of vaccine exemptions in select counties'](/exemptionchangeresults.png) <br> The answer is 188.21% in Nevada County, 500.27% in Shasta County, and 236.00% in Trinity County.

### Question 6: Which counties had the highest infant pertussis case rates (per 1,000) between 2014 and 2015?
1. Refer to the Infant Dataset and navigate to the column titled "Case_Rate"
2. Click the drop down arrow and filter the values from Z --> A to sort the case rates from highest to lowest. Your answer should be Madera County (6.1), Imperial County (5.3), and Butte County (5.1). <br> ![Infant Case Rate','Pertussis Case Rates Among Infants in California Counties'](/infantcaserate.png)

### Question 7: What was the median case rate among Counties for each year between 2010 and 2014?
1. Refer to the dataset titled "PertusisRates2010_2015"
2. Filter the cases for 2010 from Z --> A so that California is in the first row. 
3. Create a new row beneath the dataset titled "Median"
4. In your new row, go to column C. In that column, insert the equation =MEDIAN (C3:C60). This will calculate the median case rate among the counties, exempting the state of California.
5. Repeat the appropriate equation in each column with case rates.
6. Your answer should be 20.555 for 2010, 5.58 for 2011, 2.07 for 2012, 4.10 for 2013, and 17.28 for 2014. Notice that the median case rate is significantly higher in 2010 and 2014 -- the years the outbreaks occurred. <br> !['mediancaserate','Median case rates between 2010 and 2014'](/mediancaserate.png)
