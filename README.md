# California Kindergarten Immunization Data Analysis

## Story 
Incoming kindergarteners in California schools, both public and private, are [required by state law](https://cchealth.org/immunization/school-requirements.php) to receive certain immunizations, such as that for Diptheria, Tetanus, and Pertussis (DTP). However, students can opt out of these required vaccinatons with Personal Belief Exemptions (PBE) given for religious or philosophical reasons, as well as Permanent Medical Exemptions (PME) given for certain medical conditions. However, the 2016-2017 school year marked the last year that incoming kindergarteners could enroll with PBEs due to the passage of [Senate Bill 277](/https://leginfo.legislature.ca.gov/faces/billNavClient.xhtml?bill_id=201520160SB277). In turn, between 2016 and 2019, there has been a 500% increase in Personal Medical Exemptions throughout the state of California, according to [KidsData](https://www.kidsdata.org/topic/748/immunizations-kindergarteners-exempt/table#fmt=1141&loc=2,127,347,1763,331,348,336,171,321,345,357,332,324,369,358,362,360,337,327,364,356,217,353,328,354,323,352,320,339,334,365,343,330,367,344,355,366,368,265,349,361,4,273,59,370,326,333,322,341,338,350,342,329,325,359,351,363,340,335&tf=124&ch=1102,1268,1103,1104,1438&sortColumnId=0&sortType=asc). Particularly, counties that reported a high percentage of students with exemptions before the legislation tended to have a significant increase in reported PMEs. 

Therefore, my story will focus on vaccine exemption trends in California counties over time. Specifically, it will compare pre-legislation exemptions with post-legislation exemptions in order to determine how Senate Bill 277 has changed vaccination patterns. Additionally, by consulting with experts on the issue, I will determine key drivers of high exemption rates (such as religious beliefs and [unfounded concerns regarding the link between vaccines and autism](https://www.thelancet.com/journals/lancet/article/PIIS0140-6736(97)11096-0/fulltext)). Particular emphasis will be placed on counties that have sustained high exemption rates before and after the legislation, such as Nevada County.

*Note: Data for post-Senate Bill 277 will focus on the 2018-2019 school year, which represents the most recent data reported by the California Department of Public Health*

***Interviewees***

Source | Contact | Description
-------| --------|------------
Dr. Ninez Ponce | Email: nonponce@uclas.edu <br> Phone: (310) 794-2691 | Dr. Ninez Ponce is the principal investigator at the [California Health Interview Survey](https://healthpolicy.ucla.edu/chis/Pages/default.aspx), which conducts surveys throughout the state of California in order to gather health related data. Based on her multidisciplinary research, she can speak to broader trends and possible behavioral patterns contributing to an unwillingness to get vaccinated.
Leah Russin | Email 1: press@vaccinatecalifornia.org <br> Email 2: info@vaccinatecalifornia.org <br> Twitter: [@LeahinCA](https://twitter.com/leahinca?lang=en)| Leah Russin is a leader at [Vaccinate California](https://vaccinatecalifornia.org/about/), a parent advocacy group that encourages statewide vaccination through volunteer efforts. She can speak on the difficulties of her advocacy and trends she has noticed in what is driving continued exemption rates, even after the passing of Senate Bill 277.


***Document Sources***
Source | Description
------ | -----------
[KidsData](https://www.kidsdata.org/topic/748/immunizations-kindergarteners-exempt/table#fmt=1141&loc=2,127,347,1763,331,348,336,171,321,345,357,332,324,369,358,362,360,337,327,364,356,217,353,328,354,323,352,320,339,334,365,343,330,367,344,355,366,368,265,349,361,4,273,59,370,326,333,322,341,338,350,342,329,325,359,351,363,340,335&tf=124&ch=1102,1268,1103,1104,1438&sortColumnId=0&sortType=asc) | KidsData has updated data on vaccination and exemption rates from the California Department of Public Health. It also has analysis of trends that have occurred after the passage of Senate 277. This will further inform and support my analysis of the data.
[Research Report](https://jamanetwork.com/journals/jama/fullarticle/2652640) by Paul L. Delameter, et al | This research report demonstrates a correlation between counties with high Personal Belief Exemptions pre-2016 and high increases in Permanent Medical Exemptions post-2016. This will help support my analysis of exemption trends before and after California’s ban on Personal Belief Exemptions. 

## Data Visualizations: Exemption Rates Before and After Senate Bill 277

[!['Pre Senate Bill 277 Visualization','Visualization of Exemptions by County before Senate Bill 277'](/DataViz1(1).png)](https://datawrapper.dwcdn.net/uViB8/9/)

[!['Post Senate Bill 277 Visualization','Visualization of Exemptions by County after Senate Bill 277'](/DataViz2(2).png)](https://datawrapper.dwcdn.net/hKlu5/4/)

## Data Analysis

### Question 1: Which counties had the highest percentage of incoming kindergarteners with the DTP vaccination between the 2000-2001 and 2015-2016 school years? Which counties had the lowest?
1. Create a pivot table using the Student Data File. Make the row County and the Value a SUM of "nDTP" in order to determine the number of incoming kindergarteners with DTP vaccinations in each county <br> !['nDTPcounty','Pivot Table for Sum of DTP Vaccinations by County'](/nDTPcounty.png)
2. Copy and paste the results into another sheet titled "DTP_Vax"
3. Create another pivot table using the Student Data File. Make the row County and the Value a SUM of "n" in order to determine the number of incoming kindergarteners enrolled in each County. <br> !['ncounty','Pivot Table for Students Enrolled in Each County'](/ncounty.png)
6. Copy and paste the results into the "DTP_Vax" sheet. Make sure each value is aligned with the appropriate county. 
7. Create a new column in the "DTP_Vax" sheet and title it "DTP_Rate." I put mine in Column D. My sheet looks like thi: s<br> !['DTPcountyratesheet',DTP vaccination rates by county sheet'](/DTPcountyratesheet.png)
8. Divide the number of students vaccinated against DTP by the total number of students enrolled in each county. I went to cell D2 input the equation "=B2/C2." Use autofill or the dragging feature to extend this formula to all cells in the column. Convert the resulting values in DTP_Rate into percentages using the "123" feature in the toolbar
10. Sort the percentages from largest to smallest (Z --> A) to get the counties with the highest percentage of incoming kindergarteners with the DTP vaccination. Your answer should be Colusa County (97.95%), Glenn County (97.76%), and Kings County (97.53%).
11. Sort the percentages from smallest to largest (A --> Z) to get the counties with the lowest percentage of incoming kindergarteners with the DTP vaccination. Your answer should be Nevada County (79.26%), Tuolumne County (83.56%), and Humboldt County (84.68%).

### Question 2: Which counties had the highest percentage of incoming kindergarteners with vaccine exemptions, including both Personal Belief Exemptions (PBEs) and Permanent Medical Exemptions (PMEs)? Calculate for the span between the 2000-2001 and 2015-2016 school years.
1. Create a pivot table in the Student Data File. Make the row "County" and the value a SUM of "nPBE" in order to determine the total number of incoming kindergarteners with PBEs in each county. <br> !['PBE Pivot Table','Pivot table of students reporting PBE in each county'](/PivotPersonalBelief.png)
2. Copy and paste your results into a new sheet called "Exemptions." 
3. Create a new pivot table. Make the row "County" and the value a SUM of "nPME" in order to determine the total number of students with PMEs in each county. <br> !['PME Pivot Table','Pivot table of students reporting PME in each county'](/PivotPermanentMedical.png)
4. Copy and paste your results into the "Exemptions" sheet.
5. Create a new pivot table. Make the row "County" and the value a SUM of "n" for the total number of incoming kindergarteners enrolled in each county. <br> !['Enrollment Pivot Table','Pivot table of incoming Kindergareners enrolled in each county'](/ncounty.png)
6. Copy and paste your results into "Exemptions." My sheet looks like this: <br> !['Exemption Sheet','Screenshot of Exemption Sheet'](/exemptionsheetbefore.png)
7. Create a new column titled "Exemption_Rate." I made mine in column F. Add together the SUM of PBE and the SUM of PME and divide by the SUM of n. For instance, in cell F2, I input the equation "=(B2 + C2)/D2." Extend the equation to all cells in the column. Use the "123" feature to convert to a percentage.
8. Sort "Exemption_Rate" from Z-->A to get the highest percentages on top. The top 3 should be Nevada County, Trinity County, and Siskiyou County. Here are my answers: <br> !['Exemption Results','Screenshot of Google Sheet with exemption results'](/exemptionsheetafter.png)

### Question 3: What percent of incoming Kindergarteners in each county had PBEs? What percent had PMEs?
1. Refer to the "Exemptions" sheet in the Student Data File.
2. Create two new columns titled "PercentPBE" and "PercentPME." Mine are in columns G and H, respectively.
3. Under "PercentPBE," divide the SUM of PBE by the SUM of n. For instance, I wrote in cell G2, "=(B2/D2)." Extend the equation to all cells in the column. Use the "123" feature to convert to a percentage. 
4. Under "PercentPME," divide the SUM of PME by the SUM of n. For instance, I wrote in cell H2, "=(C2/D2)."  Extend the equation to all cells in the column. Use the "123" feature to convert to a percentage. 
5. These are my results (refer to columns G and H): <br> !['Percentages of PBE and PME by County','Screenshot of Google Sheet that shows percentage of incoming kindrgarteners with PBE and PME by county'](/exemptionsheetpt2.png)

### Question 4: Did Public or Private Schools have a higher percentage of incoming kindergarteners with exemptions, including PBEs and PMEs?
1. Refer to the Student Data File.
2. Create a new pivot table. Set the row as "schoolType" and the value as a SUM of "n" (the number of enrolled students). This will give you the number of students enrolled at private and public schools, respectively. <br> !['schooltypeenrollmentpivottable','Pivot table of enrollment by school type'](/schooltypenrollmentpivottable.png)
3. Copy and paste the results into a new sheet titled "School_Type."
4. Create another pivot table. Set the row as "schoolType" and the value as a SUM of "nPBE" (number of Personal Belief Exemptions). This will give you the number of students with Personal Belief Exemptions at private and public schools, respectively. <br> !['schooltypePBEpivottable','Pivot table of number of students with PBE by school type'](/schooltypePBEpivottable.png)
5. Copy and paste the results into the "School_Type" sheet.
6. Create another pivot table. Set the row as "schoolType" and the Value as a SUM of "nPME" (number of Permanent Medical Exemptions). This will give you the number of students with Personal Medical Exemptions at private and public schools, respecitvely. <br> ![schooltypePMEpivottable','Pivot table of number of students with PME by school type'](/schooltypePMEpivottable.png)
7. Copy and paste the results into the "School_Type" sheet.
8. In the "School_Type" sheet, create a new column titled "Exemption_Percent." I did this in column F. My sheet looks like this: <br> !['schooltypeexemptionsheet1','Screenshot of Exemption Sheet Format'](/exemptionpercent.png)
9. In the first cell under "Exemption_Percent," add together the number of PMEs and PBEs and divide this total by the total number of students enrolled (this calculation is for private school students). For instance, in cell F2 (in the "Exemption_Rate" column), I inserted the equation "(C2+D2)/B2)." 
10. Extend this equation to all cells in "Exemption_Percent" to calculate for public schools as well.
11. Highlight the column and use the "123" feature to convert your values to percentages. 
12. You should have an exemption rate of 3.23% at private schools and 1.81% at public schools.
13. The answer: Private schools have a higher exemption rate. <br> ![Schooltypeexemptions',Vaccine Exemptions by School Type'](/exemptionpercent2.png)

### Question 5: What percent of Exemptions were Personal Belief Exemptions? Calculate the results by school type (public school vs. private school).
1. In the "School_Type" Sheet in the Student Data File, create a new column in G titled "Percent_PBE."
2. divide the number of PBEs by the total number of exemptions (PBE + PME). For instance, in cell G2, I wrote the equation "=C2/(C2+D2)." 
3. Press enter and extend the equation to cell G3.
4. For your answer, you should get that 93.21% of exemptions were PBEs at private schools, and 91.38% of exemptions were PBEs at public schools.
!['PBEschooltype','PBE by School Type'](/PBEschooltype.png)

### Question 6: Which counties had the greatest percent increase in DTP vaccinations between the 2000-2001 and 2015-2016 school years? Greatest percent decrease?
1. Create a pivot table using the Student Data File. Make the row "County" and the Value a SUM of "nDTP" (number of students reporting DTP vaccinations). 
2. Filter by year and clear all values. Only select 2000 (for the 2000-2001 school year). <br> !['countynDTPtable','DTP vaccinations by county for the 2000-2001 school year'](/countynDTPtable.png)
3. Copy and paste the values into a new sheet titled "VaxRate_Change". Title the column "DTP_2000."
4. Go back to the same pivot table. Change the filter to only include the year 2015 (for the 2015-2016 school year). <br> !['countynDTPtable2015','DTP vaccinations by county for the 2-15-2016 school year'](/countynDTPtable2015.png)
5. Copy and paste the values into the "VaxRate_Change" Sheet. Name the column "DTP_2015."
6. Create a pivot table. Make the row "County" and the Value a SUM of "n" (number of students enrolled in each county). Create a filter for year and only select 2000 (for the 2000-2001 school year). <br> !['countyenrollmenttable2000','Enrollment by county for the 2000-2001 school year'](/countyenrollmenttable2000.png)
7. Copy and paste the values into the "VaxRate_Change" Sheet. Name the column "n2000."
8. Go back to the same pivot table. Change the filter to only include the year 2015 (for the 2015-2016 school year). <br> !['countyenrollmenttable2015','Enrollment by county for the 2015-2016 school year'](/countyenrollmenttable2015.png)
9. Copy and paste the values into the "VaxRate_Change" Sheet. Name the columnn "n2015."
10. Notice that values in "n2015" are missing for Alpine County. Insert N/A in order to indicate null values. 
11. My "VaxRate_Change" Sheet looks like this: !['DTPratesheet',DTP Numbers for Rate Calculation'](/DTPratesheet.png) <br> *Notice that column D is left blank. This is intentional, because this is where we will make rate calculations.*
12. Create a new column in "VaxRate_Change" titled "Rate2000." I did this in column D. Then, divide the DTP vaccinations by the number of enrolled students and multiply by 100. We will multiply by 100 in order to calculate the rate per 100 students for the 2000-2001 school year. For instance, in cell D2, I wrote the equation "=(B2/C2)*100." Extend your equation to all cells in the column.
16. We will now repeat this process for the the 2015-2016 school year. Create a new column titled "RATE2015." I did this in column G.  Then, divide the DTP vaccinations by the number of enrolled students and multiply by 100. We will multiply by 100 in order to calculate the rate per 100 students for the 2015-2016 school year. For instance, in cell G2, I wrote the equation "(E2/F2)*100." Extend this equation to all cells in the column. 
18. My sheet now looks like this: !['DTPratesheet2',Sheet with DTP Rate Calculations'](/DTPratesheet2.png)
19. Now, we will calculate the percent change of the rates. Create a new column  and title it "PERCENT_CHANGE." I did this in column H. We will now use the percent change equation: (New-Old)/Old * 100.  For instance, in cell H2, I wrote the equation "=(G2-D2)/D2." Extend this equation to all other cells in the column.
22. Highlight the column and use the "123" feature to convert all values to percentages.
23. Sort Column H from Z --> A. This will place the highest positive percent change values at the top. (Note: Alpine County will appear in row A. This is due to the fact that, with its null values, the equation will come back with an error message.)
24. Ommitting Alpine County, the counties with the greatest percent increase are Sierra County (26.92%), Alameda County (2.33%), and Inyo County (2.33%). ![DTPpercentincrease','Counties with greatest percent increase in DTP vaccinations'](/DTPpercentincrease.png)
25. Now sort Column H from A --> Z. This will place the counties with the lowest negative percentages (largest percent decrease) at the top. Your answer for the counties with the greatest percent decrease should be Trinity County (-14.21%), Nevada County (-11.71%), and Shasta County (-11.26%). !['DTPpercentdecrease','Counties with greatest percvent decrease in DTP vaccinations'](/DTPpercentdecrease.png)

### Question 7: Of the counties with the greatest percent decrease in DTP vaccinations among students (Trinity, Nevada, and Shasta), what was the percent change in vaccine exemptions (including both PBEs and PMEs)?
1. Create a pivot table in "Student Data." Set the row as "County" and the value as "nPBE" for the number of students with Personal Belief Exemptions for each county.
2. Create a filter for County and select only Trinity, Nevada, and Shasta.
3. Create a filter for year and choose 2000 (for the 2000-2001 school year). <br> !['Personal Belief Exemptions 2000','Pivot table of personal belief exemptions for the 2000-2001 school year'](/PBE2000.png)
4. Copy and paste your results into a new sheet titled "ExemptionChange" <br> 
5. Return to the same pivot table. Modify the filter to only include 2015 (for the 2015-2016 schoool year). <br> !['Personal Belief Exemptions 2015','Pivot table of personal belief exemptions for the 2015-2016 school year'](/PBE2015.png)
6. Copy and paste your results into a new column in the same sheet where you pasted your previous results. 
7. Create a new pivot table. Set the row as "County" and the value as "nPME" for the number of students with Permanent Medical Exsemptions for each county.
8. Create a filter for County and select only Trinity, Nevada, and Shasta.
9. Create a filter for year and choose 2000 (for the 2000-2001 school year). <br> ![Permanent Medical Exemptions 2000','Pivot table of permanent medical exemptions for the 2000-2001 school year'](/PME20001.png)
10. Copy and paste your results into a new column in the "ExemptionChange" sheet.
11. Return to the same pivot table. Modify the filter to only include 2015 (for the 2015-2016 school year). <br> ![Permanent Medical Exemptions 2015','Pivot table fo permanent medical exemptions for the 2015-2016 school year'](/PME20151.png)
12. Create a new pivot table. Set the row as "County" and the value as "n" for the number of students enrolled in each county.
13. Create a filter for County and select only Trinity, Nevada, and Shasta.
14. Create a filter for year and choose 2000 (for the 2000-2001 school year). <br> ![Enrolled students 2000','Students enrolled in each county for the 2000-2001 school year](/n2000.png)
15. Copy and paste your results into a new column in the "ExemptionChange" sheet.
16. Return to the same pivot table. Change the year filter to 2015 (for the 2015-2016 school year). <br> ![Enrolled students 2015','Students enrolled in each county for the 2015-2016 school year'](/n2015.png)
17. Copy and paste your results into a new column in the "ExemptionChange" sheet.
18. Your sheet should look like this: <br> !['Percent Change in Exemptions Sheet','Sheet layout before calculations for the percent change in vaccine exemptions'](/exemptionchangesheet.png) <br>  *Notice the empty columns. This is purposeful for the sake of necesary calculations.*
19. Create a new column called "Total2000." I did this in Column D.
20. Add together the total number of PBE and PME for the first county during the 2000-2001 school year. For instance, in cell D2, I wrote the equation "=B2+C2."
21. Extend this equation to all cells in the column.
22. Create a new column titled "Total2015." I did this in Column I.
23. Add together the total number of PBE and PME for Nevada County during the 2015-2016 school year. For instance, in cell I2, I wrote the equation "=G2+H2" in order to 
24. Create a column called "Rate2000." I did this in Column F.
25. Divide total exemptions for the 2000-2001 school year by the number of enrolled kindergarteners for that same school year. For instance, in cell F2, I wrote the equation "=(D2/E2)*100." Ths will give you the rate of exemptions per 100 students in Nevada County for the 2000-2001 school year.
26. Extend the equation to all cells in the column.
27. Create a new column called "Rate 2015."  I did this in Column K.
28. Divide total exemptions for the 2015-2016 school year by the number of enrolled kindergarteners for that same school year. For instance, in cell K2, I wrote the equation "=(I2/J2)*100." This will give you the rate of exemptions per 100 students in Nevada County for the 2015-2016 school year.
29. Extend the equation to all cells in the column.
30. Create a new column called "PCT_CHG." I did this in Column L.
31.  We will now use the percent change equation: (New-Old)/Old * 100. In cell L2, I wrote the equation "=(K2-F2)/F2." This will calculate the percent change in exemptions for Nevada County between the 2000-2001 and 2015-2016 school years. 
32. Extend the equation to all cells in the column. Use the "123" function to change the values to percentages.
34. Your sheet should look like this: <br> !['Final Results Percent Change Exemptions','Sheet that documents the final results for the calculations in the percent change of vaccine exemptions in select counties'](/exemptionchangeresults.png) <br> The answer is 188.21% in Nevada County, 500.27% in Shasta County, and 236.00% in Trinity County.

### Question 8: Which counties had the highest infant pertussis case rates (per 1,000) between 2014 and 2015?
1. Refer to the Infant Data File and navigate to the column titled "Case_Rate"
2. Click the drop down arrow and filter the values from Z --> A to sort the case rates from highest to lowest. Your answer should be Madera County (6.1), Imperial County (5.3), and Butte County (5.1). <br> ![Infant Case Rate','Pertussis Case Rates Among Infants in California Counties'](/infantcaserate.png)

### Question 9: What was the median case rate among counties for each year between 2010 and 2014?
1. Refer pertusisRates2010_2015 File.
2. Filter the cases for 2010 from Z --> A so that California is in the first row. 
3. Create a new row beneath the dataset titled "Median"
4. In your new row, go to column C. In that column, insert the equation =MEDIAN (C3:C60). This will calculate the median case rate among the counties, exempting the state of California.
5. Repeat the appropriate equation in each column with case rates.
6. Your answer should be 20.555 for 2010, 5.58 for 2011, 2.07 for 2012, 4.10 for 2013, and 17.28 for 2014. Notice that the median case rate is significantly higher in 2010 and 2014 -- the years the outbreaks occurred, according to the [Kaggle description](https://www.kaggle.com/broach/california-kindergarten-immunization-rates). <br> !['mediancaserate','Median case rates between 2010 and 2014'](/mediancaserate.png)
