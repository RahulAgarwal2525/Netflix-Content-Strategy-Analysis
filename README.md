# 🎬 Netflix Content Strategy Analysis

An end-to-end Data Analytics & Machine Learning project analyzing Netflix’s content catalog to uncover structural patterns in the platform’s content strategy.

This project combines data cleaning, exploratory data analysis, clustering, and business insight generation to understand how Netflix’s content portfolio is structured and evolving.

# 📌 Project Objective

The goal of this project is to analyze Netflix's catalog of movies and TV shows to:

- Understand content distribution patterns
- Identify structural segments in the catalog
- Detect trends in content production
- Generate strategic insights using data
- Apply machine learning techniques for content segmentation

# 📊 Dataset

The dataset contains metadata about Netflix titles including movies and TV shows.

### Key Features
| Feature | Description |
|------|------|
| type | Movie or TV Show |
| title | Content title |
| director | Director name |
| cast | Main cast members |
| country | Production country |
| date_added | Date added to Netflix |
| release_year | Original release year |
| rating | Age certification |
| duration | Runtime (minutes or seasons) |
| listed_in | Genres |
| description | Short summary |

Dataset size: **~8800 titles**

#🧹 Data Cleaning & Preprocessing

Several preprocessing steps were required before analysis.

## Handling Missing Values

Columns such as:

- director  
- cast  
- country  
- rating  

contained missing values.

These were handled using appropriate strategies such as filling with placeholders or excluding rows for specific analyses.

---

## Fixing Data Inconsistencies

Some rows contained incorrect entries where movie durations appeared inside the rating column, for example:

```python
rating = "66 min"
```


These were programmatically corrected by moving them back to the duration column.

## Duration Normalization

The duration column contained two formats:

Movies:
```python
90 min
120 min
```


TV Shows:
```python
1 Season
2 Seasons
```


Numeric values were extracted to enable quantitative analysis.

# 📈 Exploratory Data Analysis

Several analyses were performed to understand content patterns.

## Movies vs TV Shows

Movies dominate the Netflix catalog, while TV shows represent a smaller but strategically growing segment.

## Content Growth Over Time

Netflix experienced rapid catalog expansion after 2015, corresponding with:

- Global market expansion
- Increased original production
- Regional content investment

## Country Distribution

Top content-producing countries include:

- United States
- India
- United Kingdom
- Canada

This highlights Netflix’s strong presence in both Western and emerging markets.

## Genre Analysis

Most common genres include:

- Drama
- International Movies
- Comedy
- Documentaries

Modern content often combines multiple genres, increasing cross-audience appeal.

## Movie Duration Analysis

Movie runtimes were grouped into ranges.

Most Netflix movies fall within the 90–110 minute range, suggesting an optimized runtime for streaming consumption.

## TV Show Duration Analysis

Most Netflix TV shows have only one season, indicating a strategic preference for:

- Limited series
- Short storytelling formats
- Binge-watching friendly content

# 🤖 Content Segmentation Using Machine Learning

To identify structural patterns within the catalog, K-Means clustering was applied.

Features Used

- duration_int
- release_year
- number_of_genres
- rating_encoded

Features were standardized before training.

## Determining Number of Clusters

The Elbow Method was used to determine the optimal number of clusters.

The curve suggested k = 4, indicating four meaningful content segments.

# 🔍 Cluster Interpretation

The clustering model revealed four distinct content segments.

## Cluster 0 — Modern Limited Series

Characteristics:

- Short duration
- Recent release years (~2017)
- High genre diversity

Interpretation:

Modern Netflix content focusing on short-form storytelling and limited series.

## Cluster 1 — Focused Mid-Length Content

Characteristics:

- Medium duration
- Low genre diversity
- Recent release years

Interpretation:

Content designed for specific niche audiences, such as documentaries or focused single-genre productions.

## Cluster 2 — Modern Feature Films

Characteristics:

- Average runtime ~108 minutes
- Multi-genre
- Mid-2010 release years

Interpretation:

Core Netflix feature-length film portfolio.

## Cluster 3 — Legacy Film Catalog

Characteristics:

- Older release years (~1989)
- Longer runtimes
- Lower rating diversity

Interpretation:

Older licensed films forming Netflix’s legacy content library.

# 📊 PCA Cluster Visualization

Principal Component Analysis (PCA) was used to visualize the clustering results.

The PCA projection shows clear separation between clusters, validating the segmentation structure.

# 💡 Key Insights

From the analysis, several important patterns emerge.

## Growth of Short-Form Content

Recent Netflix content increasingly focuses on limited series and shorter storytelling formats.

## Rise of Multi-Genre Content

Modern titles frequently blend multiple genres, improving discoverability and audience engagement.

## Legacy Content as a Separate Segment

Older licensed films form a distinct cluster, suggesting lower integration with modern Netflix content strategy.

## Optimized Movie Runtime

Most successful films cluster around 90–110 minutes, indicating a streaming-optimized duration.

# 📌 Strategic Recommendations

Based on the findings, several strategic recommendations can be proposed.

## Expand Limited Series Production

Short-format storytelling aligns with modern binge-watching behavior and reduces production risk.

## Encourage Multi-Genre Content

Genre blending expands audience reach and improves recommendation engine performance.

## Evaluate Legacy Content Investment

Older catalog films may generate lower engagement relative to modern originals.

Strategic licensing optimization could improve catalog efficiency.

## Maintain Optimal Movie Runtime

Maintaining the 90–110 minute duration range may maximize viewer retention.

# 🔮 Predictions

Based on current trends:

- Limited series will continue to dominate streaming content.
- International content production will increase.
- Genre hybridization will grow further.
- Netflix will rely more heavily on original productions.

# 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- KMeans Clustering
- PCA

# 📁 Project Structure
```python
Netflix-Content-Strategy-Analysis
│
├── data/
│   └── netflix_titles.csv
│
├── notebooks/
│   └── netflix_analysis.ipynb
│
├── README.md
└── requirements.txt
```

# 📌 Future Improvements

Potential extensions of this project include:

- Building a content recommendation system
- Time-series forecasting for future content growth
- Interactive dashboard using Streamlit
- Genre-based recommendation modeling

# 👤 Author

Rahul Agarwal

B.Tech – Computer Science & Engineering

MANIT Bhopal
