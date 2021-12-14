
## Louise's Crowdfunding Analysis & Projections

### Summery:

A few months back, Louise reached out because she was gearing up to orchestrate her play, *Fever*, and was concerned with her success rate with the budget that she was given. She requested that
we perform some analytics for her in relation to other crowdfunding campaigns that have taken place in the past, and to see if there were any positive correlations that could be applied
to better increase her chance for a successful campaign. Likewise, if there was any mistakes that she should also avoid. Recently Louise reached back out with the wonderful news that 
*Fever* came close to its fundraising goal in a short amount of time. Now she would like for us to visualize some campaign outcomes based on their launch date and goals.

### Analysis:

I first started with creating a new column in the Kickstarter worksheet (Filtered/Cleaned excel sheet that I created when Louise first sent over the raw data) and derived the 
year in which the campaigns were launched using the function Year() in excel. The reason I want to do this is so that I can get more specific and better representaion from the data 
that I am going to be using for the next step. 

> The Year() function is used to return the year corresponding to a date.
>>[Microsoft] <https://support.microsoft.com/en-us/office/year-function-c64f017a-1354-490d-981f-578e8ec8d3b9>

###### Creating the Pivot Chart:

Following that, I created a pivot table that would allow me to assimilate the data from the Kickstarter worksheet into an easier format that would allow me to filter topics such as the 
parent category and years involved. It would also display topics such as the amount that succeeded, failed, and canceled in their campaigns, and in which month those occurred. I then actively 
filtered for theater in the parent category and created a line chart to help visualize the relationships between outcomes and launch month.

- I originally had issues with getting my pivot chart to show the months. So I had to highlight all the data that was present when I added the Date Created Conversion to the rows column and group it together. I then went to the group selection tap and selected months to get it to present corectly. 

#### Pivot Chart:

>![Theater_Outcomes_Pivot_Table](https://user-images.githubusercontent.com/95380144/145981973-08e9a4df-de8e-41fb-a83c-eb219e5ef958.png) 

#### Line Graph For Outcomes and Launch Months:

>![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/95380144/145983806-3647e31e-1fad-4e11-a562-021efee59143.png)

###### Creating the Outcomes vs Goal Table:

The next step I took to help Louise and her aspirations flourish was to create a sheet in the Kickstarter campaign that would illustrate the outcomes based on the goals. The way I went
about this was to create a table that could be used later to help visualize the percentage of successful, failed, and canceled plays based on the funding goal amounts from the subcategory I extracted 
earlier. I started by using the function CountIfs() with its corresponding criteria ranges to count the occurrences of successful, failed, and canceled campaigns within a $5000 range.

>The COUNTIFS() function applies criteria to cells across multiple ranges and counts the number of times all criteria are met.
>>[Microsoft] <https://support.microsoft.com/en-us/office/countifs-function-dda3dc6e-f74e-4aee-88bc-aa8c2a866842>

#### Active CountIfs() Formula:

>![Outcomes_Based_on_Goals_Formula_CountIfs()](https://user-images.githubusercontent.com/95380144/145994254-018e24a1-759f-4bed-9729-14b5b0689c35.png)
* After writing the CountIfs() function I inserted the criteria that I wanted it to pull the data from. In this example, it was the parent sheet Kickstarter, followed by cells in which I wanted it to search, and lastly the data that I specifically was searching for. It was challenging because of the second criteria I had to insert for the range. 

#### Data Table After Inputting CountIfs() Formula:

>![Outcomes_Based_on_Goals_Table](https://user-images.githubusercontent.com/95380144/145994734-6a639318-65eb-4edd-a861-d812ee4d847d.png)

After getting all the data inserted and formulated correctly, I added the cells (Successful, Failed, and Canceled) together to get the total projects that were associated with the target class.
I then used a simple formula to get the percentage of each of those categories as well. Following the entire process up by creating a line graph to better represent the data for the correlation. I filtered
the graph to only show the percentage for each segmented range (every $5000) to which I have attached below. 

>The SUM() function adds values.
>>[Microsoft] <https://support.microsoft.com/en-us/office/sum-function-043e1c7d-7726-4e80-8f32-07b23e057f89>

>Finding percentage in excel is easy if you divide the part against the whole. 
>>[Microsoft] <https://www.microsoft.com/en-us/microsoft-365/blog/2011/08/02/how-to-do-percentages-in-excel/>

#### Line Graph for Outcomes vs Goals:

>![Outcomes_vs_Goals](https://user-images.githubusercontent.com/95380144/145995214-7b2111cb-75bc-45e6-81b4-85f114a72237.png)

### Results:

#### Theater Outcomes by Launch Date:
1. The **best** time to launch a new campaign is in May.
2. The **worst** time to launch a new campaign is in December.

#### Outcomes Based on Goals:
1. You will have the best success if you can keep you goal for a campaign under $15,000, although the most successful campaigns have been in the $1,000-$5,000 range. 

#### Limitations:

Some of the limitations of the data would be things such as the reasoning behind the success, fail, or cancelation of the campaigns. There are many external factors that can play
a role in that. Another is the sample size, with more data comes better accuracy with statistics. 4,100 points of data is a good start, but more is better in this situation. The last that I
would like to mention is the demographic of the age in which we are looking to crowdsource from. There are a lot of ways to get funding for projects likes plays and theater events and the
ages of the people that will be attending or contributing to it plays a major role in how you want to set the entire process up. From the stage to the actors, plays, marketing, etc. So, it 
would have been beneficial to Louise to know what audience she is trying to appease to. 
