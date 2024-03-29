# Concept of Keystone Species in Web Systems: Identifying Small Yet Influential Online Bulletin Board Threads

This is the data we used in the Ejima, Oka and Ikegami 2019 paper in the *proceedings of the 11th ACM Conference on Web Science (WebSci '19)*. The paper can be found [here](https://doi.org/10.1145/3292522.3326023).

## Abstract 
Research is being conducted to understand social and innovative behavior in human interactions on the Web as a biological ecosystem.
Keystone species in a biological ecosystem are defined as a set of species that significantly impacts the ecosystem if they are removed from the system, irrespective of its small biomass. Identifying keystone species is an important problem as they play an important role in maintaining diversity and stability in ecosystems.
A human community in the web system also possesses keystone species. They can be influential users or contents on the web systems, even though their commitments to the web are relatively small. 
We use data from an online bulletin board, and identify kestone threads (= "species") that have a large impact if they are removed or become unpopular, despite their small population size.
Here, the removal of threads can be regarded as a state in which there is no attention or actions by users on the thread. 
The multivariate Hawkes process is used to measure the degree of influence among all threads and calculate the overall activity level on the online bulletin board. 
Our analysis confirms that keystone threads do exist in the system.
Apparently, the number of keystone species increases along with the service maturation. 
The keystone concept in online services proposed in this study gives a new viewpoint for their stable operation.

## Description of data
In this study, we use data from online bulletin boards in the following two types of communities, provided by [QON, Inc.](https://www.q-o-n.com/en/)

* before or during pregnant women (community A)
* mothers who are raising children (community B)

Each community has threads and users enjoy to communicate with others by commenting and clicking claps for threads and/or comments in the threads.

The types of event occurrence are the following:

* accesses: the datetime of user access to the thread
* comments: the datetime of user comment to the thread
* claps: the datetime of user clap to other user's comment

We used all these three types of event occurrences as action sequences.

The data acquisition period for each community is approximately one and a half years.
We devided this data into 2 weeks and got 30 valid windows for community A and 34 valid windows for community B.
The event occurrence time of the first event in each window is set to 0, and the timestamps of the subsequent event occurrences are represented in seconds.
The data of each window is sroted in a directory in which timestamps for each thread are written in a file.
A unique ID is set for each thread.

## Note
We disregard threads having less than 50 actions in the event sequences, as fitting cannot be performed if the number of actions is too small.

## License
© 2019 Association for Computing Machinery.
