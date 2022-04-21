# French Box Office 
IS THE SUCCESS OF A MOVIE PREDICTABLE ? 

<img src="https://bit.ly/2VnXWr2" alt="Ironhack Logo" width="100"/>


## Content
[table des matière]

## Project Description

xx

## Workflow

1. Data Collection - Building a database with the historical data on french box office, movies genres and french box office features.
   - French box office from 2010 to 2019, in number of tickets sold, including the max number of theaters used (jpboxoffice.org)
   - Corresponding movie features such as cast, budget, genre from 2010 to 2019 (themoviedb.com) 
   - NB: the data gathers the total tickets sold from 2010 to 2019, but excludes 
2. Data Cleaning and Processing
   - selection of specific data needed 
   - cleaning and processing of each dataset
   - cleaning and processing of data for Time Series Analysis and Machine Learning
  
5. Time Series Analysis
6. Machine Learning
7. Models testing.
9. Creating Dashboards
10. Preparing the Powerpoint presentation
11. Preparing other deliverables (readme file, Git-Hub repository).

## 01 - Data Collection

The data was collected using API wrapper from themoviedb(https://developers.themoviedb.org/3/) and scraping from jpboxoffice.org with Scrapy. The app to scrap was designed by Artefactory (https://github.com/artefactory/french-box-office/tree/main/app), and we are deeply thankful for this.
The challenge was to understand how to use it and configurate an appropriate virtual environment.

## 02 - Data Cleaning
_______________________________________________________________________________________________________________
The selected data , where cleaned and processed before Time Series and Supervised Machine Learning Analysis. This process was divided into different parts, the files collected were in JSON format, we met a lot of difficulties to be able to use the data

### Cleaning for Time Series Analysis and EDA

The columns which presented relevant information for Time Series analysis were the columns containing the air pollution and date information, i.e. : 'day', 'year', 'total_sales', 'max_theaters_used', 'viewers_by_theaters'.

The process of data cleaning and processing included:

- converting datetime column into datetime type and split date on different columns day, month and year.
- missing values processing:
  - column 'first_screening_sales' was deleted due to the high number of missing values
  - column 'cast' had values of a List type so we decided to split in 6 columns 'cast1','cast1_popularity', 'cast2', 'cast2_popularity', 'cast3', 'cast3_popularity'

### Cleaning for Supervised ML:

The aim of second stage of cleaning was to prepare the data for Supervised Machine Learning. This process included:

-DANIEL-

The cleaned data ready for Time Series and ML was saved in the separate files.

*Using : python, pandas, numpy, matplotlib, seaborn*

## 03- Time Series

Time Series Analysis was performed separately for each pollutant (PM2.5, PM10, ozone and nitrogen dioxide) in each city.
The analysis included:

- Stationarity test - all analysed time series data was stationary.
- Autocorrelation check 
- Decomposition to see trend line.
- Train/test split in proportion 80/20 to evaluate chosen model.
- Fitting the model on the whole available data.
- Plotting important figures.

*Using : python, pandas, numpy, matplotlib, seaborn, statmodels

## 04 - Machine Learning

The purpose of this part of the project was to create a supervised machine learning model, which would correctly predict the succss of a movie.
For the Supervised Machine Learning part 4 models were evaluated:

- Random Forest Classifier,
- Tree classifier,
- KNeighbors classifier,
- Nearest Neighbors classification

The process of Machine Learning Analysis included:

- random train/test split of data in proportion 80/20.
- Features selection using Select From Model, Recursive Feature Elimination and Recursive Feature Elimination with Cross-Validation.
- Hyperparameters Tunning using grid search and randomized search.
- Evaluations of the different models used.
- TOPT implementation:
  - TPOT proposed Stacking Estimator using KNeighbors
- Comparison of obtained results.


## Conclusions

- xx

## Links

[Repository](x)

[Trello]()

