# Ford GoBike System Data
## by H.YUAN


## Dataset
This dataset contains various information regarding 181,8897 trips from Dec. 2017 to Nov. 2018 about the Ford GoBike system in the greater San Francisco Bay area, including trip duration, start/end time, station GPS location, user birth year, gender, subscription status. The original data can be found [here](https://www.fordgobike.com/system-data). Due to the limitation of submission, only the raw dataset files are included, to ensure the functionality of codes, please first run the codes in 'exploratory_analysis.ipynb' to generate the cleaned datasets, then 'explanatory_analysis_slide_deck.ipynb' for polished visualization and slides.


## Summary of Findings

In this project, I want to know about user demand for this bike sharing system, so I explored the dataset by looking for patterns in: user behavior and station traffics. The key to interpret the data is to calculate trip counts regarding user demographics, time and stations.

There are 330 stations, 4087 bikes in use, covering San Francisco, Berkeley and San José. 21.36% of the trips are made by  female subscribers, 65.92% by male subscriber, only 11.4% by one-time customers. Morning/night commutes are obvious patterns as trip count only peaks at 8 and 17 o'clock during weekdays, at weekends increase at normal daytime. The demand is also quite seasonal, people tend to ride bikes more frequently in warm seasons (summer and autumn) than cold ones. I also notice that the mean trip duration is longer at weekends than workdays, the same tendency among one-time customers than subscribers, maybe there are tourists using the bike sharing system for sightseeing.

The geographical distribution of stations and total traffic volume shows a relative higher demand for bike sharing in San Francisco than the other two cities. Further more, with a slopegraph, I found out that the inflow (drop-offs) and outflow (pick-ups) doesn't balance out for most of the stations, this indicates manual rellocation of bikes is required in order to keep up with user demand. Then I took a look at the daily traffics of the busiest stations (San Francisco Caltrain Station 2 during weekday and The Embarcadero at Sansome St during weekend), where the total traffic volume and the gap between pick-ups and drop-offs are both the largest. For the first station, there are only small variations within weekdays with two peaks due to commute needs, however at weekend the demand is quite low with onlz a few pick-ups and drop-offs. For the second one, flow direction is opposite to the first one, but still with two peaks on weekdays, during weekend, the flow direction is similar but with just one peak for pick-up and drop-off each at different time points. For stations, the inflow and outflow are time-dependent, which is a sign of tidal traffic due to commutes or other possible activities.


## Key Insights for Presentation

For the presentation, I focus on the different patterns of user demand within different time frames. I start by checking the distributions of trip durations using histogram, then user demographics with different categorical variables, and plot heatmaps to show the percentages of trips taken by different user groups.

Then, to identify time-related patterns, I plot the total trip counts and duration in minutes within different timeframes: by month, day of week, and hour. As well as the mean trip counts of all stations together, by hour of day for both weekday and weekend.

Afterwards, I plot the geographical distribution to get an overall feeling of station traffics, and using slopegraph by Edward Tufte, to plot the traffic volume of the busiest stations along with the gap between inflow and outflow. To further identify the tidal traffic patterns, I divide the stations into two groups: the ranking of station popularity on weekday and on weekend, then plot the busiest station of each with mean hourly traffic through out the week. I've made some revisions for polishing purpose, in order to visualize the results in a better way.
