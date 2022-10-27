# Phase 1 Project

### Business Problem

Microsoft sees all the big companies creating original video content and they want to get in on the fun. They have decided to create a new movie studio, but they don’t know anything about creating movies. You are charged with exploring what types of films are currently doing the best at the box office. You must then translate those findings into actionable insights that the head of Microsoft's new movie studio can use to help decide what type of films to create.

### The Data

In the folder `zippedData` are movie datasets from:
* [IMDB](https://www.imdb.com/) - Database file containing reference data about movies.  We use this to map year & title to genres.
* [Rotten Tomatoes](https://www.rottentomatoes.com/)  - Flat file containing reference information.  We use this to analyze release scheduling, runtime, and box office sales.
* [The Numbers](https://www.the-numbers.com/) - Flat file containing information about budget & sales.  We use this to analyze budget as a driver of profit & ROI.

For this analysis I also scraped an additional data set:
[Minneapolis Fed](https://www.minneapolisfed.org/about-us/monetary-policy/inflation-calculator/consumer-price-index-1800-) - Inflation data, we use to adjust all dollar figures over time from the above 3 sources to normalize to 2022 dollar values.

## Overview
In launching a studio we seek to maximize profit for any new movie we produce.
That is to say, we are focussed on sales, net profit, and ROI.
This means we are less focussed on reviews & ratings.

## Business Understanding
We need to determine optimal choices for the various inputs that we control as decision makers.
The inputs we do control -  Budget, Genre, Staffing, Scheduling, Run length, and more.

## Analysis

### Genres vs Sales
We can see Action & Adventure are the stand-out genres for box office sales.
![genres](https://github.com/steve-gomes/dsc-phase-1-project-v2-4/blob/master/graphs/genres.png?raw=true)

### Scheduling
Summer & Winter are the busy season for box office sales, with November, December, June and February being the highest grossing months.
![season](https://github.com/steve-gomes/dsc-phase-1-project-v2-4/blob/master/graphs/season.png?raw=true)
![season](https://github.com/steve-gomes/dsc-phase-1-project-v2-4/blob/master/graphs/month.png?raw=true)

### Budget vs ROI & Profit 
We can see that ROI & Profit fall off after a maximum $300M budget.
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

### Specific ideas
* Release a Summer block buster action film in June, with a full $300M budget, roughly 120 minutes runtime
* Release two Adventure films during the Winter holidays, one each in November & December targeting school children, on the shorter end of the 90-120min recommended range, in the $150-200M budget range
* The third best release time is February, so release any films that don’t make the holiday cut then

### Next Steps
Multi-factor drill downs such as:
* Optimal budget for each genre
* Drill into day-of-week and week-of-year time slices
* Look at how time of year & budget interact
* Trends - evolution of popularity by year
* Identifying hit makers in targeted genres
* Etc

### top-level directory layout

    .
    ├── graphs                   # visuals from notebook
    ├── zippedData               # provided input files for project
    ├── .canvas
    ├── .gitignore
    ├── CONTRIBUTING.md
    ├── LICENSE.md
    ├── README.md
    ├── notebook.pdf            # analysis notebook PDF
    ├── presentation.key        # project presentation src
    ├── presentation.pdf        # project presentation PDF
    ├── student.ipynb           # analysis notebook
