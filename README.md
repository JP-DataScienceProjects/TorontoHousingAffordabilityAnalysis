# Toronto House Price Affordability Analysis
### By:  John Pazzelli
**Nov. 2017**

This analysis was performed as part of an assignment for the [Applied Plotting, Charting and Data Representation in Python](https://www.coursera.org/learn/python-plotting) course as part of the [Applied Data Science in Python Specialization](https://www.coursera.org/specializations/data-science-python) on Coursera.  

The assignment required that we independently find **at least 2 datasets** on the web that are **related in at least one dimension** to answer a question of our choosing related to **economic activity or measures** for the **City of Toronto**.  

### Topic
I decided to perform an **analysis of Toronto housing affordability by neighbourhood** given the runaway prices of housing and condominiums in the city in recent years.

To answer this question, I decided to **compare the average household income by city region to the average house price in that region** to look for areas in the city where the residents are living above their means (i.e. the **average house price far exceeds the average household income**).  I used two datasets from the **City of Toronto** website (one containing **household income data by neighbourhood** and another using **average household income by city ward**)

### Challenges
- The **average home price data was listed per neighbourhood** but the **household income data was listed per city ward** and there was **no direct mapping** of city neighbourhood to ward number

- To overcome this, I obtained a [Map of Neighbourhoods](https://www.toronto.ca/city-government/data-research-maps/neighbourhoods-communities/neighbourhood-profiles/) and a [Map of Wards](https://www.toronto.ca/city-government/data-research-maps/neighbourhoods-communities/ward-profiles/) and [overlayed them in Photoshop](https://github.com/JP-DataScienceProjects/TorontoHousingAffordabilityAnalysis/blob/master/Screenshots/Overlay.png) to manually **add a Ward number column** to my **average home price data**:

**Neighbourhoods**  
![alt text](https://github.com/JP-DataScienceProjects/TorontoHousingAffordabilityAnalysis/blob/master/Screenshots/Neighbourhoods.png)

**Wards**  
![alt text](https://github.com/JP-DataScienceProjects/TorontoHousingAffordabilityAnalysis/blob/master/Screenshots/Wards.png)

**Overlay**  
![alt text](https://github.com/JP-DataScienceProjects/TorontoHousingAffordabilityAnalysis/blob/master/Screenshots/Overlay.png)

### Result
An **interactive plot** was created in **matplotlib** that showed the neighbourhoods in the city where the **average house prices were significantly more than the average household incomes**, indicated by the position and colour of each bubble on the chart (**higher = less affordable**).  The **size** of the bubbles **indicate the number of households** in that neighbourhood.  

**On user click, the neighbourhood name is displayed** next to the bubble as shown below.

![alt text](https://github.com/JP-DataScienceProjects/TorontoHousingAffordabilityAnalysis/blob/master/Screenshots/FinalPlot.png)

### Datasets
I used the following data sources (note that the latest available data was from 2011):

**City of Toronto**:
1. [Wellbeing - Housing data](http://opendata.toronto.ca/social.development/wellbeing/WB-Housing.xlsx) taken from [here](https://www.toronto.ca/city-government/data-research-maps/open-data/open-data-catalogue/#0ee5007f-7c8b-5107-7fa8-24de3ae06f22)

2. [National Household Survey Data - 2011](http://opendata.toronto.ca/it/com/Ward%20Profiles%20-%20NHS_2011.xlsx) taken from [here](https://www.toronto.ca/city-government/data-research-maps/open-data/open-data-catalogue/#0dcc4b06-b0e8-3db3-80d0-a10aed2a0312) 
