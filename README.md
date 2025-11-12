

**COFFEE SHOP SALES**

**OBJECTIVE 1: PREPARE THE DATA FOR ANALYSIS**

1)	*Familiarizing with the data. How many transactions were recorded, over what period of time? What products and product categories were sold? (Data Observation)*
   
•	Data from Jan 2023 to June 2023.

•	Timestamp from 6 am to 8 pm.

•	Transaction quantity ranges from 1 to 8.

•	There are 3 different locations with store ids:
Lower Manhattan (store id: 5),
Hell’s Kitchen (store id: 8),
Astoria (store id: 3).

•	There are 87 things on the menu with the price ranging from 80 cents to $45.

•	The 80 cent product is a flavor shot and $45 product is a premium coffee beans.

•	The items are categorized into bakery goods, tea, coffee, chocolates, branded items, etc.

2)	*Add a new column to calculate revenue (price* quantity).*
   
Make a revenue column, 
Put =transaction qty* price,
Ie. =D2*H2

(Double click to put the value all across the column and change the number format to accounting with decimals & dollar sign).

3)	*Add new columns to calculate the month and the Day of the week based on the transaction date (Display them as text ie. Sun, Jan, Feb instead of numerical values)*
   
Make four different column.

For the Month column, use =MONTH(B2) formula to get the numerical value from the transaction date.

For the month name column,  use =TEXT(B2,”mmm”) formula to change the numerical values Into text format.

For the weekday column, use =WEEKDAY(B2,2) formula to get the numerical values from transaction date.

For the weekday name column, use =TEXT(B2,”ddd”) formula to change the numerical values into text format.

4)	*Add a new column to Extract Hour from the transaction time.*
   
Make a column name ‘Hour’, use =HOUR(C2) formula to extract the hour from the transaction time.



**Objective 2: Explore data with Pivot Table**


1)	*Insert a Pivot Table on a new tab to show revenue by month*
   
Insert the Table into the PivotTable:
Insert > Pivot Table> New WorkSheet > OK

Put revenue Column into values section & put month name into Rows.
Format the values of the aggregate values

2)	*Add two more Pivot Tables (on the same sheet) to show the number of transactions by day of week and by the hour of day.*
   
Add the transaction id column (Change the value field settings> Count ) & Add weekday Name 

Same for the Hour of the Day

3)	*Add a Pivot Table ( on the same sheet) to show the number of transactions by product category, sorted descending by transactions.*
   
Values : Count of transaction_id

Rows: product category

Go to Row Labels Drop Down > More Sort Options > Descending (Z to A) by: Count of transaction_id


4)	*Add a Pivot Table to show the number of transactions and revenue by product type, sorted descending and filtered to the top 15 (by transaction)*
   
Values: count of Transaction_id and 
             Sum of Revenue
             
Row: Product type

Row Labels Drop Down > More sort options> descending (Z to A) by : transaction_id

Row Labels Drop down> Value Filters> Top 10> Select 15> by: Transaction_id



**Objective 3: Build a Dynamic Dashboard**

1)	*Add a PivotChart to show revenue by month as a linechart, transactions by the day of the week and hour of the day as column charts, and transaction by product category as a bar chart.*
   
Click on the PivotTable > PivotTable Analyze > PivotChart> Line > OK

2)	*Assemble the charts into the rough dashboard layout and include space for PivotTable showing Top 15 Product Type*
    
Change the layout and flow by changing the position of charts and PivotTables

3)	*Add a slicer for the store location , and connect it to all of the PivotTables on the sheet*
   
Adding a slicer: Click on the PivotTable > PivotTable Analyze > Insert Slicer > Store location > OK

To connect to all PivotTables: Slicer > Report Connections > Select the Names of the PivotTables > OK

4)	*Adjust the formatting, alignment and polish to finalize the dashboard.*
   
Hide the PivotTables for cleaner look

To hide gridlines and formula bar: View > Show Ribbon > Select Gridlines > Select formula bar

Changing Slicer Setting: Select Slicer > Right Click >  Slicer Setting > Change the Display name to “Change Location”.

Changing and styling the PivotCharts: Select PivotChart > PivotChart Analyze > Field Buttons > Hide All (To hide field buttons)

Remove the gridlines and legend

Format the Data Series ( By clicking on Trend Line)

For Pivotchart: Change Row Labels > “Top 15 Products”










