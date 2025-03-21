# Analysis to Boost Customer Acquisition and Optimize Operations
## Project Background
Cyclistic, a bike-sharing company, specializes in renting 3 different bike types (electric, classic and docked) at over 800 stations, providing service for casual riders and annual members. I'm partnering with the Head of Operations to drive customer and revenue growth, optimize targeted marketing, maximize product performance and improve operational efficiency.

## Executive Summary
Cyclistic's sales analysis of 5 million trips in 2021 reveals an annual revenue of approximately $18 million, with annual subscribed members contributing 58% of total rides. However, casual rides account for 68% of revenue ($12.5 million), highlighting an urgent need to address strategies aimed at converting casual riders into long-term annual members. Cyclistic can benefit from targeted marketing campaigns, optimizing product maintenance, understanding customer behaviours during peak seasons and optimizing operations. These efforts will be key to driving membership conversions in the following calendar year.

Check out the questions used to guide the analysis for each department [HERE](https://github.com/Lekan-E/Analysis-for-a-Bike-Sharing-Company-to-Boost-Member-Conversion/blob/e381591eb6a9bccadd88b90b261f34e9027c598f/Guiding%20Questions.md)

Insights and recommendations are provided on the following key areas and departments:

* **Sales Trends Analysis**: Evalutation of sales patterns, both members and casual riders, focusing on Revenue, Ride Volume and Revenue per Ride.
* **Product Level Performance**: An analysis of Cyclistic's various bike types, understanding user's perference and their impact on the number of rides, trip duration and the revenue generated.
* **Optimize Staffing and Maintenance**: An assessment to improve operations efficiency by adjusting staffing and maintenace schedules to align with peak user demands.
* **Seasonal and Holiday Marketing Campaigns**: A seasonal analysis to offer discounts and loyalty incentives to boost ridership and membership conversion by capitalizing on timed periods.
* **Targeted Marketing and Customer Engagement**: An analysis for the marketing team, that targets campaigns at key time of the day and high-traffic regions designed to boost conversion.


The Python Jupyter notebook utilized to clean, prepare and extract data can be found [here](https://github.com/Lekan-E/Analysis-for-a-Bike-Sharing-Company-to-Boost-Member-Conversion/blob/39c0d6460c8e61f9506c2e7b95d4392f5fa97831/Data%20Cleaning%20and%20Preparation.ipynb).

The Python Jupyter notebook to analyze the data using self-guided questions can be found [here](https://github.com/Lekan-E/Analysis-for-a-Bike-Sharing-Company-to-Boost-Member-Conversion/blob/39c0d6460c8e61f9506c2e7b95d4392f5fa97831/Analyzing%20Bike-Sharing%20Data.ipynb).

An interactive monthly Tableau dashboard can be found [here](https://public.tableau.com/app/profile/lekanelegbede/viz/HRDailyRidesDashboard/RideDashboard).

Daily ride trackers can be found [here](https://public.tableau.com/views/HRDailyRidesDashboard/TripDetails?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

## Data Structure & Final Data
The data structure as seen below consists of a single table with a total row count of 5,300,458 rides.
To gain deeper insights, we need to collect/extract the following data:
* **Holiday Dates** - Via webscraping we extracted the dates and events for the whole year
    - Source: https://www.timeanddate.com/weather/usa/chicago/historic?month=1&year=2021
* **Weather**: Collect hourly data for each day with over 8,785 records.
    - Source: (PAID) https://www.visualcrossing.com/weather/weather-data-services/Chicago,United%20States/metric/2020-12-01/2021-11-30
* **Pricing Schema**: We used a similar pricing as BIKE SHARE TORONTO to generate our revenue.

![Alt Text](https://github.com/Lekan-E/Customer-and-Product-Analysis-using-ML/blob/9719f429419f7dddcc29019b758d4dd613a80558/Images/Misc/drawSQL-image-export-2024-09-27.png)

Prior to beginning the analysis, a variety of data cleaning checks were conducted using statistical techniques for data accuracy and using the pricing schema from BIKE SHARE TORONTO to calculate trips revenue. The Python notebooks to inspect and perform quality checks can be found here.


## Insights Deep-Dive
### Overview of Findings

In analyzing last year's data, several key insights emerged. 
- Revenue fluctuates significantly, with July and August being the peak months, generating over $2.8M each, while the winter months saw much lower revenues reaching a low of $130k. 
- Casual riders produced higher revenue per trip ($5.89) compared to members ($2.06), with the highest revenue coming from electric bikes. 
- Operational data showed the busiest periods were afternoons. 
- Member riders use stations such as Rockwell St & 57th St frequently, while casual riders prefer popular tourist locations. 
- 46 stations of the 520 were underutilized, suggesting a need for relocation or rebalancing. 

The following sections will explore additional contributing factors and highlight key opportunities that will inform future budgeting, targeted promotions, and operational improvements to enhance service and profitability.


Below is the yearly overview page from the Tableau dashboard and more examples are included throughout the report. The entire interactive dashboard can be viewed [here](https://public.tableau.com/app/profile/lekanelegbede/viz/HRDailyRidesDashboard/RideDashboard)

![alt text](https://github.com/Lekan-E/Customer-and-Product-Analysis-using-ML/blob/12231dcfcd7f969f99256c7bf1d1af14b5755cd9/Images/Misc/Sales%20Trends.png)

### Sales Trends
- The company's peak revenue occurred during July and August, each generating over $2.8M. In contrast, February saw the lowest revenue at $130k, highlighting the seasonality of demand. The data shows the importance of **strategic pricing and promotions to counter revenue dips in colder months.**
- Casual riders drove ride volume in the summer months, contributing to higher revenue. **Winter months saw a sharp decline in rides for both casual and member riders**, suggesting the need for targeted efforts during the off-season to maintain consistent usage.
- The casual riders generated significantly higher revenue per trip ($5.89) compared to members ($2.06). This discrepancy suggests a need to explore pricing strategies and promotions that could encourage casual riders to convert to memberships.

![alt text](https://github.com/Lekan-E/Customer-and-Product-Analysis-using-ML/blob/460b92cf5fc9b2e6fdeda62d41bcf329710c012a/Images/Misc/correlation.png)

### Product Level Performance
- The classic bikes had the highest number of rides overall, but **electric bikes were favored by casual riders, especially during weekends and holidays**, accounting for longer trips and higher spend per ride. Docked bikes accounted to less than 5% of the total trips despite having the longest average duration.
- **50% of the company's revenue were from classic bikes** bringing in $9.1M total, followed by electric bikes at $7.36 million. Docked bikes accounted for $2.15 million. These findings emphasize the need to **focus on classic and electric bike offerings, potentially expanding their availability to enhance overall revenue**.
- Electric bikes were a key driver of higher revenue per ride, making them a profitable option to expand, especially for casual riders during peak demand periods.

![alt](https://github.com/Lekan-E/Customer-and-Product-Analysis-using-ML/blob/460b92cf5fc9b2e6fdeda62d41bcf329710c012a/Images/Misc/bikes.png)

### Optimizing Staffing and Maintenance
- Staffing and maintenance should be ramped up during the high-demand periods such as the summer months and the weekends, when revenue exceeded $3.9M. These periods requires more frequent bike checks and quicker turnarounds to meet increased rider activity. **Staff shifts should align with these time slots** to handle higher rider volumes and perform routine bike maintenance efficiently.
- Meanwhile **during low-revenue months like February, reduce staffing and maintenance frequencies** to match the drop in demand, conserving resources while ensuring operations run smoothly during slower periods.
- The company has **46 underutilized stations** from 838 stations, with the total number ranging from 3 to 152 rides. Where the top 10 underutilized stations have fewer than 50 rides each, indicating **potential opportunities for resource reallocation or station relocation.**
- Since electric bikes generate the highest revenue, prioritize their maintenance to minimize downtime, ensuring their availability for high-revenue casual riders, especially during weekends and holidays.

![alt](https://github.com/Lekan-E/Customer-and-Product-Analysis-using-ML/blob/64d6d3a82eaf88c86dbd6b89976664e5c2ade799/Images/Misc/Rides%20by%20Region.png)

### Targeted Marketing and Customer Engagement
- Our analysis shows peak usage in the afternoons, particularly during weekends and holidays. Targeting marketing campaigns during these high-traffic times can maximize visibility and boost membership retention and conversion amongst casual riders.
- We identify that **high-value casual riders are those would most likely convert to members**. These are rides over 22 minutes long and $7.42 per trip. In our analysis we determine the following factors influence the length of those trips:
    - Warmer temperatures [20-30 degree celcius]
    - Partially cloudy days
    - Summer season [June, July, August]
    - Holidays
    - Electric bikes
    - Weekends [Saturday and Sunday]

- Streeter Dr & Grand Ave was the highest revenue generating over $420k. By **focusing campaigns at the top 10 high-traffic areas each bringing in over $120k in revenue**, we can leverage existing customer interest and drive conversions among casual users.
- Data indicates that favorable **weather conditions—such as warm and clear days—correlate with longer rides and increased revenue**. Tailoring marketing efforts to promote rides during these optimal weather conditions can boost customer participation and drive up conversions.

![alt](https://github.com/Lekan-E/Customer-and-Product-Analysis-using-ML/blob/64d6d3a82eaf88c86dbd6b89976664e5c2ade799/Images/Misc/output.png)

# Recommendations:
Based on the uncovered insights, the following recommendations for each department have been provided:

_Marketing_ 
- To enhance ridership and conversion, we recommend focusing on late afternoon promotions in July and September, targeting high-traffic stations for membership campaigns, launching winter discounts, promoting electric bikes for casual riders, and **leveraging holidays deals with exclusive offers and event-based promotions**. 
- Send membership promotional emails after high value casual rider trips, these are trips over 32 minutes.

_Operations_ 
- To optimize operations, we recommend ***adjusting staffing and maintenance schedules to peak demand**, reassessing underutilized stations for better resource allocation, proactively managing fleet availability for weather changes, and **prioritizing maintenance for high-demand bikes** to enhance overall efficiency.

_Customer Insights_ 
- To enhance customer engagement and drive conversions, we recommend **leveraging favorable weather and weekends for special offers**
- Optimizing routes based on rider preferences, and 
- **Implementing flexible pricing strategies** to encourage casual users to transition to memberships.

_Finance_
- To maximize revenue, we recommend **investing in high-performing stations to enhance services**
- Prioritizing resources towards classic and electric bikes, which have demonstrated significant profitability.
