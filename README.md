# Kickstarting with Excel

## Overview of Project

### Purpose

The purpose of this project is to analyse Kickstarter data in order to help our friend Ann set up her own Kickstarter campaign so that it is more likely to be successful. We will be analysing existing Kickstarter campaigns outcomes based on their start dates and goals. 

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

Based on the existing data we created a pivot table that allowed us to filter each of the categories: failed, successful, and canceled based on the month of the year the campaign was started. We filtered this even further to only include the subcategory of theather since this is the information that most closely resembles the campaign Ann is looking for information on.

Here are the results from when we analysed the outcome of the theater Kickstarter campaigns based on launch date:
![1](Resources/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals

In order to analyse the data based on goals we had to do some further excel manipulation. First we had to separate the goals into ranges that would allow us to look at segments of the data. The ranges we chose were less that $1000, $1000 - $4999, then $5000 segments until everything over $50000 was grouped together. At this point we were able to use the countifs() formula in excel to allow us to break down that data based on the outcome of the campaign and the subcategory plays, again because this information would be most useful to Ann. For example theformula that allowed us to get the counts of successful campaigns with a goal of $1000 - $4999 for the category of plays is:
>=COUNTIFS(Kickstarter!$D:$D, ">=1000", Kickstarter!$F:$F, "successful", Kickstarter!$R:$R, "plays", Kickstarter!$D:$D, "<=4999", Kickstarter!$F:$F, "successful", Kickstarter!$R:$R, "plays")

That format can be altered to count different data as need for all of our ranges. 

Here are the results from when we analysed the outcome of the kickstarter based on their goal:
![1](Resources/Outcomes_vs_Goals.png)

### Challenges and Difficulties Encountered

The main challenge I encountered while analysing this data is making sure that the data was pulling from the correct column in the Kickstarter worksheet and that I had included all of the filters required both in the pivot table and the further data analysis. 

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

The first conclusion we can draw from our analysis based on launch date is that the most successful month to start a theatre Kickstarter campaign is May and the lease successful is in December.  

- What can you conclude about the Outcomes based on Goals?

We can conclude that the outcomes for the campaigns is not particularly related to goal of the campaign and that other factors are more likely to be the deciding factor on whether a campaign is successful.

- What are some limitations of this dataset?

Some of the limitations of this data set are that it doesn't include the amount spent on advertising for a campaign which could have a great impact on the outcome. There are also only aproximately 4000 results in the data set and that might not be large enough to allow for significant analysis. 

- What are some other possible tables and/or graphs that we could create?

I would want to create a graph that show the percentage of all successful campaigns across all subcategories so that it would be simple to see which subcategories were most successful. If only 5% of the theatre Kickstarters were successful versus 80% of the children's books that would be something to take into consideration. 
