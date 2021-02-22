# An Analysis of Kickstarter Campaigns

## Overview of Project

The project uses Excel to organize, sort and analyze several thousand crowdfunding projects to uncover any hidden trends and determine if there are specific factors that make a campaign successful.

### Purpose

This particular analysis aims to understand and visualize the impact that launch dates and funding goals has on the outcome of different campaigns in the Theatre/plays category.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
To visualize what role a campaign's Launch Date plays in its outcome:
1. We first made sure the data was in a readable format and converted Unix Timestamps to Date format using the following equation: 

2. Used Year() fundtion on the converted Launch Date column to extract the year. 
3. Create a pivot table based on "parent Category" and "Years", then filter the category to "theatre".
5. Create a line chart from the pivot table to visualize the relationship between outcomes and launch month. 


### Analysis of Outcomes Based on Goals
To analyze the relationship between outcomes and goals:
1. We needed to sort through the data and look at the % of successful, failed and canceled plays based on goal ranges, the table had the following layout:

2. Used COUNTIFS() function to filter the data based on the specified goal ranges, subcategory ('plays'), and the outcome ('successful','failed','canceled') in columns B,C and D respectively. 


### Challenges and Difficulties Encountered

## Results

Conclusions you can draw about the Outcomes based on Launch Date:
* The number of successful campaigns is the highest from April to August compared to the rest of the dataset, so a launch date in those months is recommended. 
* Ratio of failed campaigns to successful ones is low from April to August compared to the ratio of failed/successful in other months. 
* There is no information on number of canceled plays in October. 

Conclusion about the Outcomes based on Goals:
* Looking at the line chart, it is visible that the higher the goals, the more likely they campaigns are to fail. 
* Given that there are no canceled plays, the highest  % of failed campaigns directly reflects the lowest % of successful ones in a given month. 
* There's a 50 % chance the campaigns fail at points of intersection
* Campaigns with goals <=$1000 are more likely to succeed, and are more likely to fail if their goals exceed $45000

- Limitations of this dataset
* Looking at duration of the campaign might be as relevant as looking at the launch date. 
* What could also be useful is studying any correlation between launch date and goal. 

Other possible tables and/or graphs that we could create:
* We could also take the analysis a step further and look into the statistical distribution of the data, identify, explain and eliminate any outliers if necessary to have a cleaner set of data by looking at the quartile ranges and creating a Box and Whisker plot.
