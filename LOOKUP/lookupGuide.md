Lookup Formulas

| Function | Description |
| -------- | ----------- |
| CHOOSE | Returns a specific value from a list of values supplied as arguments. |
| IF | Returns one value if a condition you specify is TRUE and returns another value if the condition is FALSE. |
| LOOKUP | Returns a value from either a one-row or one-column range. Another form of the LOOKUP function works like VLOOKUP but is restricted to returning a value from the last column of a range. |
| OFFSET | Returns a reference to a range that is a specified number of rows and columns form a cell or range of cells. |

**VLOOKUP** 
Designed for lookup value that is to the left of what you want to search for. So in the example below, use the ID to find the name/pay/etc. As long as the value is you are looking for is to the left of what you are use as the lookup value, you don’t need the entire table. But the column where you have your range has to start with the lookup value or it won’t work. So left-most column must be the column with the lookup value. Vertical lookup. Searches for a value in the first column of a table and returns a value in the same row from a column that you specify in the table.
=VLOOKUP(K1,C:D, 2, FALSE): this works K1 references column C
=VLOOKUP(K1,A:D, 4, FALSE): this fails since the range (A:D) does not start with the lookup value col

Data Example
	B	C	D	E	F	G	H	I
2	ID	Employee Name	Address	Frequency	Salary	Tax Rate	Insurance	401K
3	154	Paige Jones	1 fake St	26	42,900	15%	100.00	8%
4	240	Elijah Ward	2 G St	26	64,600	16%	200.00	7%
Get each of these values after getting the employee id
VLOOKUP(lookup value, lookup range, column, match)  col = where to find val, match = t/f
Employee Name: VLOOKUP($L$3, $B$3:$I$4, 2, FALSE) false means exact match only
Pay (M7): VLOOKUP($L$3, $B$3:$I$4, 5, FALSE)/($L$3, $B$3:$I$4, 4, FALSE)  4 & 5 =cols (Freq & Salary)
Insurance (O8): VLOOKUP($L$3, $B$3:$I$4, 7, FALSE)
Retirement (O9): VLOOKUP($L$3, $B$3:$I$4, 8, FALSE)
Taxes (O7): =(M7-O8 –O9)* VLOOKUP($L$3, $B$3:$I$4, 6, FALSE)
Total (O11): =SUM(O7:O10)
Net Pay (O3): =M7-O11

VLOOKUP Example2

 
HLOOKUP
Horizontal lookup. Searches for a value in the top row of a table and retruns a value in the same column from a row you specify in the table. Use when data is structured by rows
Data Example
	B	C	D	E
2	City	Tempe	New York	Kathmandu
3	Temp	40	30	48
4				
5	Your City	New York		
6	Your Temp:			
7				
8	Index			
=HLOOKUP(C5, C2:E3, 2, FALSE)
Index and Match
Used for values that are on the right or in the middle of what you are searching. In this case matching value in middle column to get the two outer columns you use index and match.
Match: Returns the relative position of an item in a range that matches a specified value
Index: Returns a value (or the reference to a value) from within a table or range.
Data Example
	B	C	D	E	F	G
2	City	State	Store #			
3	Chandler	AZ	6493t			
4	Glendale	CO	4369		State:	NH
5	Manchester	NH	2608		City:	
6	Peoria	IL	3493		Store:	
7	Green Bay	WI	9340			
8	Toledo	OH	4304		LOOKUP City:	
9	SF	CA	3301		LOOKUP Store:	
City =INDEX(B3:D9, MATCH(G4, C3:C9, FALSE, 1) Matching G4, return 1st col (city)
Store=INDEX(B3:D9, MATCH(G4, C3:C9, FALSE, 3)  Match G4 return 3rd col (store)

Hiding Errors with Lookup Functions
IFERROR
If the first argument returns an error
=IFERROR(VLOOKUP(C3, $F$3:$G$11, 2, False), “”) rather than N/A for no match get a blank
Setting parameter to True (Not exact match)
Ex: if you have withholding amount and don’t have the exact total, VLOOPUP will look down the first column and stop when the next value is higher than the lookup value if you set the final parameter to true. But it may not be the closest match, they just look for the next highest value in the column over the threshold. So if the data is not sorted, this could be an issue. Setting it to true is much faster, so if the data is sorted it can save time.

