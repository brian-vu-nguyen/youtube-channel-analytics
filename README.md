# Veritasium YouTube Channel Analysis

## Overview
This project performs **Exploratory Data Analysis (EDA)** on Veritasium's YouTube channel using the **YouTube Data API v3**. The analysis focuses on extracting video metadata, understanding engagement metrics, and visualizing trends.

## Features
- Extracts **video statistics** (views, likes, comments, etc.) from the YouTube API.
- Converts and processes **video metadata** (e.g., duration, publish dates).
- Performs **exploratory data analysis (EDA)** on:
  - Views per video
  - Likes and comments vs. views
  - Title length vs. views
  - Video duration distribution
  - Video upload schedules
- Visualizes data using **Seaborn** and **Matplotlib**.

## Dependencies
Ensure you have the following Python packages installed:
```sh
pip install isodate google-api-python-client pandas seaborn matplotlib python-dotenv
```

## Installation & Setup
1. Clone this repository:
   ```sh
   git clone https://github.com/yourusername/veritasium-youtube-eda.git
   cd veritasium-youtube-eda
   ```
2. Set up your API key:
   - Create a `.env` file inside the project directory.
   - Add your YouTube API key:
     ```
     api_key=YOUR_YOUTUBE_API_KEY
     ```
3. Run the script to fetch and analyze video data:
   ```sh
   python analysis.py
   ```

## Data Extraction
- Retrieves **channel-level statistics** such as total views, subscribers, and total uploaded videos.
- Extracts **video-level data** including:
  - **Title, description, tags**
  - **View count, like count, comment count**
  - **Video duration, caption availability**
  - **Published date and upload schedule**

## Exploratory Data Analysis (EDA)
### 1. Understanding Video Metrics
- **Top 10 most viewed videos** (Bar chart)
- **Bottom 10 least viewed videos** (Bar chart)
- **View distribution analysis** (Histogram & KDE plot)
- **Likes vs. Views correlation**

### 2. Analyzing Video Duration
- Convert `duration` to seconds for better analysis.
- Compare **video duration vs. view count**.
- Identify trends in **long-form vs. short-form content**.

### 3. Upload Schedule Impact
- Extracts **publish day of the week** for each video.
- Analyzes if certain days have higher engagement.
- Creates a **heatmap of feature correlations**.

## Visualization Examples
- **Pairplot** to compare multiple video features.
- **Heatmap** showing correlations between key metrics.
- **Histograms** and **KDE plots** for understanding distributions.

## Results & Insights
- **Videos with more views tend to receive more likes** (high correlation).
- **Longer videos are more likely to have captions**, but **video length alone does not guarantee high views**.
- **The day of the week does not strongly influence video performance**.
- **Some videos with fewer views still receive a high number of likes**, suggesting **strong audience engagement**.

## Next Steps
- Expand analysis to **multiple YouTube channels**.
- Analyze **comments sentiment** to understand audience feedback.
- Use **machine learning** to predict video performance based on metadata.

## License
This project is licensed under the MIT License.

---
**Author:** Brian Nguyen  
**GitHub:** [brian-vu-nguyen](https://github.com/brian-vu-nguyen)

