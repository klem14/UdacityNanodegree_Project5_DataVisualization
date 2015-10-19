Summary
Are the flights always on time, and the ones delayed or cancelled statically insignificant. As a casual traveler I have already experienced a couple of flight delays and even cancellation (am I just unlucky then?).
Do the ageing infrastructures and the growing number of connection contribute to increase the delays and cancellations, or the aircrafts innovation and improved reliability lower them?
Surprisingly, the percentage of delays and cancellations hardly gets under 10%. By 2001-2002 the situation had improved, but from that point on, it then constantly deteriorated until 2008.


Design
I chose to represent the flights information on a (US) map, so it provides a good overview of all the airports.
Each airport is marked as a circle, whose size (i.e. diameter) is function of the number of flights landing on (I focused only on the destination airport).
Depending on the number of delays and cancellation it suffered, the airport will be filled with different colors (from green to red, that is, from normal to very critical).
Finally, the map is meant to be analyzed per year, so when loading it will update through the different years available in the dataset. Afterward the user can take on, and select the year he wants to analyses in more details via a slider.

Based on the feedbacks I received, I:
- added a legend for better understanding of the chart. 
- kept only three colors (green, orange, red) for a better perception of the levels of delays and cancellations.
- changed the title to be self-explaining.
- added tooltip so the users can access the pieces of information drawn.

Feedback - include all feedback you received from others on your visualization from the first sketch to the final visualization
“Great map! I like the animation and found it well done. I however had hard time to figure out what kind of data was shown up. I think, a legend is mandatory here.”
Nicolas G.

Resources:
US state map TopoJSON data: https://gist.githubusercontent.com/stuartlynn/fb148318c332ac8360f5/raw/c0a59badd26d6736b5b65faf1241ee2ddb85c724/usstates.json
D3 Wiki API references: https://github.com/mbostock/d3/wiki/selections
Slider library (adjusted to my needs): https://github.com/MasterMaps/d3-slider
adding a legend: http://bl.ocks.org/mbostock/4573883
