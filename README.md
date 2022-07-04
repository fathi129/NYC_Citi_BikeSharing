# NYC_Citi_BikeSharing

##Overview of the Analysis
##Purpose of the Analysis

## Resources Used
*DataSources*: https://redplanetscience.com, https://spaceimages-mars.com/, https://galaxyfacts-mars.com/, https://marshemispheres.com/ <br>
*Software used*: Visual Studio Code 1.56.0, Jupyter Notebook, Flask 1.1.2, Splinter 1.26.4, Web Drive Manager, Beautiful Soup, Pymongo, MongoDB 4.4.6, Mongo DB Compass, HTML, Bootstrap 3.3.7
*Language*: Python. <br>

## Deliverable 1: Change Trip Duration to a Datetime Format 
Using Python and Pandas functions, you’ll convert the "tripduration" column from an integer to a datetime datatype to get the time in hours, minutes, and seconds (00:00:00). After you convert the "tripduration" column to a datetime dataytpe, you’ll export the DataFrame as a CSV file to use for the trip analysis in Deliverable 2.

Follow the instructions below to complete Deliverable 1.

Download the NYC_CitiBike_Challenge_starter_code.ipynb file into your bikesharing folder, and rename it NYC_Citibike_Challenge.ipynb.
Use the instructions below to add code where indicated by the numbered-step comments in the starter code file. We have provided the dependencies you will need for this challenge.
In Step 1, create a DataFrame from the 201908-citibike-tripdata.csv file.
In Step 2, check the datatypes of each column in the DataFrame.
In Step 3, convert the "tripduration" column to a datetime datatype by passing the DataFrame column and the units inside the to_datetime() function.
When using your GoogleFu to find out how to convert an int64 to a datetime object, it may be more useful to use the following search: "convert seconds to minutes in pandas." Additionally, you can refer to the pandas.to_datetime() documentation (Links to an external site.). In the documentation, it states that in the to_datetime() function, you’ll have to specify the units for conversion. The default is "ns," which stands for nanoseconds.

In Step 4, check the datatypes of the DataFrame.
Confirm that the converted values in the "tripduration" column match the following image:
<img src = " width = 350><br> 

## Deliverable 2: Create Visualizations for the Trip Analysis 
Using Tableau, create visualizations that show:
How long bikes are checked out for all riders and genders.
How many trips are taken by the hour for each day of the week, for all riders and genders.
A breakdown of what days of the week a user might be more likely to check out a bike, by type of user and gender.<br>

## 1. Create the Checkout Times for Users Viz
In this visualization, you’ll graph the length of time that bikes are checked out for all riders.

Add the number of records or the generated field that counts the number of records in the CSV file to the Rows.
Add the "tripduration" column you converted to the Columns, and filter the "More" option by "Hour".
Add the "tripduration" column again to the Columns, and filter the "More" option by "Minute", and then change the values from "discrete" to "continuous".
Add the "tripduration" column that shows the "Hour" to the Filters field, and select "Show Filter".
Edit the X and Y axis labels by right-clicking on the axis label and selecting "Edit Axis".
Your graph should look similar to the following image:
<img src = " width = 350><br>                                                                                           
                                                                                          
## 2.Create the Checkout Times by Gender Viz
In this visualization, you’ll graph the length of time that bikes are checked out for each gender.

Repeat steps 1-4 of the "Checkout Times for Users" visualization.
Add the converted column for gender as a color to the Marks field, add it to the Filters field, and select "Show Filter".
Edit the X and Y axis labels by right-clicking on the axis label and selecting "Edit Axis".
Your graph should look similar to the following image: 
<img src = " width = 350><br> 
            
## 3. Create the Trips by Weekday for Each Hour Viz
In this visualization, you’ll graph the number of bike trips by weekday for each hour of the day as a heatmap.

Add the "Starttime" column to the Rows, and filter the "More" option by "Hour".
Add the "Stoptime" column to the Columns, and filter the “More” option by "Weekday".
Add the number of records or the generated field that counts the number of records in the CSV file to the Marks field as a color. Select "Automatic" for the type of graph to create the heatmap.
Format the Y axis of the Starttime by Hour to show the 12-hour format, as shown in the following image:

Optional: Format the X axis of Stoptime by Weekday as "Abbreviation".
Your graph should look similar to the following image:
<img src = " width = 350><br> 


            





##6.Top Starting and Ending Locations

|   *** Top Starting Location ***    | ***Top Ending Locations ***   |
|  ----------------------------------|  -----------------------------| 
|  <img src = "" width = 350><br >   | <img src = "" width = 350><br>|<br>




