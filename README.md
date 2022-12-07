# bikesharing
# Des Moines - Bike Sharing Project
## Overview of Project
Now that we've gotten a good idea of how to create our story, there is still some more work to be done to convince investors that a bike-sharing program in Des Moines is a solid business proposal. To solidify the proposal, one of the key stakeholders would like to see a bike trip analysis.

For this analysis, you’ll use Pandas to change the "tripduration" column from an integer to a datetime datatype. Then, using the converted datatype, you’ll create a set of visualizations to:

  Show the length of time that bikes are checked out for all riders and genders
  Show the number of bike trips for all riders and genders for each hour of each day of the week
  Show the number of bike trips for each type of user and gender for each day of the week.
  Finally, you’ll add these new visualizations to the two you created in this module for your final presentation and analysis to pitch to investors.

1. ***Deliverable 1***: Change Trip Duration to a Datetime Format
2. ***Deliverable 2***: Create Visualizations for the Trip Analysis
3. ***Deliverable 3***: Create a Story and Report for the Final Presentation

## Resources and Before Start Notes:

* Data Source: `NYC_Citibike_Challenge.ipynb` and `201908-citibike-tripdata.csv`
* Data Tools: Jupyter Notebook, CSV, Tableau and IO (Web Server)
* Software: Jupyter Notebook and Visual Studio Code 1.50.0

For more information, visit [`Tableau website`](https://public.tableau.com/en-us/s/). 




# Deliverable 1:  
## Change Trip Duration to a Datetime Format
### Deliverable Requirements:
Using Python and Pandas functions, you’ll convert the "tripduration" column from an integer to a datetime datatype to get the time in hours, minutes, and seconds (00:00:00). After you convert the "tripduration" column to a datetime dataytpe, you’ll export the DataFrame as a CSV file to use for the trip analysis in Deliverable 2.

Your final results should look similar to the following image:

<img width="726" alt="Screen Shot 2022-12-07 at 1 14 30 AM" src="https://user-images.githubusercontent.com/104086409/206102657-70c4cab9-4e2a-4253-b5ba-803ff1d94450.png">



1. The data in the "tripduration" column is converted to a datetime datatype and has the correct time format.
2. The DataFrame is exported as a new file without the index column.

 
### Results with detail analysis:

1. **The data in the "tripduration" column is converted to a datetime datatype and has the correct time format.**


> Image with `Jupyter Notebook` & `Tableau` Code below.

**Code and Image**


````py
# CHALLENGE 14
### MODULE 14 - Des Moines - Bike Sharing Project
#### by: Morifing Koné

import pandas as pd

# 1. Create a DataFrame for the 201908-citibike-tripdata data. 
citibike_data = "201908-citibike-tripdata.csv"
citibike_df = pd.read_csv(citibike_data)

# 2. Check the datatypes of your columns. 
citibike_df.info()

# 3. Convert the 'tripduration' column to datetime datatype.
citibike_df['tripdur_orig'] = citibike_df['tripduration']
citibike_df['tripduration'] = pd.to_datetime(citibike_df['tripduration'], unit='m')
citibike_df.head()

# 4. Check the datatypes of your columns. 
citibike_df.info()
````

2. **The DataFrame is exported as a new file without the index column.**


> Image with `Jupyter Notebook` & `Tableau` Code below.

**Code and Image**


````py
# 5. Export the Dataframe as a new CSV file without the index.
citibike_df.to_csv('citibike_201908_updt.csv', index=False)

# by Morifing Koné
````
[NYC_CitiBike_Challenge - Jupyter Notebook.pdf](https://github.com/Morifingk/bikesharing/files/10173332/NYC_CitiBike_Challenge.-.Jupyter.Notebook.pdf)




# Deliverable 2:  
## Create Visualizations for the Trip Analysis
### Deliverable Requirements:
Using Tableau, create visualizations that show:

  - How long bikes are checked out for all riders and genders.
  - How many trips are taken by the hour for each day of the week, for all riders and genders.
  - A breakdown of what days of the week a user might be more likely to check out a bike, by type of user and gender.

### Create the Checkout Times for Users Viz
In this visualization, you’ll graph the length of time that bikes are checked out for all riders.

<img width="730" alt="Screen Shot 2022-12-07 at 1 22 58 AM" src="https://user-images.githubusercontent.com/104086409/206104191-cec7cf28-1b79-4568-8fa3-55fba60ebda6.png">


### Create the Checkout Times by Gender Viz
In this visualization, you’ll graph the length of time that bikes are checked out for each gender.

Your final results should look similar to the following image:

<img width="724" alt="Screen Shot 2022-12-07 at 1 24 12 AM" src="https://user-images.githubusercontent.com/104086409/206104401-0a92743d-5b1c-4526-ae41-7f6f5c984ab8.png">


### Create the Trips by Weekday for Each Hour Viz
In this visualization, you’ll graph the number of bike trips by weekday for each hour of the day as a heatmap.

Your final results should look similar to the following image:

<img width="302" alt="Screen Shot 2022-12-07 at 1 24 50 AM" src="https://user-images.githubusercontent.com/104086409/206104510-9267d7c0-3461-4af3-a107-fbdd06045ccf.png">


### Create the Trips by Gender (Weekday per Hour) Viz
In this visualization, you’ll graph the number of bike trips by gender for each hour of each day of the week as a heatmap.

<img width="685" alt="Screen Shot 2022-12-07 at 1 25 20 AM" src="https://user-images.githubusercontent.com/104086409/206104614-5d1a9190-390f-4a73-80a2-f2b5b45b9189.png">


### Create the User Trips by Gender by Weekday Viz
In this visualization, you’ll graph the number of bike trips by gender for each hour for each day of the week as a heatmap.


<img width="728" alt="Screen Shot 2022-12-07 at 1 25 42 AM" src="https://user-images.githubusercontent.com/104086409/206104651-6c53816c-b05d-42f1-b3d0-bc81fa6f042d.png">


### Deliverable 2 Requirements:
You will earn a perfect score for Deliverable 2 by completing all requirements below:

1. There is a line graph displaying the number of bikes checked out by duration for all users, and the graph can be filtered by the hour.
2. There is a line graph displaying the number of bikes that are checked out by duration for each gender by the hour, and the graph can be filtered by the hour and gender.
3. A heatmap is created showing the number of bike trips for each hour of each day of the week.
4. A heatmap is created showing the number of bike trips by gender for each hour of each day of the week, and the heatmap can be filtered by gender.
5. A heatmap is created showing the number of bike trips for each type of user and gender for each day of the week, and you can only filter by user and gender.

 
### Results with detail analysis:

1. **There is a line graph displaying the number of bikes checked out by duration for all users, and the graph can be filtered by the hour.**


> Image with `Jupyter Notebook` & `Tableau` Code below.

##### Des Moines - Bike Sharing Project Analysis Completed by Morifing Koné
