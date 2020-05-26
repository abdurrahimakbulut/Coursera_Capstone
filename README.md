# Coursera_Capstone
## **STARTING A JOB DURING COVID 19**
During Covid-19 outbreak all countries has taken some measures to slow down and eliminate this threat. Lockdown is considered to be effective and must measure. So governments, including Turkey which i'm currently living in, applied lockdown under some conditions. For example
in Turkey, bakeries are allowed to remain open and people can to go bakeries during the lockdown. But there is one condition: Bakery must be within the walking distance.

Why did i explained this? Because if you consider to start a new job, bakery might be very logical since it's always needed in Turkey and allowed to remain open even during lockdown.

So let's assume you've decided to open a bakery. Now here comes the most important question. Where should you open it?

#### **WHERE TO OPEN A BAKERY**
I believe these two criterias should be taken account while opening a bakery:
  * Number of bakeries in the neighborhood
  * Population
If there are too many bakeries in the neighborhood it's not logical to start a new bakery. Also if the number of residents is low, again it might not be logical. So we have to select an optimal location with enough population and not many bakeries. 

I'll focus on the Nilüfer district of Bursa, which is one of the biggest districts of this city, due to simplify the visualization process. Please note that it's possible to expand the area to whole city.

## **COLLECT & ANALYZE NEIGHBORHOOD DATA**
I'll be using population data which is provided by TUIK (Turkish Statistical Institute). This dataset includes all cities, districts and neighborhoods in Turkey along with their population. 
Dataset can be downloaded from here: https://biruni.tuik.gov.tr/medas/zkau/view/z_f0a/dwnmed-0/b5f/95.xlsx

Extracted the necessary information for this project which is neighborhood populations. Final excel sheet contains all the neighborhoods in Turkey. After reading it from the xlsx file to a dataframe the data looks like this:

![img1](https://user-images.githubusercontent.com/65724505/82919102-41fcbe80-9f7e-11ea-9173-7d64bb78860e.JPG)

Let's filter the neighborhoods down to the Nilüfer(District), BURSA(City) where we would like to start our bakery. Also let's translate the column names. (The district is selected manually due to simplify the visualization but it's possible to )

![img2](https://user-images.githubusercontent.com/65724505/82919724-14644500-9f7f-11ea-8286-e7f26a95f226.JPG)

Now we have names of all the neighborhoods in Nilüfer district. Next step is getting coordinates of the neighborhoods. For this, i am going to use Nominatim geocoder from GeoPy package.

![img3](https://user-images.githubusercontent.com/65724505/82921232-d2d49980-9f80-11ea-89d5-cc386f3b830a.JPG)

Let's merge the 2 dataframes to get a resulting dataframe which contains population, latitude, longitude of each neighborhood.

![img4](https://user-images.githubusercontent.com/65724505/82921691-57bfb300-9f81-11ea-8331-4fa5a764e89c.JPG)

Now, it's time to use Foursquare API to collect data about bakeries in each neighborhood.

![img5](https://user-images.githubusercontent.com/65724505/82923385-8b034180-9f83-11ea-973a-4e7a2ab91cfd.JPG)

So far, i have tried to demonstrate the data which will be used in this project. The images meant to illustrate the main properties of the data. The collection and preparation of the data will be explained in much more detail later in the notebook.
