# Title
Evolution in music through the years. [Blog Post](https://maxpr.github.io/ADA/project/DataStory/)

# Abstract

The music world is constantly increasing with lot of songs published everyday from all over the world. Moreover, the world is becoming more connected and this helps to spread music popularity. We want to understand how music popularity evolved in the last roughly 60 years, as music is a really important social factor. People express themselves, and lot of cultural events and customs are derived from it.
This popularity could help explain some movements influence, the creation of some music styles and what makes a song popular.
If there was a "perfect" composition it would be interesting as it has also become a money-making industry.
We will use the dataset from MillionSongDB, coupled with some website such as The Echo Nest API (now Spotify) and musicbrainz.


# Research questions

- Which features did change (e.g. bpm, beats)?
- How did genres change (e.g. popularity, features of specific genres, higher variance)?
- How did the distribution of music change (e.g. change of number of genres, variance of features)?
- Which songs from the past are still trending (why)?
- How did song titles (artist names) change over time?
- Where did (which) songs get released at which time (do dependencies exist between similar Songs)?

# Dataset
We want to use the dataset from MillionSong DB.  
It consist of .h5 files containing song, classified in different subfolders.
For each .h5 files, we can use the method given in the hdf5_getters provided by the website to extract useful information.
The most important one is the .get_num_song(file) that return the number of rows in the actual files, then you can get lot of information on the artists, songs, etc.
The fields that could be exploited are mentioned on the following wepage in the field list paragraph: https://labrosa.ee.columbia.edu/millionsong/faq .  
Furthermore a few additional files with aggregated data (e.g. longitude, similarities, year) can be bundled via offered scripts: https://labrosa.ee.columbia.edu/millionsong/pages/getting-dataset.  
Genres are called "terms" in the dataset. The genres of an artist can be fetched from the field "artist terms". Or from one of the additional files.
There are several features which have been calculated with algorithms: BPM ("tempo"), dancabilty, duration, etc.
Possibly further facts can be retrieved from the Spotify API since the Echo Nest API is shut down.  
Since the dataset is quite large and we will start to look in the additional files to get as much simple information as we can.
Furthermore, a subset exits, which we can use for first tests.
Later on, we can fetch additional information from the whole data set.


# A list of internal milestones up until project milestone 2

**03.11.2017**: Prepare subdataset locally

**05.11.2017**: Analysed additional files

**10.11.2017**: Fetched data from subdataset and APIs, create functions for additional data collection

**17.11.2017**: Functions created for explanatory data analysis on subdataset

**19.11.2017**: Prepared complete dataset on cluster

**24.11.2017**: Applyed created functions on whole dataset, do needed modifications

**26.11.2017**: Extended functions and analysis for whole dataset, prelimiary result

**28.11.2017**: Rechecked prelimiary result, updated plan

**03.12.2017**: Relevant conclusions drawn

**08.12.2017**: First blog design

**15.12.2017**: Data visualisation

**19.12.2017**: Finalized Data Story and notebook

**29.01.2018**: Create poster, demo of visualisation

# Questions for TAa

Is there a possibility to convert IDs from the dataset to Spotify URNs?


# What did each group member did  

**Maximilian Rünz** = Data fetching from cluster, Descriptive Statistics, Feature Analysis, Genre mapping, Genre Dataframes, Genre Distribution, Website (HTML+JS), Text spelling corrections   
**Max Premi** = Cluserting, Mapping to genre improving, Interactive Plot by genre, Some Data Cleaning, Analysis of Result for Feature Analysis, Text for DataStory
