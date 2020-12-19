# Kickstarting with Excel

## Overview of Project

### Purpose

  An aspiring playwright, Louise, utilized the crowdfunding platform of Kickstarter to attempt to raise over $10,000 to finance her latest play. While her crowdfunding campaign was fairly successful, having come close to raising its full fundraising goal in just a short amount of time, Louise is interested seeing in how other Kickstarter campaigns similar to hers fared based on their different launch dates and fundraising goals. Were these campaigns more successful? Less successful? These are the questions Louise is interested in. By utilizing data analysis and visualizations, these questions will be answered and Louise will know what new adjustments to make to ensure more successful Kickstarter campaigns in the future.    

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

As mentioned, Louise is interested in seeing how similar theater-related Kickstarters with some differing variable parameters performed in comparison to hers.  One of these variables was the launch date of the Kickstarter campaign. Before commencing this particular analysis, it was imperative to first create an additional column in the raw Kickstarter data from the “Category and Subcategory” column called “Parent Category” as this would allow the analysis the ability to specifically drill down to the *type* of campaigns we are focusing on which, in this case, are theater-related campaigns. 

After this initial step, an additional column named “Years” was created by capturing the individual year from the “Date Created Conversion” column using the Excel Year() function. With this column created, the raw Kickstarter data is now ready to be pivoted. By creating a pivot table and putting the following columns in these particular pivot fields, "Parent Category" and "Years" to Filters, "Outcomes" to Columns, count of "Outcomes" to Values, and "Date Created Conversion" to Rows, it allows the ability to view the counts of each specific campaign outcome at a monthly view. Since Louise is only interested in theater-related campaigns at this point, the "Parent Category" filter is set to "theater" and, as she is just interested in completed campaigns, the "live" selection is filtered out of the "Outcomes" field as well.  The finalized pivot table appeared as follows:

<img src = "https://github.com/Jafranco96/kickstarter-analysis/blob/main/Outcomes_Pivot.png"/>

While the pivot table is certainly useful in obtaining the conclusions from the analysis, a more clear, concise, and high-level way to draw these conclusions would be to create a visualization from the data, in this case a line chart would be the most appropriate visualization method. Creating a line chart from the pivot data results in the following chart where we can accurately and quickly infer how the launch dates affect the outcomes of theater-related campaigns.


### Analysis of Outcomes Based on Goals

The second variable Louise is interested in analyzing its effect on a campaign’s outcome is the fundraising goal. For example, are campaigns with lower fundraising goals much more successful than those with higher goals? Is there a specific fundraising range that has the most successful percentage outcome? This is the purpose of this particular analysis.  To perform this analysis, a new table was created in the following format:

To populate the “Number Successful”, “Number Failed”, and “Number Canceled” columns, the Excel COUNTIFS() function was utilized.  By categorizing both the specific fundraising range and outcome, along with having the “Subcategory” column fixated on the “plays” category, the formula returns the precise count of cells that meet all three conditionals within the data. This procedure is repeated until all three columns are completely populated, with the “Subcategory” filter on “plays” as the only constant in the formula. After this, the Excel SUM() function is used on each row to populate the “Total Projects” column.  Lastly, the “Percentage Successful”, “Percentage Failed”, and “Percentage Canceled” columns are populated for each fundraising range. The finalized table appeared as follows:

Like in the previous analysis, a visualization of the data will quickly lead to identifying the analysis outcomes, so a line chart with the fundraising goal ranges on the X-axis and the outcome percentages on the Y-axis was created. From this line chart below, the fundraising goal ranges with the greatest success percentages are readily apparent. 

<img src = "https://github.com/Jafranco96/kickstarter-analysis/blob/main/Outcomes_vs_Goals.png"/>

### Challenges and Difficulties Encountered

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

- What can you conclude about the Outcomes based on Goals?

- What are some limitations of this dataset?

- What are some other possible tables and/or graphs that we could create?


