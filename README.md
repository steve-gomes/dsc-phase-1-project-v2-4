# Phase 1 Project

### Business Problem

Microsoft sees all the big companies creating original video content and they want to get in on the fun. They have decided to create a new movie studio, but they don’t know anything about creating movies. You are charged with exploring what types of films are currently doing the best at the box office. You must then translate those findings into actionable insights that the head of Microsoft's new movie studio can use to help decide what type of films to create.

### The Data

In the folder `zippedData` are movie datasets from:

* [Box Office Mojo](https://www.boxofficemojo.com/)
* [IMDB](https://www.imdb.com/)
* [Rotten Tomatoes](https://www.rottentomatoes.com/)
* [TheMovieDB](https://www.themoviedb.org/)
* [The Numbers](https://www.the-numbers.com/)

Because it was collected from various locations, the different files have different formats. Some are compressed CSV (comma-separated values) or TSV (tab-separated values) files that can be opened using spreadsheet software or `pd.read_csv`, while the data from IMDB is located in a SQLite database.

![movie data erd](https://raw.githubusercontent.com/learn-co-curriculum/dsc-phase-1-project-v2-4/master/movie_data_erd.jpeg)

Note that the above diagram shows ONLY the IMDB data. You will need to look carefully at the features to figure out how the IMDB data relates to the other provided data files.

It is up to you to decide what data from this to use and how to use it. If you want to make this more challenging, you can scrape websites or make API calls to get additional data. If you are feeling overwhelmed or behind, we recommend you use only the following data files:

* `im.db.zip`
  * Zipped SQLite database (you will need to unzip then query using SQLite)
  * `movie_basics` and `movie_ratings` tables are most relevant
* `bom.movie_gross.csv.gz`
  * Compressed CSV file (you can open without expanding the file using `pd.read_csv`)

## Analysis

### Genres vs Sales
We can see Action & Adventure are the stand-out genres for box office sales
![genres](https://github.com/steve-gomes/dsc-phase-1-project-v2-4/blob/master/graphs/genres.png?raw=true)

### Scheduling
Summer & Winter are the busy season for box office sales, with November, December, June and February being the highest grossing months
![season](https://github.com/steve-gomes/dsc-phase-1-project-v2-4/blob/master/graphs/season.png?raw=true)
![season](https://github.com/steve-gomes/dsc-phase-1-project-v2-4/blob/master/graphs/month.png?raw=true)

### Budget vs ROI & Profit 
We can see that ROI & Profit fall off after a maximum $300M budget
![budgets](https://github.com/steve-gomes/dsc-phase-1-project-v2-4/blob/master/graphs/budget_profit.png?raw=true)
![budgets](https://github.com/steve-gomes/dsc-phase-1-project-v2-4/blob/master/graphs/budget_roi.png?raw=true)

### Runtime
Runtime is not that correlated with sales, however we can see a typical range of 90-120min for movie runtime.  Studios are not rewarded for exceeding 120min, and audiences would expect a movie to be at least 90min given the rest of the market.
![runtime](https://github.com/steve-gomes/dsc-phase-1-project-v2-4/blob/master/graphs/runtime.png?raw=true)

## Recommendations & Next Steps

### Recommendation
* Focus your studio on Action & Adventure movies as these genres are the most profitable
* Release films primarily in Winter & Summer seasons, as box office sales show moviegoing is highest in these seasons
* Budget up to 300M per film, as ROI and Profit increases with budget until 300M at which point it drops off
* Keep movie runtime in the sweet spot of 100-120 minutes length as higher run times do not result in higher sales

### Next Steps
Multi-factor drill downs such as:
* Optimal budget for Action & Adventure genres individually
* Drill into day-of-week and week-of-year time slices
* Look at how time of year & budget interact
* Etc
