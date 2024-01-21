[# PhiloMap](http://88.80.186.165:3838/PhiloMap/)
Visulalizing Philosophers Influence
![philo1](https://github.com/aalbusaidi/PhiloMap/blob/main/www/philo1.png)
a web-based tool that helps students remembering all social network analysis concepts by visualizating, interacting and observing the dynamic of graph and network structure in front of their screens. Students can visualize, interact with the source of influence and the target. I build this tool by downloading data from Wikipedia by accessing its API using SPARQL database and with some syntax of sparql I was able to get data and create relational data. I then used Gephi, converted into GEXF, and finally used java-script tools! The tool I developed is very useful for any instructor teaching Social Network Analysis. It is currently used by some instructors from the US who are teaching SNA.
The tool can be accessed *[HERE](http://88.80.186.165:3838/PhiloMap/)*

# Motivation 
* _(Written & developed Aug 21, 2013)_
  
Ever since I wrote a paper on Arab Spring and formation of virtual groups in Dr. Laura Black class, mining social media (text & data) became like a hobby that I do in my free time with Omani coffee and dates . When I analyzed the role of social media and the diffusion of Arab Spring with big networks (thousands of social actors) , I realized that sociograms/network-visuals can be troublesome. Visuals are supposed to represent meaningful information on a single space, but big networks become chaos.  So, I searched for tools of visualizing network graphs that are very interactive and simple. Luckily, I came across [JavaScript GEXF Viewer for Gephi](https://github.com/raphv/gexf-js) that was developed by [Raphaël Velt](http://raphaelve.lt/) and other contributors. I downloaded the code but I never used it, till last week when I accidentally read Simon Raper amazing work on ['Graphing the history of philosophy'](http://drunks-and-lampposts.com/2012/06/13/graphing-the-history-of-philosophy/). He did an amazing job on mapping most influential philosophers on a single sociogram. Due to my interest in philosophy of science i was caught up with his blog and I was intrigued by the way he collected data. I never knew that Hegel will be the most influential philosopher based on extracting data from Wikipedia. Basically What Simon did is to go to Wikipedia database [(DBpedia)](http://dbpedia.org/About) and extract data of philosophers based on who influenced them. The below image is an article about Hegel from Wikipeida and you can see on the right of the page two things: Influenced, and Influenced By.

![philo2](https://github.com/aalbusaidi/PhiloMap/blob/main/www/philo2.png)

Based on these two pieces of data he was able use SPARQL (a query language) to extract available data of philosophers from DBpedia. However, I came across the same problem of making sense with big social graphs. So, I thought to replicate his work and make it more dynamic, interactive, and meaningful even to the readers who do not have background in relational data. It was a positive excuse to practice [JavaScript GEXF Viewer for Gephi](https://github.com/raphv/gexf-js)  and know how it works. I was inspired by the approach Simon used, so I followed [his instructions](http://drunks-and-lampposts.com/2012/06/13/graphing-the-history-of-philosophy/) to extract data from DBpedia. This was my first time I started learning SPARQL. Having taken database and SQL class in my undergraduate, I realized that SPARQL is far way difficult. However, I used Simon's code below:-

_SELECT * WHERE {
?p a <http://dbpedia.org/ontology/Philosopher> .
?p <http://dbpedia.org/ontology/influenced> ?influenced.
}_

I did little search on Google to refine my search criteria. I was interested to find details about a specific philosophical tradition. I thought this is very important for graduate students. For example, I'm a big fan of the work of Anthony Giddens and If i want to know who influenced his ideas I can search his egocentric network and see who influenced him in which i can go and do further reading about thinkers who influenced him. You can also see people who were influenced by Giddens, so you can predict the the trends of his ideas and where they are going. 
![philo7](https://github.com/aalbusaidi/PhiloMap/blob/main/www/philo7.png)

![philo8](https://github.com/aalbusaidi/PhiloMap/blob/main/www/philo8.png)

