This repository contains a notebook and datasets that will be used to explore and analyse global mortality data for the years through 1987 to 2021, 
focusing on four classes of cause of death or health conditions, including communicable diseases, non-communicable diseases, ill-defined diseases, and injuries.
The primary objective is to explore patterns and trends in mortality rates for different health conditions, 
and determine how these rates vary across different regions, countries, sex and age groups.
The datasets, in csv formats were read in and merged into a single dataframe, merged_deaths_df. 
All libraries imported and used in the notebook are all pre-installed packages.
Some key functions created to curb repitition of codes include: 
read_data(csv_filename), reads a csv file to return a dataframe after cleaning it by dropping irrelevant rows and columns and filters the desired years.
Also worthy to note is that the dataset set had issues of extra commas, this altered the desired output dataframe.
so in the above function, i also included the index_col=False to handle that.
plot_death_trends(df, number_of_deaths_column, title_suffix='') was created for comparative analysis of the number of deaths for each category across the regions. 
the parameters include the dataframe, the column for a particular category of cause of death and the title of th plot.
plot_trend is also a function defined to plot trends categorized by the four category of cause of death for each region.
plot_deathrate_distribution was also defined to filter Europe region and plot age sex-specific distribution.
for ANOVA long_format_df was used to modify the data and create a dataframe that is suitable for it. one-way ANOVA was employed.
for the post hoc test, the tukey hsd library was used for the pairwise comparison.
The multiple linear regression model was trained to predict total deaths. this yielded an R-square of 0.99 but the model was not hypertuned.
looking to investigate other models in future.
