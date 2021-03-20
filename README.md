<b>Extract:</b>
Chelsea Chaussee, Cindy Jones, Lauren Toothaker, and Serena Baker representing "The Bones of Dreamers Past" will be analyzing two data sets from Recreation.gov https://ridb.recreation.gov/download (*** The reservation csv is exceptionally large and cannot be pushed to github. We each downloaded the file and saved the data one folder outside of the repository, in order to look through the data*** When opening jupyter notebook for this file be sure to be one file outside the repostiory or will not work.) and the American National Park Service(via Kaggle) https://www.kaggle.com/nationalparkservice/park-biodiversity?select=species.csv in order to coordinate native plants located near hiking trails.

We will extract the csv formatted data files and join on park name, filter, and perform any additional cleaning as needed on the data to provide a final relational database.

We will then load our final database into an ORM and present a final project report.

<b>Transform/Load:</b>
Starting with the parks.csv we read in the csv file and created an empty list to store our dictionary values. We kept all columns from this file. The collection was then uploaded into a database in Mongo.

<p align="center">
  <img src="https://github.com/CChaussee/Wildlife_in_National_Parks/blob/main/Images/parks_output.PNG" />
</p>
For the species csv, we kept only a few columns and followed the same procedure as before to upload the collection into its own database within Mongo.
<p align="center">
  <img src="https://github.com/CChaussee/Wildlife_in_National_Parks/blob/main/Images/species_output.PNG" />
</p>
The recreation csv went through similar cleanup as the species file and was also loaded into its own database within Mongo. The csv file is over 1 million rows and will take a bit of time to go through the dataset.
<p align="center">
  <img src="https://github.com/CChaussee/Wildlife_in_National_Parks/blob/main/Images/recreation_output.PNG" />
</p>
<b>Summary:</b>
Each data source file has been created to be housed in it's own unique Mongo database. If we were to rework our files, a more usable form of this data would have been creating one Mongo database with multiple collections, one for each of the source datasets. Setting up the data this way would provide a more functional way to answer our original question: What parks could you visit to see certain animals?

Ideally, we would be setting up a collection that holds the unique Park Names and an array of all the species that can be found there. Additionally we would build a collection of unique species and an array of all of the parks that they can be found in. Our third collection would be a unique list of park names and their geocoordinates with an array of all the reservation data of 'nights' stayed.


With this set up, you could identify all of the places to go to see a specific species, you could pick a park to visit based on what species you want to see or you can identify parks that have more total reservations or longer stays to infer a degree of populatrity of the unique parks. The limitations to this last assessment is the lack of information on amount of reservable sites to be able to perform per capita calculations to allow for better comparisons between parks.



<p align="center">
  <img src="https://github.com/CChaussee/Wildlife_in_National_Parks/blob/main/Images/Wildlife%20in%20National%20Parks%20ERD.PNG" />
</p>


