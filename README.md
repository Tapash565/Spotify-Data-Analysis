# Spotify Data Analysis with Python

An exploratory data analysis (EDA) project that uses Python to investigate Spotify track data, identify relationships between audio features, and uncover patterns in song popularity, release activity, duration, and genres.

## Project Overview

This project analyzes Spotify music data to understand how track characteristics such as **energy, danceability, acousticness, loudness, tempo, and popularity** relate to one another.

The analysis is implemented in a Jupyter Notebook using **Pandas, NumPy, Matplotlib, and Seaborn**. It covers data inspection and cleaning, descriptive statistics, correlation analysis, regression visualizations, release-year analysis, and genre-level exploration.

## Objectives

* Understand the structure and quality of Spotify track and artist datasets.
* Identify missing values and inspect data types and memory usage.
* Explore the most and least popular songs.
* Calculate descriptive statistics for numerical track attributes.
* Examine correlations between Spotify audio features.
* Investigate relationships such as:

  * Loudness vs. Energy
  * Popularity vs. Acousticness
* Analyze song releases and duration across years.
* Combine track and artist information to investigate genres.
* Identify genres associated with higher popularity and longer total song duration.
* Extract insights that can support playlist curation and music-industry decisions.

## Dataset

The notebook works with two CSV files:

* `tracks.csv` — Spotify track-level information.
* `artists.csv` — artist information, including genre data.

Important track attributes explored in the notebook include:

| Feature        | Description                                      |
| -------------- | ------------------------------------------------ |
| `name`         | Song title                                       |
| `artists`      | Artist name(s)                                   |
| `popularity`   | Spotify popularity score                         |
| `duration_ms`  | Track duration in milliseconds                   |
| `danceability` | Suitability of a track for dancing               |
| `energy`       | Perceived intensity and activity                 |
| `tempo`        | Estimated tempo in BPM                           |
| `acousticness` | Confidence that a track is acoustic              |
| `loudness`     | Overall loudness in decibels                     |
| `valence`      | Musical positiveness                             |
| `release_date` | Track release date                               |
| `genres`       | Artist genre information from the artist dataset |

> **Note:** The exact fields available depend on the version of the public Spotify dataset used with the notebook.

## Technologies Used

* **Python 3**
* **Jupyter Notebook**
* **Pandas** — data loading, cleaning, transformation, and aggregation
* **NumPy** — numerical operations
* **Matplotlib** — data visualization
* **Seaborn** — statistical visualization

## Project Structure

```text
Spotify-Data-Analysis/
│
├── Spotify Data Analysis.ipynb
├── tracks.csv
├── artists.csv
└── README.md
```

## Analysis Workflow

### 1. Import Libraries

The project begins by importing the Python libraries required for data manipulation, numerical analysis, and visualization.

### 2. Load and Explore the Data

The track and artist CSV files are loaded into Pandas DataFrames.

The notebook examines:

* Number of rows and columns
* Data types
* Dataset information
* Memory usage
* Missing/null values
* Descriptive statistics

### 3. Popularity Analysis

The notebook identifies:

* The 10 least popular songs.
* Highly popular songs, including tracks with popularity scores above 90.
* Top songs based on the Spotify popularity metric.

### 4. Data Transformation

Several transformations are performed:

* `release_date` is converted to a datetime index.
* Track duration is converted from milliseconds to seconds.
* A cleaned artist ID is extracted from the track data to support merging with the artist dataset.
* Track and artist data are merged to bring genre information into the analysis.

### 5. Correlation Analysis

A Pearson correlation matrix is calculated for numerical variables and visualized using a heatmap.

This helps identify positive and negative relationships between Spotify audio features and popularity.

### 6. Regression Analysis

A sample of the track dataset is used for regression visualizations to make large-scale analysis more manageable.

The notebook explores:

* **Loudness vs. Energy**
* **Popularity vs. Acousticness**

These plots help visualize potential relationships between Spotify track characteristics.

### 7. Time-Based Analysis

Release dates are used to study music activity over time.

The notebook visualizes:

* Number of songs released per year.
* Track duration across release years.

### 8. Genre Analysis

Track and artist datasets are merged using artist IDs.

Genre information is then used to explore:

* Genres associated with total song duration.
* Highly popular genres and tracks in the merged dataset.

## Visualizations

The project includes several visualization techniques:

* **Correlation Heatmap** — relationships among numerical features.
* **Regression Plots** — relationships between selected variables.
* **Histogram** — number of songs released by year.
* **Bar Chart** — track duration across years.
* **Horizontal Bar Chart** — genres ranked by total duration.
* **Genre/Popularity Bar Chart** — popularity-related genre analysis.

## Key Questions Explored

The project is designed to answer questions such as:

1. Which songs have the highest and lowest popularity scores?
2. Which audio features are strongly correlated?
3. Is higher energy associated with greater loudness?
4. Is acousticness related to song popularity?
5. How has the number of released songs changed over time?
6. How does song duration vary across release years?
7. Which genres account for the greatest total song duration?
8. Which genres appear among the most popular tracks?

## Business & Music-Industry Applications

### Playlist Curation

Audio-feature relationships can help create playlists based on characteristics such as:

* High energy
* High danceability
* Acoustic sound
* Positive valence
* Specific tempo ranges

### Content Strategy

Popularity and genre analysis can help identify patterns in the types of tracks receiving stronger engagement.

### Music Discovery

Release-year and genre trends can support music discovery systems by highlighting emerging patterns in music characteristics.

### Artist & Genre Analysis

Combining track and artist datasets provides a foundation for studying how genres and artists perform across different periods.

## Data Quality & Interpretation Notes

* A popularity score should be interpreted as the dataset-provided Spotify popularity metric rather than a direct count of streams.
* Correlation does **not** imply causation.
* Genre analysis depends on successful artist-to-track ID matching and the genre labels available in `artists.csv`.
* Regression visualizations use a sample of the full dataset.
* Missing or inconsistent values should be reviewed before drawing conclusions from another version of the dataset.
* Track duration is converted from milliseconds to seconds for easier interpretation.

## How to Run the Project

### 1. Clone or Download the Repository

Place the notebook and both CSV files in the same project directory.

### 2. Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### 3. Launch Jupyter Notebook

```bash
jupyter notebook
```

### 4. Open the Notebook

Open:

```text
Spotify Data Analysis.ipynb
```

## Project Outcome

The final outcome is an exploratory Spotify analytics workflow that transforms raw track and artist data into statistical summaries and visual insights.

The project demonstrates practical skills in:

* Data Cleaning
* Data Transformation
* Exploratory Data Analysis
* Statistical Analysis
* Correlation Analysis
* Data Visualization
* Dataset Merging
* Time-Series Analysis
* Genre Analysis
* Business Insight Generation
