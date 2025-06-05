# 🎧 Music Recommendation System: Content-Based Filtering

## 🚀 Project Overview

This project implements a **content-based filtering music recommendation system** using Python. It analyzes both **song metadata** (titles, descriptions) and **user interaction data** (like watch durations) to recommend similar songs using textual and numerical features.

Imagine you love "Bohemian Rhapsody" by Queen. This system looks at the description and engagement data of that song and finds others with similar vibes—more than just genre matching, it captures the essence of what makes a song resonate.

---

## 🎯 Objectives

- Build a content-based recommendation engine for music.
- Use NLP to process textual features (titles + descriptions).
- Incorporate numerical features like watch durations.
- Visualize and evaluate similarities between songs.

---

## 🤔 Why Content-Based Filtering?

Unlike collaborative filtering, which needs lots of user ratings, **content-based filtering** focuses on the **features of the songs themselves**. Perfect when you have metadata but limited user data—just like a librarian recommending similar books based on genre or theme.

---

## 📁 Dataset

The dataset is a JSON file (`Music-Data.json`) with music video metadata and user interaction data.

### Key Fields:

- `loc`, `loc_song`: File paths for media storage.
- `src`: YouTube URL (e.g., `https://youtube.com/watch?v=ha3QcOXcUyY`).
- `t`: Title of the video.
- `d`: Description text.
- `act`: Interaction data with:
  - `count`: Number of interactions
  - `d`: List of watch durations (in seconds)

#### Example:  
For the video ID `ha3QcOXcUyY` (song: **Main Khiladi**)
- **Title:** Main Khiladi  
- **Description:** "Star Studios presents in association with Dharma Productions..."  
- **Interaction:** 10 views, durations like `[2.95s, 2.04s, ...]`

> 💡 **Why is watch duration important?**  
> It reflects **engagement**. Someone watching 2 seconds vs. 2 minutes has very different interest levels.

---

## 📦 Dependencies

Install these Python libraries:

```bash
pip install pandas numpy spacy gensim scikit-learn seaborn matplotlib jupyter
python -m spacy download en_core_web_sm
pip install scipy
