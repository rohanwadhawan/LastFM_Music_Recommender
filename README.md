# LastFM Music Artist Recommender!

A content-based music artist recommendation system built using the Last.fm API.

## What it does
Clusters 810 of the most popular artists on Last.fm by genre tags, then recommends similar artists based on their tag profiles.

## How it works
- Fetches artist and tag data from the Last.fm API
- Builds a 810 x 60 matrix of artist-tag scores
- Normalises and clusters artists using KMeans
- Recommends similar artists using cosine similarity within clusters
- Validates recommendations against Last.fm's own similarity scores
- Current validation scores can be improved, largely due to the tags in the API's data being generic 

## Libraries used
- pandas, numpy, scikit-learn, matplotlib, requests

## Setup
1. Get a Last.fm API key at https://www.last.fm/api
2. Create a `.env` file with `LASTFM_API_KEY=your_key`
3. Run the notebook