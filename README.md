# Movie_Dashboard

Movie_dashboard, a Jupyter Notebook that shows useful info IN ITALIAN about cinema industry of period between 1984 and 2020.

![Movie_dashboard](/images/Movie_dashboard.png)

## ATTENTION! THIS REPOSITORY IS ARCHIVED. FEEL FREE TO FORK IF YOU WANT: GIVE CREDIT TO THE ORIGINAL PROJECT

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
    </li>
    <li>
      <a href="#sources">Sources</a>
    </li>
    <li>
        <a href="#built-with">Built With</a>
   </li>
    <li>
        <a href="#prerequisites">Prerequisites</a>
   </li>
    <li>
        <a href="#creators">Creators</a>
    </li>
  </ol>
</details>

<!-- ABOUT THE PROJECT -->
## About The Project

Starting feature (columns) of the dataset:
* name
* rating
* genre
* year
* released
* score
* votes
* director
* writer
* star
* country
* budget
* gross
* company
* runtime

### ETL (extract transform and load):
Several operation were applied:
* Feature selection: features released, votes, country, name were deleted
* Rating remapping: from USA to italian movie rating system https://en.wikipedia.org/wiki/Motion_picture_content_rating_system

  dict = {'R':'VM18',
  'PG-13':'VM14',
  'PG':'VM6',
  'Not Rated':'NC',
  'G':'T',
  'Unrated':'NC',
  'NC-17':'VM18',
  'TV-MA':'VM18',
  'TV-PG':'VM6',
  'X':'VM18',
  'Approved':'VM18',
  'TV-14':'VM14'}

* Translation of movie genres in italian (as the dashboard is written in italian)

  dict = {'Comedy':'Commedia',          
  'Action':'Azione', 
  'Biography':'Biografia',
  'Drama':'Drammatico',
  'Animation':'Animazione',
  'Crime':'Giallo',
  'Adventure':'Avventura'
  }

* Added profit info for each film in datatset
* Final dataset: <br>
    ![final_dataset](/images/final_dataset.png)
    <br>
* Samples with missing "score" variable are MAR (missing at random) as there is correlation with "votes" variable
* Other samples are MCAR (missing completely at random) as no relationships were found between the variables
* For missing data in «votes» and «score», a DELETION policy was used
* Others were ignored

### Data visualization
There are 6 plot in this dashboard:
* Choice of movie genre <br>
  ![1](/images/1.png) 
  <br> 
  ![2](/images/2.png)
  <br>
  Shows directors/screenwriters/actors (in 3 DIFFERENT PLOTS) with the greatest number of films produced. Quantitative comparisons using the length of the bars.
  
* Choice of maximum 3 production companies
  <br>
  ![3](/images/3.png)
  <br>
  Shows time evolution of average profit per film. Highlight the profit trend by comparing 3 companies.

* Choice of maximum 3 production companies
  <br>
  ![4](/images/4.png)
  <br>
  Show rating distribution of film production of 3 companies by category. Highlights quantitative comparisons between category for selected companies.

* Choice of maximum 3 production companies
  <br>
  ![5](/images/5.png)
  <br>
  Shows runtime time series of different movie genres. Highlight the trend and allows qualitative comparison.

<!-- SOURCES -->
## Sources:
* [Texas Open Data Portal](https://data.texas.gov/dataset/Movie-Data-Demonstration-Dataset/783c-ev6z/about_data)

<!-- BUILT WITH -->
## Built With

* [Anaconda Navigator](https://www.anaconda.com/anaconda-navigator)
* [Jupyter Notebook](https://jupyter.org/)
* [Python](https://www.python.org/)


<!-- PREREQUISITES -->

### Prerequisites

* Install Ananconda Navigator: https://www.anaconda.com/download
* Install Jupyter Notebook app within Ananconda Navigator (reference: https://www.youtube.com/watch?v=-MyjG00la2k)

<!-- CREATORS -->
## Creators

* [CapoBoss23](https://github.com/CapoBoss23)
* [Danksteak](https://github.com/Danksteak)
