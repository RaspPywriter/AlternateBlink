Pivot Table
Data must have column headers, it must look like a standard spreadsheet

Anatomy of a pivot table

A pivot table is made up of four areas:
Values, Rows, Columns, Filters

![image](https://github.com/RaspPywriter/ExcelDataAnalysis/edit/master/PivotTables/pivotView.png)

Before creating a Pivot Table
1.	Make sure that data is not in the column headers (ex: January – it should be month)
2.	Ensure there are not blank columns/rows. You can have some blank cells, but it’s not ideal.


Questions to ask when setting up a pivot table: 
1.	What am I measuring
2.	How do I want to see it?

Pivot Table Tools
Slicers
Timeline Slicer
Insert  Timeline Slicers
Can insert timeline slicers so that you have one pivot chart and can switch between time periods, so for the sales data it is a slicer for Orderdate
Standard Slicer
Insert  Slicer
Let’s you slice by other values, for instance state, you see the sales by state. In the case of by state, the slicer has many states, so you have to scroll. Go into Format Slicer Position and Layout  and select 3 columns. This works since the timeline slicer above is quite wide. This way it looks better visually. 
Filters
Top 10
Right click in chart, and select top 10.
Pivot Reports
Can choose Reports with Subtotals, without Subtotals, Outline Mode
Customizing Pivot Tables
Change Column Name
Click on the column name in the table and simply type in a new name. 
Group By
Multiple Values
In the case of a chart where there are many options, such as for quantity ordered, if you want to see the sales for those categories, select the pivot table and right click Group By  in this case I picked to start at 6 and go to 97 (all data points) and group by 10. 
Dates
I also used group by for a large variety of dates, I grouped by month. 
Pivot Chart
After creating a pivot chart, can click on the gray buttons on pivot chart  called pivot field buttons (can collapse and expand entire field). Can use slicer on pivot chart.
Alternatives to using pivot chart
1.	You don’t want overhead
2.	Avoid formatting limitations of pivot chart
Method 1: Turn pivot table into hard values: create pivot and copy it  select paste values from insert tab  just use values it disables by name functioning of pivot table
Method 2: Delete underlying pivot table and select the entire pivot table and press delete key
Method 3: Distribute a picture of the pivot chart 
Method 4: Use cells linked back to the pivot tables as the source data for the chart

Conditional Formatting with Pivot Tables
Home  Conditional formatting

Preprogrammed Scenarios for condition level: data bars, top Nth items, Top Nth %

Format cells based on column, values, formulas
Top or bottom ranks, create a formula to determine which cells to format.

Pivot table to more than one dataset
Go to dataset 1: insert pivot table when dialog box opens click “add this to data model”
Go to dataset2 click same box
Go to pivot table should see: active: ALL and see both datasets  select data from each table to go into the pivot table  button comes up to create relationship between data click it and create relationship table open: click manage relationship button: can create a new relationship, edit, activate, deactivate, delete relationships.

To add another table to existing pivot, add to data, no deletions or go to new table, select insert table  create connection  add to model
