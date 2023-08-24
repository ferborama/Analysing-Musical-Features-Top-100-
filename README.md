# Analysing the Musical Features of Popular Music in the United Kingdom between 2005 to 2022
This repository contains the source code for my MSc Project on "Analysing the Musical Features of Popular Music in the United Kingdom between 2005 to 2022".


## Table of Contents
1. [General Info](#general-info)
2. [Files](#files)
3. [Technologies](#technologies)
4. [Installation and execution](#installation)
5. [Notes](#notes)


### General Info
***
The project code is essentially in two parts: a)"Data collection" using webscrapping and Spotipy/Spotify Developer API b)"Data analysis" containing preprocessing, analysis and modelling using the sklearn library.
Jupyter Python notebooks are provide for data collection and processing/analysis along with CSV files containing input data (sourced March 2023) and output data.


### Files
***
* Data collection.ipynb - Jupyter Notebook for data collection
* Data analysis.ipynb - Jupyter Notebook for data preprocessing, analysis and visualisation
* chartspotifydata.csv - Listing of Annual Top100 chart songs from 2005 to 2022 (from officialcharts.com), combined with their associated Spotify audio feature data
* 600kspotify.zip - a Kaggle dataset of approx, 600k songs with their associated Spotify audio feature data
* kmeans_output.csv - Top100 chart song data with an additional column identifying their K-Means cluster assignment (output of the K-Means clustering sections)


## Technologies
***
A list of technologies used within the project:
* [Python 3](https://python.org) 
* [Jupyter Notebook](https://jupyter.org): Version 6
* [Spotipy Library](https://github.com/spotipy-dev/spotipy): Version 2.22
* [scikit-learn machine learning tools](https://scikit-learn.org/)
* [Matplotlib: Visualization with Python](https://matplotlib.org/)


## Installation and execution
***
The follow instructions assume a working Python 3 / Jupyter Notebook installation:

1. Download all files from this repository into a local folder.
2. Unzip the 600kspotify.zip into your local folder. 
3. Ensure that the Spotipy library (and any prerequisites) is installed (see the library documentation, you may try '!pip install spotipy').
4. To aquire chart data and associated Spotify track audio features, launch and run the Jupyter Notebook file: "Data Collection". The output of this process is already provided for chart years 2005-20022 in the file "chartspotifydata.csv". Note that the Spotify API imposes rate limits and the code provided attempts to limit the request rate.
5. Open the Jupyter Notebook file: "Data Analysing". This contains all preprocessing, analysis and modelling stages.
6. Ensure that all sections of the Jupyter Notebook are run in sequential order, it is particularly important to ensure that the imports and Data Preparation sections are run at the start. Note that some functions have long runtimes, such as the K-Means and Random Forest optimisation algorithms; ensure that these functions have completed before progressing. 


## Notes
***
*Spotify Developer API and Spotipy library were employed in March 2023 with configuration correct at that time. Any subsequent changes to the API or Spotipy library in future versions may require adaptaion of the data collection code.
