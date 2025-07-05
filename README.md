# POWER-BI-PROJECT
A Power BI project analyzing employee attrition using visual and data modeling

## ANALYSIS PERFORMED IN EXCEL
The Palmora Group's emp-data was uploaded to Excel to assign gender to the blank space in the gender column.
- The =COUNTBLANK(B:B) function was executed in a cell outside the data set to determine how many blank cells were present, and it returned 43. It was divided into two, 21.5, I assigned 22 Males and 23 females.

## ANALYSIS PERFORMED IN POWER BI
The Palmora Group's emp-data CSV  was uploaded and transformed(Mechanics Workshop)
A filter was used to remove (null) from the salary column and the department column to ensure 100% column quality. The location column was changed to (Region).
Keep Rows(keep top rows), then 946 was input; this was done to make sure the (null) did not return. I Close & Apply.
The Bonus Rules file was also taken to the mechanic workshop to transform it.
All the column was selected to unpivot them.
A unique relationship was created between the 2 tables by creating a Custom Column called (Dept_Rating)
- Dept_Rating=[Department]&"/"&[Attribute]
- The Custom Column was also created for Palmora Group's emp-data
- Dept_Rating=[Department]&"/"&[Rating]
- Merge Queries as new was used to merge the 2 tables(Dept_rating) was chosen as the relationship that exists between the 2 datasets.
- The Bonus Mapping was filtered, and only the value was selected. The column name was changed to Bonus Rate.
- For the staff who are not rated, the value was replaced with 0.
- Another Custom Column was created: ANNUAL BONUS =[Salary]*[Bonus Rate].
- For each staff, Total Salary, including Bonus, CUSTOM COLUMN(TOTAL PAY)=[Salary]+[Annual Bonus]
- The CONDITIONAL COLUMN was created to show the pay distribution of employees by a band of $10,000.

## MEASURE CREATED
- Gender Count = DISTINCTCOUNT('PB DATA'[Name])
- Average Rating by Gender = (PB DATA'[Rating]








