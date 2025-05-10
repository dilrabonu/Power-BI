
# ✈️ US Airlines Twitter Sentiment Analysis – Power BI Dashboard

## 📌 Project Overview

This Power BI project analyzes customer sentiment based on 14,640+ tweets directed at major US airlines. The dashboard visualizes how passengers feel (positive, neutral, or negative) using NLP-processed data, DAX measures, and interactive visuals.

The aim is to explore public perception, identify key complaints, and showcase Power BI capabilities for text-based sentiment analysis.

---

## 📂 Dataset Information

- **Source**: Kaggle – [Twitter US Airline Sentiment](https://www.kaggle.com/datasets/crowdflower/twitter-airline-sentiment)
- **Records**: 14,640 tweets
- **Columns Used**:
  - `text`: Raw tweet content
  - `clean_text`: Cleaned version for word cloud
  - `sentiment`: Label (`positive`, `neutral`, `negative`)
  - `label`: Numeric encoding (0–2)

---

## 📊 Dashboard Features

- ✅ **Tweet Count by Sentiment** (bar chart)
- ✅ **Sentiment Distribution** (pie chart with DAX %)
- ✅ **Word Cloud** of frequent words (custom visual)
- ✅ **Q&A AI Visual** for natural language queries
- ✅ **Average Tweet Length by Sentiment** (donut chart)
- ✅ **Positive Tweets Total** (card)
- ✅ Page navigation and slicers

---

## 🧮 DAX Measures Used

```dax
// Total number of tweets
Total Tweets = COUNT('us-airline'[text])

// Sentiment Percentage
Sentiment % = 
DIVIDE(
    COUNTROWS('us-airline'),
    CALCULATE(COUNTROWS('us-airline'), ALL('us-airline'[Sentiment]))
)

// Count of Positive Tweets
Positive Tweets = 
CALCULATE(
    COUNTROWS('us-airline'),
    'us-airline'[Sentiment] = "positive"
)

// Tweet Length (Column)
Tweet Length = LEN('us-airline'[text])

// Average Tweet Length (Measure)
Average Tweet Length = AVERAGE('us-airline'[Tweet Length])

// Word Count (Column)
Word Count = 
LEN(TRIM('us-airline'[text])) - LEN(SUBSTITUTE('us-airline'[text], " ", "")) + 1




![image](https://github.com/user-attachments/assets/a5da58fb-4cc2-467a-b7c1-a794d2fa96a0)

![image](https://github.com/user-attachments/assets/ea8860c6-2828-47c2-a118-11469737c6a7)

### Using By DAX

![image](https://github.com/user-attachments/assets/7be360cf-cb08-447e-9bf1-e2a8491a55b8)

