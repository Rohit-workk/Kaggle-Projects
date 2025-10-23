# 🎌 Anime Recommendation System — EDA and Model Development  

This project performs **Exploratory Data Analysis (EDA)** and builds a **Recommendation System** using the [Anime Recommendation Dataset](https://www.kaggle.com/datasets/ylmzasel/anime-recommendation-dataset).  
The notebook **`anime-recommendation-and-eda-from-scratch.ipynb`** demonstrates how to analyze anime ratings, visualize audience behavior, and create a personalized recommendation model from scratch.

---

## 🔍 Exploratory Data Analysis (EDA)

The analysis begins by exploring patterns within the anime dataset, which contains thousands of anime titles along with their genres, ratings, members, and user preferences.

### Key Steps and Insights:

- **Data Cleaning and Preparation:**
  - Removed missing or duplicate values in anime titles, genres, and ratings.
  - Standardized genre information for better grouping and keyword analysis.

- **General Statistics:**
  - Counted total unique anime titles, number of users, and rating distribution.
  - Analyzed rating frequency to understand user engagement and dataset density.

- **Visualization Insights:**
  - **Top Rated Anime:** Bar charts displaying the most highly rated anime based on average scores.
  - **Most Popular Anime:** Count plots showing anime with the largest member base.
  - **Genre Analysis:** Word clouds and bar plots highlighting the most frequent genres (e.g., Action, Comedy, Drama, Fantasy).
  - **Score Distribution:** Histograms showing how user ratings are distributed, revealing user bias toward high or mid-level ratings.
  - **Correlation Maps:** Explored relationships between rating counts, average score, and member engagement.

**Summary:**  
The EDA revealed that popularity and quality don’t always overlap — some anime receive high member counts but moderate ratings, while niche genres achieve strong user loyalty and high scores.  

---

## 🤖 Building the Recommendation System

The notebook then constructs an **Anime Recommendation Engine** to suggest shows similar to a user’s preferences.

### Methodology:
1. **Data Preparation:**
   - Created a user–anime matrix based on ratings.
   - Normalized the data to manage rating scale differences.

2. **Similarity Calculation:**
   - Implemented **cosine similarity** to measure similarity between anime titles.
   - Built a similarity matrix to find the closest matches to any given anime.

3. **Recommendation Logic:**
   - For a selected anime, retrieved the top 10 most similar titles based on similarity scores.
   - Combined similarity metrics with popularity (member count) to refine recommendations.

4. **Example Output:**
   - Input: *"Naruto"*  
     → Recommendations: *Bleach, One Piece, Fairy Tail, Hunter x Hunter, Dragon Ball Z*  
   - Input: *"Attack on Titan"*  
     → Recommendations: *Fullmetal Alchemist: Brotherhood, Code Geass, Death Note, Parasyte, Tokyo Ghoul*

### Evaluation:
- Verified recommendation quality through logical consistency and popularity overlap.
- Compared content-based and collaborative approaches for future hybridization.

---

## 📊 Key Insights

- Action and adventure genres dominate user interest, but romance and slice-of-life genres show strong niche engagement.
- Similarity-based recommendations effectively group titles with matching tone, themes, and viewer base.
- The content-based filtering approach ensures that even lesser-known anime can be recommended if their metadata closely matches user favorites.
- Visualization confirmed how user preferences cluster by genre and style.

---

## 🚀 Future Work — Web App Integration

The next step is to extend this system into a **web-based anime recommendation platform**, inspired by the workflow used in the IMDb sentiment analysis web app.

### Planned Features:
- **Search & Recommend Interface:**  
  A Flask or Streamlit web app where users can search for an anime title and get instant recommendations.
- **User Sentiment Integration:**  
  By combining with IMDb or MyAnimeList user reviews, integrate NLP-based sentiment analysis to personalize results.
- **Hybrid Recommendation:**  
  Merge **content-based filtering** (using anime metadata) with **collaborative filtering** (based on user similarities).
- **Interactive Dashboard:**  
  Real-time analytics dashboard to explore anime trends, ratings, and genre heatmaps.

This approach would connect **data-driven EDA**, **recommendation modeling**, and **NLP-based sentiment scoring** into a unified recommendation engine for anime enthusiasts.

---

## 📁 Dataset Information

**Source:** [Anime Recommendation Dataset](https://www.kaggle.com/datasets/ylmzasel/anime-recommendation-dataset)  
**Description:** Contains user ratings and metadata for thousands of anime titles, including genres, popularity, and member statistics.  
**Usage in this project:** Used for EDA, correlation analysis, and building similarity-based recommendation models.

---

## 🧠 Tools & Libraries

- **Python** for data analysis and modeling  
- **Pandas**, **NumPy** for data manipulation  
- **Matplotlib**, **Seaborn**, **Plotly** for visualization  
- **Scikit-learn** for cosine similarity and model development  

---

## 🤝 Credits

- **Dataset by:** [Yilmaz Asel on Kaggle](https://www.kaggle.com/ylmzasel)  
- **Developed by:** Rohit  
- **Inspired by:** prior IMDb Sentiment Analysis web app project  

---

## 📜 License

This project is intended for **educational and learning purposes**.  
You are free to use and adapt the notebook with appropriate credit.
