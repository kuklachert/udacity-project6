# Udacity Data Analyst Nanodegree
## Project 6 - Illya Payanov

**Please note**: the main file in this version is *index_final.html* which contains the revised version of the vizualisation and is based on the data from *eu_unemployment.csv* and *eu_events.csv*. I renamed the file with my first submission, that didn't meet all specifications, to *index2.html*. The corresponding data files for the first submission are *g8_unemployment.csv* and *globalevents.csv*.

### Summary

In this project, I decided to visualise the unemployment rates of selected EU countries in the period between 1991 and 2014 (time series extracted from the World Bank database, see *eu_unemployment.csv*). To add further context to the unemployment stats, I accompanied them with the timeline of major events in the EU (*eu_events.csv*), as well as the timeline of political changes (admission into the EU, new Head of State or Head of the Executive, see *eu_unemployment.csv*) in the respective countries.

There are multiple insights that can be gathered from the infographic, such as the positive impact of the EU admission for Eastern European countries (Poland and Czech Republic), the devastating effect of the recent economic crises on the Southern European economies, a correlation between political instability (changes in power) with high unemployment, as well as some individual success stories (such as Angela Merkel's Germany or Spain's improvement under Aznar).

**Compared to my previous submission, I feel that the new data sample provides a much more coherent story, as the countries included are much more interconnected economically (thus allowing to extract individual success and failur stories more reliably) and have similar political systems where changes in power rather accurately reflect the degree of economic stability**.

### Design

As the underlying data is a time series, the choice of the plot type is an obvious one: a line chart. dimple.js allows to create line charts with datapoint markers and ready-made tooltips which is very useful, as you can put further information into the tooltips that isn't hidden from the user. 

Each color in the chart represents a single country, the X and Y coordinates are used to depict numerical data (year and unemployment rate), and the tooltips contain additional information (change in power in a country). Additionally, I decided to mark the data points which contain a change in power and to make them more visible. This should make the user more curious ('why are these data points bigger?') and to navigate through tooltips to find out more.

A legend is of course necessary to map the line colors to single countries and to explain the meaning of markers.
Other design decisions (font type, font size, opacity) are of cosmetic nature.

This is how the first version of the graphic (index1.html) came about. I showed this visualisation to 3 friends of mine to get feedback. After getting feedback, I enhanced my visualisation with additional data and visual elements (see *Visualisation enhancements after feedback*).

### Feedback

I'm only including the most interesting feedback and piece of advice here.

*Friend 1*: 

"Big red points instantly attract attention and I decided to find out why some countries have more and the other have fewer of them. It's interesting that Japan had a new prime minister almost every year but still did well with regards to unemployment. Japan is kind of an Anti-Italy in this regard".

"Transparent markers on the data points without power change look pretty ugly".

*Friend 2*:

"TBF i think this graph is pretty uninformative compared to the ones you could see in the press, DER SPIEGEL for instance. It's cool to see when changes in power occurred in each country, but there's some global context missing here. You don't see any mention of the 2007-2008 financial crisis, or the European debt crisis, but these are also events that had a major influence on macroeconomic variables. It would be cool if you added this data to your visualisation somehow."

*Friend 3*:

"I spent 2 minutes hovering over data points and got bored. Too little information".

"Also, the lines for the US and France have almost the same color".

**Feedback for the revised version of the project**:


### Visualisation enhancements after feedback

After hearing from my friends, I decided to add/ change the following things:

1) To add further context to the data, I went to Wikipedia and composed a list of major global events between 1991 and 2014 (globalevents.csv) to enhance the infographic. I decided to depict this data along the X axis in form of bubbles. Each year that appears in this dataset is highlighted and accompanied with a light-blue bubble containing the description of the event. The bubbles have been added to the axis using d3.js.

2) With regards to the color palette, it's true that it's not that easy to distinguish between France and the USA if the standard color scheme is used. However I tried creating different palettes using the ColorBrewer site and wasn't satisfied with any of the results. The issue pertains and I found the ColorBrewer palettes less aesthetically pleasing, so I decided to stick with the standard palette.

3) To make the markers less ugly, I just made them smaller. I think they look much more elegant with the size 2.

The enhanced visualisation can be found in index_final.html.
Overall I think that with the enhanced data set the infographic has quite a lot of content and still remains pretty navigable.

### Resources

Apart from the dimple.js (https://github.com/PMSI-AlignAlytics/dimple/wiki) and d3.js (https://github.com/d3/d3/wiki) documentations, I used the following links for my project: 

* http://koaning.s3-website-us-west-2.amazonaws.com/html/d3format.html to modify the number format on the Y axis as well as the tooltips

* http://stackoverflow.com/questions/4540684/java-round-up-any-number for rounding up numbers

* http://dimplejs.org/adhoc_viewer.html?id=adhoc_bar_custom_tooltips to customize tooltips

* https://www.sitepoint.com/community/t/css-text-indent-all-lines/1707 to indent text paragraphs using CSS

* http://stackoverflow.com/questions/32831489/idomatic-way-of-drawing-a-triangle-in-d3 to draw pointer triangles for the bubbles below the X axis.
