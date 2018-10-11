# Disaster-Location-Mapping-And-Warning-System

## Objective

The objective of our project is to build a location tagged early warning system for disasters by analysing the posts on social media sites like Twitter.

## Proposed Solution 

For this purpose, the system continuously ingests data from social media sites like Twitter, processes it (i.e., using machine learning classification techniques), classifies it into one of the several categories(like damages, need food and resources, people stuck etc). We also use the geo tagged information from the tweets to identify the latitudes and longitudes on world map in real time. The volume of tweets originating from a particular region are analysed and if the number exceeds certain threshold then we predict a disaster, followed by notifying the relief teams and government about the location.

## Architecture and Implementation

* It consists of four core components; collector, tagger, mapper, notifier.
* The collector is responsible for data collection from  Twitter  using  the  Twitter
streaming API. 
* The collected tweets are then passed to the tagger, it is responsible for the classification of each individual tweet to one of the user-defined categories (e.g., donations, damage, casualties, etc.). The tagger is comprised of three modules:  feature extractor, learner, and classifier.
* Then using latitudes and longitudes of the tweet, the mapper plots the tweet to the world map.
* When a large volume of tweets starts popping out from a small geo-location then the notifier detects that event, parses the tweets and sends the summarized report to disaster relief agencies as the warning.

![architecture](https://image.ibb.co/ecui69/aidr.png)

## Expected Impact 

We believe our solution can help government and disaster relief teams in following ways:
  * Quickly developing situational awareness of disaster and analyzing where the critical infrastructure should be deployed.
  * Seeing how different groups in the community are impacted.
  * Prioritizing the resources to save more lives.
  * By providing tactical and actionable information to disaster relief agencies.
