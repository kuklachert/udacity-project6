# Udacity Data Analyst Nanodegree
## Project 6 - Illya Payanov

**Please note**: the main file in this version is *index_final.html* which contains the revised version of the visualisation and is based on the data from *eu_unemployment.csv* and *eu_events.csv*. I renamed the file with my first submission, that didn't meet all specifications, to *index2.html*. The corresponding data files for the first submission are *g8_unemployment.csv* and *globalevents.csv*.

### Summary

The main question that this visualisation tries to shed light on is the following: does data confirm the widespread belief that the economies of the Eastern European countries have benefitted from joining the European Union? One of the most widely used economic indicators is the unemployment rate, so it would be interesting to find out whether the unemployment of the selected countries has decreased since they joined the EU. 

The graphic shows that Poland was the only country to achieve a significant decrease of unemployment after becoming a Member State, whereas the other countries cound only show short-term improvements, sometimes followed by a very steep rise in unemployment starting around 2008, and are now at roughly the same level or even worse off than before were admitted into the EU. The main contributors for this development might have been the crises that were plaguing the global economy between 2007 and 2011.

### Design

As the underlying data is a time series, the choice of the plot type is an obvious one: a line chart. dimple.js allows to create line charts with datapoint markers and ready-made tooltips which is very useful, as you can put further information into the tooltips that isn't hidden from the user. 

Each color in the chart represents a single country, the X and Y coordinates are used to depict numerical data (year and unemployment rate), and the tooltips contain detailed information (exact numbers for each country). Additionally, I decided to encode for every country the exact year it has joined the EU - the corresponding data points are being highlighted using size and fill. This should make the user more curious ('why are these data points bigger and yellow?') and to navigate through tooltips to find out more.

A legend is of course necessary to map the line colors to single countries and to explain the meaning of markers.
Other design decisions (font type, font size, opacity) are of cosmetic nature.

The last design decision, that was inspired by one of my friends' feedback, was to include non-country-specific information about major political and economic events in the EU below the X axis. This data is contained in an additional file (eu_events.csv) and is plotted using text bubbles that are connected to the ticks of the X axis. The years on the X axis are highlighted in case a major event has occurred in that year. 

### Feedback

To provide a complete picture of the progress of the visualisation, I'll start with the feedback I've gotten for the previous version of my visualisation (that has now been discarded).
I'm only including the most interesting feedback and piece of advice here.

**Initial version (see index1.html)**

*Friend 1*: 

"Big red points instantly attract attention and I decided to find out why some countries have more and the other have fewer of them. It's interesting that Japan had a new prime minister almost every year but still did well with regards to unemployment. Japan is kind of an Anti-Italy in this regard".

"Transparent markers on the data points without power change look pretty ugly".

*Friend 2*:

"TBF i think this graph is pretty uninformative compared to the ones you could see in the press, DER SPIEGEL for instance. It's cool to see when changes in power occurred in each country, but there's some global context missing here. You don't see any mention of the 2007-2008 financial crisis, or the European debt crisis, but these are also events that had a major influence on macroeconomic variables. It would be cool if you added this data to your visualisation somehow."

*Friend 3*:

"I spent 2 minutes hovering over data points and got bored. Too little information".

"Also, the lines for the US and France have almost the same color".

**Visualisation enhancements after initial feedback (see index2.html)**

After hearing from my friends, I decided to add/ change the following things:

1) To add further context to the data, I went to Wikipedia and composed a list of major global events between 1991 and 2014 (globalevents.csv) to enhance the infographic. I decided to depict this data along the X axis in form of bubbles. Each year that appears in this dataset is highlighted and accompanied with a light-blue bubble containing the description of the event. The bubbles have been added to the axis using d3.js.

2) With regards to the color palette, it's true that it's not that easy to distinguish between France and the USA if the standard color scheme is used. However I tried creating different palettes using the ColorBrewer site and wasn't satisfied with any of the results. The issue pertains and I found the ColorBrewer palettes less aesthetically pleasing, so I decided to stick with the standard palette.

3) To make the markers less ugly, I just made them smaller. I think they look much more elegant with the size 2.

**Feedback for the revised version (see index_final.html)**

After having my project reviewed and getting my visualisation re-done, I once again asked my friends what they think. This was the most interesting feedback:

*Friend 1*: 

"I see you've changed the selection of countries in the graphic and the text above. I tried to answer the question in the title and for most countries it's far from obvious that there was any improvement. Only Poland's unemployment rate has strongly decreased. Latvia and Estonia had some violent swings around 2008 which is anything but an improvement".

*Friend 2*:

"Including international events on the X axis has made the graphic more readable and comprehensible. I don't think that most countries improved their situation since joining the EU."

### Resources

Apart from the dimple.js (https://github.com/PMSI-AlignAlytics/dimple/wiki) and d3.js (https://github.com/d3/d3/wiki) documentations, I used the following links for my project: 

* http://koaning.s3-website-us-west-2.amazonaws.com/html/d3format.html to modify the number format on the Y axis as well as the tooltips

* http://stackoverflow.com/questions/4540684/java-round-up-any-number for rounding up numbers

* http://dimplejs.org/adhoc_viewer.html?id=adhoc_bar_custom_tooltips to customize tooltips

* https://www.sitepoint.com/community/t/css-text-indent-all-lines/1707 to indent text paragraphs using CSS

* http://stackoverflow.com/questions/32831489/idomatic-way-of-drawing-a-triangle-in-d3 to draw pointer triangles for the bubbles below the X axis.
