# An Analysis of Kickstarter Campaigns

## Overview of Project

The project uses Excel to organize, sort and analyze several thousand crowdfunding projects to uncover any hidden trends and determine if there are specific factors that make a campaign successful.

### Purpose

This particular analysis aims to understand and visualize the impact that launch dates and funding goals have on the outcome of different campaigns in the Theatre/plays category.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
To visualize what role a campaign's Launch Date plays in its outcome:
1. We first made sure the data was in a readable format and converted Unix Timestamps to Date format using the following equation: 

![date](https://user-images.githubusercontent.com/79415699/108647945-e49f8a80-7487-11eb-8ff4-e82e4f00e7be.JPG)

2. Used Year() function on the converted Launch Date column to extract the year. 
3. Created a pivot table based on "Parent Category" and "Years", then filter the category to "theatre".

 ![pivot](https://user-images.githubusercontent.com/79415699/108649368-2978f080-748b-11eb-8bd6-cf37283d8baa.JPG)
 
4. Created a line chart from the pivot table to visualize the relationship between outcomes and launch month. 

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/79415699/108649354-23830f80-748b-11eb-850d-cb6b5d05203d.png)



### Analysis of Outcomes Based on Goals
To analyze the relationship between outcomes and goals:
1. We needed to sort through the data and look at the % of successful, failed and canceled plays based on goal ranges, the table had the following layout:

![table](https://user-images.githubusercontent.com/79415699/108647933-de111300-7487-11eb-8795-1b11a6d0d2e9.JPG)

2. Used COUNTIFS() function to filter the data based on the specified goal ranges, subcategory ('plays'), and the outcome ('successful','failed','canceled') in columns B,C and D respectively. 

![countifs()](https://user-images.githubusercontent.com/79415699/108647954-e9fcd500-7487-11eb-88ef-7a67e5ddf090.JPG)

3. Created Line chart to visualize Outcome vs. Goals relationship
![Outcomes_vs_Goals](https://user-images.githubusercontent.com/79415699/108649352-23830f80-748b-11eb-9eb6-13cb4ca5d10c.png)

### Challenges and Difficulties Encountered
* Initial clean-up of data and converting it into a readable format (Unix Timestamp).


## Results

Conclusions about the Outcomes based on Launch Date:
* The number of successful campaigns is the highest from April to August compared to the rest of the dataset, so a launch date in those months is recommended. 
* Ratio of failed campaigns to successful ones is low from April to August compared to the ratio of failed/successful in other months. 
* There is no information on number of canceled plays in October. 

Conclusion about the Outcomes based on Goals:
* Looking at the line chart, it is visible that the higher the goals, the more likely they campaigns are to fail. 
* Given that there are no canceled plays, the highest  % of failed campaigns directly reflects the lowest % of successful ones in a given month. 
* There's a 50 % chance the campaigns fail at points of intersection
* Campaigns with goals <=$1000 are more likely to succeed, and are more likely to fail if their goals exceed $45000

Limitations of this dataset
* Looking at duration of the campaign might be as relevant as looking at the launch date. 
* What could also be useful is studying any correlation between launch date and goal. 

Other possible tables and/or graphs that we could create:
* We could also take the analysis a step further and look into the statistical distribution of the data, identify, explain and eliminate any outliers if necessary to have a cleaner set of data by looking at the quartile ranges and creating a Box and Whisker plot.
