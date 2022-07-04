# NYC_Citi_BikeSharing
To explore and analyze the New York Citi Bike Program and create powerful dashboards and stories using Tableau.

## Overview of the Analysis
Tableau is a data analysis and visualization tool.It is so popular because it allows data visualization professionals to create assets that are visually appealing and easy for non-technical audience to understand.We can create clear,easy to grasp data stories.
Tableau provides the tools for creating powerful analytic dashboards,tell a clear story and can be easily shared with others.The components in tableau are Worksheets,Dashboards,Stories.<br>

## Purpose of the Analysis
The aim of this analysis is to explore and visualize the CitiBike,which is a privately owned public bicycle sharing system serving the New York city.
The Bike is the key tool which allows to explore the city and interact with various people who live there.An tourist who visited the New York wants to establish a similar bike sharing business in their home town Des Moines,Iowa.In order to establish the same program,we need to analyze the New York citibike program further to know more about the data.

## Resources Used
*DataSources*: [NYC_CitiBike_Data](https://ride.citibikenyc.com/system-data) <br>
*Software used*:  Jupyter Notebook,Tableau.<br>
*Language*: Python.<br>
*Dashboard*:[Link to DashBoard](https://public.tableau.com/app/profile/nasreen.fathima.habeeb.rahman/viz/NYC_Citi_Bike_Program/NYCCitiBikeProgram)

## Deliverable 1: Change Trip Duration to a Datetime Format 
The New York Bike Sharing Data has the following columns,Trip Duration,Start Time and Date,Stop Time and Date,Start Station Name,End Station Name,Station ID,Station Lat/Long,Bike ID,User Type (Customer = 24-hour pass or 3-day pass user; Subscriber = Annual Member),Gender (Zero=unknown; 1=male; 2=female)
Year of Birth.Using Python and Pandas functions, we will convert the "tripduration" column from an integer to a datetime datatype to get the time in hours, minutes, and seconds (00:00:00). After we convert the "tripduration" column to a datetime dataytpe, we will export the DataFrame as a CSV file to use for the trip analysis.When we check the datatypes of each column in the DataFrame.<br>
<img src = "https://github.com/fathi129/NYC_Citi_BikeSharing/blob/master/Screenshot_Tableau/initial%20check%20data%20type.png" width = 500><br> 
            
We convert the "tripduration" column to a datetime datatype, by passing the DataFrame column and the units inside the to_datetime() function.We need to specify the units for conversion.The default is "ns," which stands for nanoseconds.Here we have specified unit as 's'.After converting when we check the datatypes of the DataFrame.<br>
<img src = "https://github.com/fathi129/NYC_Citi_BikeSharing/blob/master/Screenshot_Tableau/datatypecheck.png" width = 700><br> 
The converted values in the "tripduration" column looks like the following image:<br>
<img src = "https://github.com/fathi129/NYC_Citi_BikeSharing/blob/master/Screenshot_Tableau/trip%20duration%20converted.png" width = 800><br> 

## Deliverable 2: Create Visualizations for the Trip Analysis 
Using Tableau, we create visualizations that show:
How long bikes are checked out for all riders and genders.
How many trips are taken by the hour for each day of the week, for all riders and genders.
A breakdown of what days of the week a user might be more likely to check out a bike, by type of user and gender.<br>

### 1. Create the Checkout Times for Users Viz
In this visualization, we will graph the length of time that bikes are checked out for all riders.Add the number of records or the generated field that counts the number of records in the CSV file to the Rows.Add the "tripduration" column you converted to the Columns, and filter the "More" option by "Hour".Add the "tripduration" column again to the Columns, and filter the "More" option by "Minute", and then change the values from "discrete" to "continuous".Add the "tripduration" column that shows the "Hour" to the Filters field, and select "Show Filter".<br>
The graph should look similar to the following image:<br>
<img src = "https://github.com/fathi129/NYC_Citi_BikeSharing/blob/master/Screenshot_Tableau/Checkout_times_for%20users.png" width = 800><br>            
Most bikes were used for less than 1 hour, and most were used for 20 minutes or less. The male riders are more, but we can see the same pattern of checkout times regardless of gender.<br> 

### 2.Create the Checkout Times by Gender Viz
In this visualization, we will graph the length of time that bikes are checked out for each gender.
Add the number of records or the generated field that counts the number of records in the CSV file to the Rows.Add the "tripduration" column you converted to the Columns, and filter the "More" option by "Hour".Add the "tripduration" column again to the Columns, and filter the "More" option by "Minute", and then change the values from "discrete" to "continuous".Add the "tripduration" column that shows the "Hour" to the Filters field, and select "Show Filter".
Add the converted column for gender as a color to the Marks field, add it to the Filters field, and select "Show Filter".
The graph should look similar to the following image: 
<img src = "https://github.com/fathi129/NYC_Citi_BikeSharing/blob/master/Screenshot_Tableau/checkout%20time%20for%20gender.png" width = 800><br> 
Most bikes were used for less than 1 hour, and most were used for 20 minutes or less. The male riders are more, but we can see the same pattern of checkout times regardless of gender.
            
### 3. Create the Trips by Weekday for Each Hour Viz
In this visualization, we will graph the number of bike trips by weekday for each hour of the day as a heatmap.
Add the "Starttime" column to the Rows, and filter the "More" option by "Hour".Add the "Stoptime" column to the Columns, and filter the “More” option by "Weekday".Add the number of records or the generated field that counts the number of records in the CSV file to the Marks field as a color. Select "Automatic" for the type of graph to create the heatmap.Format the Y axis of the Starttime by Hour to show the 12-hour format.Format the X axis of Stoptime by Weekday as "Abbreviation".<br>
The graph should look similar to the following image:<br>
<img src = "https://github.com/fathi129/NYC_Citi_BikeSharing/blob/master/Screenshot_Tableau/del2_trip_weekday_hr.png" width = 700><br> 
We can see that morning, 7-9 am, the bicycle usage is more during the same in the evening from 4-7 pm during weekdays except for Wednesday. We can see full-day use during the weekends.<br>          

### 4.Create the Trips by Gender (Weekday per Hour) Viz
In this visualization, we will graph the number of bike trips by gender for each hour of each day of the week as a heatmap.
Add the "Starttime" column to the Rows, and filter the "More" option by "Hour".Add the "Stoptime" column to the Columns, and filter the “More” option by "Weekday".Add the number of records or the generated field that counts the number of records in the CSV file to the Marks field as a color. Select "Automatic" for the type of graph to create the heatmap.Add the converted column for "Gender" to the Columns and to the Filters field, and select "Show Filter".Format the Y axis of the Starttime by Hour to show the 12-hour format.Format the X axis of Stoptime by Weekday as "Abbreviation".<br>
The graph should look similar to the following image:<br>
<img src = "https://github.com/fathi129/NYC_Citi_BikeSharing/blob/master/Screenshot_Tableau/del2_trip_by_gender.png" width = 800><br>
The usage of bikes is more in males, but we can see the same pattern of hours regardless of gender.<br>
            
### 5.Create the User Trips by Gender by Weekday Viz
In this visualization, we will create a heatmap that shows the number of bike trips broken down by gender for each day of the week by each Usertype.
Add the converted column for "Gender" to the Columns and to the Filters field, and select "Show Filter".Add the "Usertype" to the Rows and to the Filters field, and select "Show Filter".Add the "Starttime" column to the Rows, and filter the "More" option by "Weekday".Add the number of records or the generated field that counts the number of records in the CSV file to the Marks field as a color. Select "Automatic" for the type of graph to create the heatmap.<br>
The graph should look similar to the following image:<br>

<img src = "https://github.com/fathi129/NYC_Citi_BikeSharing/blob/master/Screenshot_Tableau/usertrips_gender.png" width = 800><br>  
We can see that the bike usage of Subscribers is higher compared to the customers during weekdays, with the male being more elevated. But during the weekends, both the users have similar use.<br>

### 6.Top Starting and Ending Locations
When we see closely the maps, the CitiBike usage in the starting and ending locations looks the same, with same patterns,smaller and dark-colored circles.

|   *** Top Starting Location ***    | ***Top Ending Locations ***   |
|  ----------------------------------|  -----------------------------| 
|  <img src = "https://github.com/fathi129/NYC_Citi_BikeSharing/blob/master/Screenshot_Tableau/starting_loc.png" width = 350><br >   | <img src = "https://github.com/fathi129/NYC_Citi_BikeSharing/blob/master/Screenshot_Tableau/endloc.png" width = 350><br>|<br>
                                                    
## 7.Gender,Bike Utilization and Bike Repairs
We can see that the bike usage of Subscribers is higher compared to the customers during weekdays, with the male being more elevated. But during the weekends, both the users have similar use.

<img src = "https://github.com/fathi129/NYC_Citi_BikeSharing/blob/master/Screenshot_Tableau/gender_bike_repair.png" width = 700><br>
             
 ## Summary
- By seeing all the visualizations, we can say that NYC's Citi Bike Program is a massive success for the city with an active population. We can expect the same from Des Moines which is an active city with large population.It has lots of tourist attractions so the CitiBike program would be a success if it is launched there.
- Generally we can see from the New york CitiBike data Visualizations,there are more number of riders in the morning 7-9am and in the evening 4-7pm.We can say most of the office or college people use this commute.We can even see that there are more number of riders for the whole day during weekends.The people spend biking time with family and kids during weekend.We can always say that biking is great way to reach places faster with out traffic.It is generally preferred by people of all ages and genders.<br>              
 ### Ride Count by Birth Year
 We can perform further visualizations on the given data to know more about riders age group,From this analysis we can see that the riders with the birth year 1969 are high in this graph.So we can say that riders in this group prefer bike commute.            
 <img src = "https://github.com/fathi129/NYC_Citi_BikeSharing/blob/master/Screenshot_Tableau/Ride%20count%20by%20birth%20year.png" width = 800><br>
 ### Starting Staions
 When we see the starting locations,we can see that Pershing Square North starting location has more number of riders when compared to other locations.we need to ensure that we have enough number of bikes in this location.<br>
 <img src = "https://github.com/fathi129/NYC_Citi_BikeSharing/blob/master/Screenshot_Tableau/Startingstation.png" width = 800><br>                         
 ### Customers Vs Subscribers
 We can compute the user group of customers and subscribers based on the pie chart.When we see the pie chart we can see that subscribers are high in number compared to the users.
 <img src = "https://github.com/fathi129/NYC_Citi_BikeSharing/blob/master/Screenshot_Tableau/CustvsSub.png" width = 700><br>             
             
                                                    
                                                    




