# **Analysis and Visualization of Complex Data**
Danilo III O. Gonzales (SN: 29225) <br>
Master's in Green Data Science

### Overview
In this exercise, two data visualization produced by the Deutsche Bank Research and authored by chief economist Torsten Slok were evaluated. The charts were published on March 2020 during the early stages of the COVID-19 Pandemic in the website article entitled ["Coronavirus: Facts & Charts on Covid-19"](https://ritholtz.com/2020/03/coronavirus-facts-charts/), written by Barry Ritholtz. Figure 1 and 2 are shown below.

**Figure 1** <br>
*Cumulative Confirmed Coronavirus [COVID-19] Cases*
![image_1](./graphs/graph_1.png)

**Figure 2** <br>
*Number of Physicians per 1000 people*
![image_2](./graphs/graph_2.png)

### Q1. Main visualization goal (audience)
#### Figure 1
The main goal of the Figure 1 is to help its audience understand how fast COVID-19 is spreading in different countries and tell whether its speeding up or slowing down. Since this was posted on a business institute, there is a huge chance that most of the people that visit the website are businessman or investors and aside from showing the number of confirmed cases through time per country, this can also help them gather insight on which market might stabilize or worsen.
#### Figure 2
On the other hand, Figure 2 shows which countries have more or fewer doctors per person. It gives the audience the insight where different countries stand in terms of healthcare capacity. In this figure, the bar for the US was highlighted in red. This could be because Torsten Slok published the report for US-based clients. This emphasis in the figure helps them easily identify where US stands in the figure.

### Q2. Visualization dimensions using a visualization wheel

In this part, we will use Alberto Cairo's visualization wheel to evaluate both figures. Figures 3 and 4 shows the visualization wheel created for Figure 1 and 2. Table 1 shows the explanation for the dimension score.

**Figure 3** <br>
*Visualization Wheel for Figure 1: Cumulative Confirmed Coronavirus [COVID-19] Cases*
![vizwheel_1](./graphs/vizwheel_fig1.png)

**Figure 4** <br>
*Visualization Wheel for Figure 2: Number of Physicians per 1000 people*
![vizwheel_2](./graphs/vizwheel_fig2.png)


**Table 1** <br>
*Evaluation of Figure 1 and 2 based on Cairo's Visualization Wheel*
|Dimension|Figure 1|Figure 2|
|-|:-|:-|
|Abstraction vs. Figuration|Leans toward abstraction. No actual photos or objects were used and data was represented only using lines|Leans toward abstraction. No actual photos or objects were used and data was represented only using bar|
|Functionality vs. Decoration|Mostly functional. Every element serves its purpose except the arrows which doesn't help much and is more of an additional decoration.|Very functional. Only the usage of the red color to emphasize where US stands is more of a decoration since this is sort of an editorial's choice.|
|Density vs. Lightness|Dense. The graph shows data on nine countries in the span of 36 days. There's a lot going on and it takes more time to comprehend| Light. The graph consists of one number per country (n=22). It is much faster to digest.|
|Multidimensionality vs. Unidimentionality|Moderately multidimensional. It portrays three values: number of days (x-axis), number of COVID-19 cases (y-axis), and country (color of line).|Unidimensional. Only shows one thing which is the number of doctors per country.|
|Originality vs. Familiarity|Mostly familiar. It is a line chart which is one of the common grahps.|Very familiar. Easy to read but nothing unique|
|Novelty vs. Redundancy|Redundant. The left and right y-axes shows the same scale, which adds nothing.| Redundant. There is already a number label on top of the bar so the y-axis is not necessary.|

### Q3. 