# Group 5 README
This is the ReadMe file for project 1 of Group 5. The group members include Ling Liu(lili1299@colorado.edu) , Ziying Zhang(zizh8550@colorado.edu) and Lan Sang(lasa9094@colorado.edu). 

## Information about our visualizations
* We created two main visualizations: 

	(1) A world map interactive with a bar chart and a doughnut chart. 

	(2) An interactive radar chart.

* The first visualization is a world map on the right and a bar chart and a doughnut chart on the left. 

    * The world map uses categorical data and quantitative data: categorical data are country names obtained by participants’ IP address and the country information participants provided in Question 10 of the survey; quantitative data is the number of participants from each country (counted by IP address and Question 10 answers respectively). We also used an [external data](https://github.com/jdamiani27/Data-Visualization-and-D3/blob/master/lesson4/world_countries.json) of geographical information, and changed the name of some countries to map the survey data. The map shows all the countries with information in the *world_countries.json* file, and colored the countries with the number of participants from IP address if there are participants from the corresponding country. When mouseovering a country, you will see the country become pink and a box popping out which shows the country name, the total number of participants from that country by IP address and the total number of participants from that country by self-identification. The consideration for this design is to highlight the difference between the country information obtained by IP address and participants’ self-identification, because physically being in one country does not necessarily mean belonging to that country. We think the self-identification is more reliable, though some participants chose not to answer Question 10.
   
    * The doughnut chart uses categorical data and quantitative data: categorical data are the technology level participants evaluated themselves as by answering Question 1 “I consider myself:”, and there are 4 tech level categories plus one category for those not answering this question; quantitative data are how many participants fall into each category. The color of the doughnut slices indicates the categorical information, and the size of the doughnut slices depends on the number of participants in each category. The starting visualization of the doughnut chart is the analysis of the whole country. When you mouseover countries in the map, the doughnut chart will visualize the information for the corresponding countries. We design the interaction between the map and the doughnut chart to facilitate people exploring conditions in different countries.

    * The visualization below the doughnut chart is a bar chart. It also uses categorical data and quantitative data: categorical data is the languages uses; quantitative data is the number of participants using each language. The color of the bar are different for each language, and the height of the bar corresponds to the number of participants using the corresponding language. When you mouseover each bar, the bar will be highlighted and the number of participants shows up on top of the corresponding bar. The bar chart also interacts with the map in the same way as the doughnut chart. We decided to visualize this information because we found that though the survey claims to represent the whole world, it was only available in 6 Indo-European languages (English, French, Germain, Italian, Portuguese(Brazil) and Spanish). This limitation in language will cause the bias in the survey result: It limits the participation from countries where these languages are not used. The width of the bar is not fixed, and when fewer languages are used in a country, the bar width becomes larger. We design it this way to make it salient and draw people’s attention to the language bias. 

* The second visualization is a radar chart. It explores the data from Column Y to Column AH. These columns reflect how participants arrange the importance of different items when they decide to buy a new tech product, and the rank is a kind of quantitative data. When you choose one country from the dropdown list of all countries, you will see two radar charts: the left one shows the average data of each factor of the current country (yellow), with a comparison of the whole world average data (red).  The right one shows different languages users' situation in this country, the six different colors represent six different languages used by participants. This visualization clearly shows the different levels of importance for each item (Price, Security, Privacy, etc) between each country and languages. We could know what is the most important aspect people will consider when they buy a new tech product in a specific country or with a specific language background.

## Design Process

* First, we analyzed the data and decided what and how to visualize it. We found that for the 10 survey questions, Questions 2 and 9 are multiple choices, Question 8 is ranking, and other questions are single choice questions. Since there is country information and there are a lot of countries in the data, we decide to use visualize the countries with map. We also found that the survey is only available in 6 Indo-European languages, which we think will cause bias in the sample, so we decided to highlight this bias in the data in all our visualizations. We want to visualize a single choice question, because this is the main question type of the survey. Considering that doughnut charts presents percentage information well which are the information we get if we aggregate participants’ answers for a single question, we decided to make a doughnut chart for Question 1. We think the ranking question is interesting and special, and radar chart can give a good comparison of different ranking. Therefore, we decided to make our second visualization radar charts for Question 8.

* The second step is to refine our systems. We did three separate visualizations at first. However, we then found if we combine doughnut chart with the world map, our visualization will be more interactive--once mouseover the map, we could see languages used and user levels at the same time, which is more convenient for people to explore the question by country. So we connected the doughnut chart with the world map visualization and made them interactive. We also decided to add a bar chart to interact with the map in order to convey the theme of our visualization: language bias in the survey. For the radar chart, we first visualized the information of a country compared to the whole world in one radar chart, then added the drop down list for people to get visualization of different countries, and we added a second radar chart of data analysis by language, because we think that the preference is closely related to culture and language is a core part of culture.

## Team Roles

* Ling Liu: Designed and implemented the map and bar chart visualization; Merged doughnut chart to world map.

* Lan Sang: Designed doughnut chart visualization; implemented doughnut chart visualization; wrote ReadMe file

* Ziying Zhang: Designed radar chart visualization; implemented radar chart visualization


## How to run our project
		
* Our project can easily be run in the browser without any additional scripts. 

   * $ git clone https://github.com/INFO-4602-5602/project-1-mozilla-5602-proj1-liusangzhang.git
   
   * $ cd project-1-mozilla-5602-proj1-liusangzhang/
   
   * $ python -m http.server
   
   * Copy the data file *20171013111831-SurveyExport.csv* to the folder *project-1-mozilla-5602-proj1-liusangzhang/*.
   
   * Open a browser, type in *localhost:8000* as address.
   
   * Click on *mapChartsLinked.html* to see the first visualization.
   
   * Click on *RadarChart.html* to see the second visualization.
         
	  * Note that we modified the column names of CSV for the radar chart visualization to delete the space and those garbled characters in the Y to AH column title. We keep 10000 rows to match the GitHub file size limitation and the new csv called 10000data.csv. When you open the RadarChart.html, the data is from this csv. If you want to try the original data, please delete all space and keep the words before colon from Y to AH columns name, and change the csv name in RadarChart.html.
	  
## References

Sources that we referred to for this project are cited in the script at relevant position, noted with the format *Source: website-address*
