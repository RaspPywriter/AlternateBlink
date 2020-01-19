# Pivot Table
Data must have column headers, it must look like a standard spreadsheet

## Anatomy of a pivot table

A pivot table is made up of four areas:
Values, Rows, Columns, Filters

![image](https://github.com/RaspPywriter/ExcelDataAnalysis/edit/master/PivotTables/pivotView.png)

### Before creating a Pivot Table
1.	Make sure that data is not in the column headers (ex: January – it should be month)
2.	Ensure there are not blank columns/rows. You can have some blank cells, but it’s not ideal.


### Questions to ask when setting up a pivot table:
1.	What am I measuring
2.	How do I want to see it?

# Pivot Table Tools
## Slicers
### Timeline Slicer
Insert :arrow_right: Timeline Slicers
Can insert timeline slicers so that you have one pivot chart and can switch between time periods, so for the sales data it is a slicer for Orderdate

### Standard Slicer
Insert :arrow_right: Slicer
Let’s you slice by other values, for instance state, you see the sales by state. In the case of by state, the slicer has many states, so you have to scroll. Go into Format Slicer :arrow_right: Position and Layout :arrow_right: and select 3 columns. This works since the timeline slicer above is quite wide. This way it looks better visually. 

## Filters
### Top 10
Right click in chart, and select top 10.

# Pivot Reports

Can choose Reports with Subtotals, without Subtotals, Outline Mode

## Customizing Pivot Tables
### Change Column Name

Click on the column name in the table and simply type in a new name. 

## Group By
### Multiple Values
In the case of a chart where there are many options, such as for quantity ordered, if you want to see the sales for those categories, select the pivot table and right click Group By  in this case I picked to start at 6 and go to 97 (all data points) and group by 10. 
### Dates
I also used group by for a large variety of dates, I grouped by month. 
