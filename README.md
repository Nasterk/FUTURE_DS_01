# Social Media Sentiment Analysis

This project analyzes social media data to extract sentiment insights and hashtag trends. It processes a dataset of social media posts, calculates sentiment scores, and summarizes hashtag usage and sentiment breakdowns.

## Project Structure

- `Dashboard/`  
  Contains dashboard images and visualizations.
- `Dataset/`  
  - `sentimentdataset.csv`: Raw dataset of social media posts.
  - `Output/`: Contains processed data and analysis results.
- `Notebook/`  
  - `analysis.ipynb`: Jupyter notebook for data processing and analysis.
- `Report/`  
  - `SocialMediaAnalyticsReport.pdf`: Final report summarizing findings.

## Dataset

The main dataset is `Dataset/sentimentdataset.csv`, which includes columns such as:
- `Timestamp`: Date and time of the post
- `Text`: Content of the post
- `Retweets`: Number of retweets
- `Likes`: Number of likes
- `Hashtags`: List of hashtags used
- `Sentiment`: Pre-labeled sentiment (if available)

## Analysis Steps

The analysis is performed in `Notebook/analysis.ipynb` and includes:

1. **Data Cleaning**
   - Removes missing values
   - Cleans and splits hashtags
2. **Sentiment Analysis**
   - Uses TextBlob to calculate sentiment polarity for each post
   - Classifies sentiment as Positive, Negative, or Neutral
3. **Hashtag Analysis**
   - Extracts and counts hashtags
   - Identifies top hashtags
   - Explodes hashtags for per-hashtag sentiment breakdown
4. **Output Generation**
   - Saves processed data and summary CSV files

## Output Files

After running the notebook, the following files are generated in `Dataset/Output/`:

- `processedData.csv`: Cleaned dataset with calculated sentiment and scores
- `topHashtags.csv`: Top 10 hashtags and their counts
- `hashtagSentimentSummary.csv`: Sentiment breakdown (percentages) for each hashtag

## How to Run

1. Install dependencies (e.g., pandas, textblob, jupyter):
   ```bash
   pip install pandas textblob jupyter
   ```
2. Open the notebook:
   ```bash
   jupyter notebook Notebook/analysis.ipynb
   ```
3. Run all cells to process the data and generate outputs.

## Results

- The notebook prints summary statistics, such as the number of processed rows and the most mentioned hashtag.
- Output CSVs can be used for further analysis or visualization.