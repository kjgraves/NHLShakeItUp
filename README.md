# NHL 'Shake It Up'


The goal of this project is to answer the questions:
1. Does 'shaking up the lines' help an NHL team to win or to generate more scoring
2. When should a team 'shake it up?'
3. When should a team NOT 'shake it up?'
4. What are the important features to determine when a team should 'shake it up?'
5. Do different rules apply in the playoffs?

## Organization

I have done (am doing) all the work on this project in Jupyter notebooks which I upload them here as I complete them. This readme file describes each of these notebooks, and provides links to each one for easy movement between files. I include a top-level description of the project on my website (link to come soon - once the project is farther along), if you don't want all of the gritty details.

## What Does 'Shaking It Up' Mean??

Unfortunately, 'shaking it up' is not a well defined term. I seems that most news stories that discuss a team 'shaking up the lines' refers to at least one of the top two lines changing (probably both). For the purposes of this investigation, I will keep it as simple as possible. I define "shaking it up" as **a change to the top line that is not due to injury.**

Surely teams play worse on average if one of their players on their top line is injured. I consider an injury where the player is not a part of the lineup, which for all intents and purposes is the same (since first line players aren't usually healthy scratches or send down to the AHL).

## Description of Notebooks

I do all of the work in jupyter notebooks which are uploaded here.

### [Scrape Lineups](https://github.com/kjgraves/NHLShakeItUp/blob/master/Scrape/ScrapeNHLLineups.ipynb)

This notebook shows how I gather the lineups for this project. I scrape all of the lineup data from https://www.rotogrinders.com, a daily fantasy sports website. I use rotogrinders, because many other websites (e.g. https://www.nhl.com/stats, https://www.hockey-reference.com) do not list starting lineups in their stats (at least, not where I could find).

### [Scrape Additional Data](https://github.com/kjgraves/NHLShakeItUp/blob/master/Scrape/ScrapeAdditionalData.ipynb) (in progress)

This (rather large) notebook shows how I gather all additional features (besides the actual dates and lineups).
So far, these are the data/features I have scraped and where I got the data:

-----
https://www.hockey-reference.com
* Scores 
* Player goals for each game
* Injuries
* +/- of players for each game
* 
----
https://www.nhl.com/stats
* Used as ground truth for attempting to correct for lineup mistakes on rotogrinders

*The later half (concerning the handling of messy data) of this notebook is still very much in progress*

### [Feature Creation](https://github.com/kjgraves/NHLShakeItUp/blob/master/FeatureCreation.ipynb) (in progress)

Much of the data gathered directly from scraping is not in a useful form. In this notebook, I do some more data wrangling to build all of the appropriate features.

List of Features:
* Win/losing streak
* Number of goals in recent (1,2,5,10?) games for the entire team or each line (goals by line probably shouldn't include powerplay or penalty kill)
* Number of goals allowed in recent (1,2,5,10?) games for the entire team or each line 
* Team record up to the current game in the season
* Number of games played recently (e.g. played last night, number in last 3,5,7 days?)
* Others?

### [Data Exploration](https://github.com/kjgraves/NHLShakeItUp/blob/master/DataExploration.ipynb) (in progress)

Finally!! We can actually look at the data now, and try to make some sense of it. Before I dive into any predictive analysis, I need to answer some of the basic questions:
1. When do teams 'shake it up?' Doe certain teams do it more often?
1. On average, does 'shaking it up' work?
2. Does 'shaking it up' work better in certain situations or for certain teams?
3. Is it detrimental in other situations?


### Modeling (not begun)

I plan to do all of my modeling, and show results in this notebook.

Models Needed:
* Prediction of W/L for a single game

## Disclaimer

This is currently a work in progress, and I will update github as I go.
