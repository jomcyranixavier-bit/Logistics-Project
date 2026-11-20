1. Check Missing Values

Select each column → Home → Find & Select → Go To Special → Blanks
=COUNTBLANK(G:G)

Check Duplicate Records
Select the table → Data → Remove Duplicates

added new Column Vehicle Type
=XLOOKUP(Table1[@[Vehicle_ID]],Table2[Vehicle_ID],Table2[Vehicle_Type])

Add a pivot table Vehicle type and find Avg Fuel


added new Column Avg Fuel from pivot table
=XLOOKUP([@[Vehicle_Type]],Table8[Vehicle type],Table8[Avg Fuel])

For finding fuel efficiency first find the 
On-Time Trips = CALCULATE(COUNTROWS('Trip Data new'),'Trip Data new'[Delivery_Status]="On-Time")
and Total Trips = COUNTROWS(Trip_Data)

For finding the Cost per km =
DIVIDE(
    [Fuel Cost] + SUM(Vehicle[Maintenance_Cost]),
    SUM(Trip_Data[Distance_km])
fuel price default 95

Fuel Cost =
SUM(Trip_Data[Fuel_Consumed_L]) * 95

Vsualization
created a new column
Route = 'Trip Data new'[Origin]&"-"&'Trip Data new'[Destination]



