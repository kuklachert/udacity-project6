# Udacity Data Analyst Nanodegree
## Project 6 - Illya Payanov

### Summary

In this project, I decided to visualise the unemployment rates of the G8 countries in the period between 1991 and 2014 (time series extracted from the World Bank database). To add further context, I accompanied the unemployment time series with the timeline of major global events as well as the timeline of political changes (new Head of State or Head of the Executive) in the respective countries.

The aim of the infographic was to let the user explore the data and make her own conclusions about what drives unemployment rates across the world. In my opinion there are multiple stories one can find in this graphic, e.g. some countries' remarkable decrease in unemployment after changes in power (most notably Germany during Angela Merkel's reign), the devastating effect of the financial crisis all over the world, or the correlation between political stability (low number of changes in power) with low/decreasing unemployment, which can be well seen on the examples of Italy and Germany (but is contradicted by Japan). 

### Design

As the underlying data is a time series, the choice of the plot type is an obvious one: a line chart. dimple.js allows to create line charts with datapoint markers and ready-made tooltips which is very useful, as you can put further information into the tooltips that isn't hidden from the user. 

Each line represents a single country, the X and Y axes are used to depict numerical data (year and unemployment rate), and the tooltips contain additional information (change in power in a country). Additionally, I decided to mark the data points which contain a change in power and make them more visible. This should make the user more curious ('why are these data points bigger?') and to navigate through tooltips to find out more.

A legend is of course necessary to map the line colors to single countries and to explain the meaning of markers.
Other design decisions (font type, font size, opacity) are of cosmetic nature.

This is how the first version of the graphic (index1.html) came about. I showed this visualisation to 3 friends of mine to get feedback.

As I mentioned in the summary, the goal of this graphic was to create a user-driven narrative where every user finds different stories and snippets of information on her own, by navigating through the graphic. After getting feedback, I enhanced my visualisation with additional data and visual elements.

### Feedback

I'm only including the most interesting feedback and piece of advice here.

*Friend 1*:
