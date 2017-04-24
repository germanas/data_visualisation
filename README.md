# Data visualisation project by Germanas

In this project the main goal was to create an explanatory visualisation using either Dimple.js or D3.js. We were given a number of data sets to craft a data story from. For this project I prepared my own dataset. I will try to write a step by step process from start to finish.

## Choosing a dataset  

I was always interested in how people interact online. I am from a small country in Northern Europe Lithuania. We currently are having problems in that one of our neighbors are hiring people or "trolls" to desinform the public through social media and news portals. My idea is to find the patterns in their behavior and create a machine learning model to find and remove their comments. But first step is to find out what are the properties of the trolls. That's why I am going to use EDA and explanatory charts to find out the properties of different people by using their comments on news portals.

To get the data, I have created a web scraper using python to get the comments as simple strings of text and ad them to csv file. Then using python I wrangled the string, appended to pandas dataframe and then cleaned it using R. The dataset included about 16 000 comments. After cleaning and grouping the data by country and average scores I got around 100 observations which was perfect for this project. The full dataset is available at my github repository which I will provide in the refferences. 

## What story can my data tell?

The data that I used for this project consists of about 100 observations with these values: country, time(hours), mean of total comment scores. Using this dataset I planned to figure out if the time and country has any relation to total comment score. Figuring this out will help me in my future analysis. 

For this project I will try to visualise what group of people tend to be agresive trolls and what kind of people gets most support from the community.

## What are my findings.

After I created my visualisation, I could clearly separate different types of people by just looking at the chart. From the chart that i made, we can see that the most positive people comment between 00:00 and 06:00. The most negative people tend to comment at daytime from around 09:00 until 23:00. The most positive countries are Norway, Great Britain and Sweden. The most negative countries being Ireland and Lithuania. From this information we could now start building labels for machine learning algorithm, to separate positive people, neutral and trolls. 

## Design

In this part I will describe my design decisions. I will go step by step from my initial desition to final visualisation. 

### Design process
Before getting some great feedback from my colegue about what chart should I choose, I selected to create a bar graph with x axis as country and y axis as average total comment score. My visual encodings were supposed to be lenght and color for the bars of the graph. I made a rough sketch how would it look like:

![alt tag](http://i.imgur.com/HPPIGnx.jpg)

What this graph is missing is that I planned on adding a time slider later which changes the bar lenght when different time is selected. As my colegue suggested that it's not the best way to show relationship. Then another idea came to my mid. I remembered that the best way to show distribution of time would be a line graph since the direction and color are not the worst visual encodings. I also added an ability to switch countries on and off by clicking on the legend, which provided a great way to compare 2 countries.

![alt tag](http://i.imgur.com/K9u6f6w.jpg)

Then another one of my colegues asked me, how can he know what's the value of the data point in certain position? And maybe the position and placement are better visual encodings to show relationship between 2 variables. So I decided to use scatterplot for my next visualisation. 

After all the feedback i sketched another visualisation and showed to my colegues.

![alt tag](http://i.imgur.com/o6nCW4u.jpg)

All agreed that this one is the best, but I still wanted to add a button to add line plot on the points if needed to better show the distribution. I settled with this sketch and started developing. These are the final visual encodings I chose: 
- Position, placement
- Angle
- Color

![alt tag](http://i.imgur.com/puTG586.jpg)

## Feedback

I tried to get feedback during the sketching and after the final visualisation was coded. I work in IT company and it was quite easy to collect feedback from my colegues. I was showing my sketches to 2 people at first and then I showed my final visualisation to 1 person. Bellow I will try to document each instance of feedback received. Note that these were not documented on a computer and it was mouth to mouth conversation:

- Person1. Person 1 didn't really like the idea of a barchart. He said that It was not the best idea to compare the separate values. He said that maybe I would think about a line chart or a scatterplot, also we discussed and then I decided to add time on x axis.
- Person2. Person 2 and Person 1 discussed how hard it would be to figure out the exact value of point on the line graph. Suggested that maybe I would use scatterplot to better show the relationship. After I created the final sketch they liked the idea and I proceeded to code it.
- Person3. This person tested a working prototype of my visualisation. I asked him if he understands what is the message and he said that it was a good idea to include into text in the visualisation and it helped him to get the message of the visualisation. He had few issues with the legend being in a wrong possition, the Title of the graph was non existant, the wording of the button was not clear and some other minor quality fixes.

Overall everyone understood the message portrayed by this visualisation.

### Refferences
- Full dataset and scraper https://github.com/germanas/delfi_comments 
- Library refference http://dimplejs.org/


