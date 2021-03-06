##Summary
Are the flights always on time, and the ones delayed or cancelled statically insignificant?  
As a casual traveler I have already experienced a couple of flight delays and even cancellation (am I just unlucky then?).  
Do the ageing infrastructures and the growing number of connection contribute to increase the delays and cancellations, or the aircrafts innovation and improved reliability lower them?  
By 2001-2002 the situation had improved, but <u>from that point on</u>, it then constantly deteriorated until 2008.


##Design
I chose to represent the flights information on a (US) map, so it provides a good overview of all the airports. I could have drawn these airports on a categorical chart, but only few people (e.g. travel agents) know the iata codes and airport names by heart. Thanks to the map, users first narrow down the geographical area (state), before paying attention to the airports.

Each **airport** is marked as a *circle*, whose *size* (i.e. diameter) is function of the number of **flights** landing on (I focused only on the destination airport). There are approximately 230 airports shown per year. Having all displayed with a default size would have overwhelmed the map. Relying on the air traffic to set the size of the circle enable me to "hide" the less significant airports and highlight the most important ones.

Depending on the number of **delays** and **cancellations** it suffered, the airport will be filled with different *colors* (from green to red, that is, from normal to very critical). The diverging color scale is highly dependent on the data. Because percentages are included in a [10% - 40%] interval, 4 colors are good enough to cover the full range. More would actually be confusing.

Finally, the map is meant to be analyzed per **year**, so when loading it will update through the different years available in the dataset. Afterward the user can take on, and select the year he wants to analyses in more details via a slider.

Based on the feedbacks I received, I:  

* added a legend for better understanding of the chart.

* kept only three colors (green, orange, red) for a better perception of the levels of delays and cancellations.

* changed the title to be self-explaining.

* added tooltip so the users can access the pieces of information drawn.

##Feedback
[Initial commit](https://github.com/klem14/UdacityNanodegree_Project7_DataVisualization/commit/ac7c9226fb23d720f7b5e5ff39f50acadb579cff)  

1. �Great map! I like the animation and found it well done. I however had hard time to figure out what kind of data was shown up. I think, a legend is mandatory here.�
Nicolas G.

2. �I faced couple of delays myself, and now, I know I am not alone. From now on, I will try to avoid Chicago and Atlanta which show the worst statistics. I however think the yellow color doesn�t provide much information. 3 colors should be enough�
Sebastien C.

[Feedback #1 & #2 commit](https://github.com/klem14/UdacityNanodegree_Project7_DataVisualization/commit/c7ca146ffa6417e740fa87f92b5b3c8b2b0b130d)  

3. �I liked it very much (I would maybe choose another color as background for the map, but that�s details) I think the year by year animation is very powerful tool. It�s a good way of conveying the evolution/trend over the time. I however wish I could somehow access the data behind the map to get more details. What happened in year 2000 to have it all red (above 25%)? Crossing weather forecast / other reasons would be nice to have as a next step�
Claude F.

[Feedback #3 commit](https://github.com/klem14/UdacityNanodegree_Project7_DataVisualization/commit/08db67d0203674c4a0ac016e3f84d54f866b6772)

##Resources:
* [US state map TopoJSON data](https://gist.githubusercontent.com/stuartlynn/fb148318c332ac8360f5/raw/c0a59badd26d6736b5b65faf1241ee2ddb85c724/usstates.json)

* [D3 Wiki API references](https://github.com/mbostock/d3/wiki/selections)

* [Slider library (adjusted to my needs)](https://github.com/MasterMaps/d3-slider)

* [Adding a legend](http://bl.ocks.org/mbostock/4573883)

