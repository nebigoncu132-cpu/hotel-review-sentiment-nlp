# Hotel Review Sentiment Classification

NLP group project — *Basic Lab: Introduction to AI*

**Group members:** Leonardo Volpe, Zhan Shakarim, Nebi Göncü

Binary sentiment classification (positive / negative) of hotel reviews using
**Bag-of-Words + Logistic Regression**. The project also demonstrates, with a
concrete example, why a logistic model with Bow is blind to order.

## Files

| File | Description |
|---|---|
| `hotel_reviews_sentiment_analysis.ipynb` | All code: runfrom top to bottom. 
| `tripadvisor_hotel_reviews.csv` | TripAdvisor dataset (download separately)) . 
| `Hotel_Reviews_NLP_Report.docx` | Writtenn report. 
| `Hotel_Reviews_NLP_Slides.pdf` | Presentation slide. 

## Dataset

**TripAdvisor Hotel Reviews** 
Download the CSV and save it as `tripadvisor_hotel_reviews.csv` in the same folder as the notebook.

## How to run it?

1. **First install requirements** :

   ```bash
   pip install pandas numpy scikit-learn matplotlib
   ```

2. **Place the dataset CSV** to the same direcyotry with the ipynb file.\


3. **Run the notebook** top to bottom:

   ```bash
   jupyter notebook hotel_reviews_sentiment_analysis.ipynb
   ```

## Results

Validation (n = 2,746)  94.90% accuracy   
Test (n = 2,747)  95.1% accuracy


## Notebook structure

1. **Setup** — first import libraries.
2. **Dataset** — load TripAdvisor reviews of random people.
3. **Binary label** —  4–5 stars are  Positive, 1–2 stars are  Negative and  drop the neutral (3 stars).
4. **Split** — 70 / 15 / 15 division to  train / val / test data sets
5. **Preprocessing** — lowercase, remove non-letters and collapsee whitespace.
6. **Tokenisation and vocabulary** — split into tokens, build vocab from training data, encode, pad to 266 tokens.
7. **BoW and Logistic Regression** — CountVectorizer (top 3000 features) and use  LogisticRegression; val and test accuracy; confusion matrix.
8. **Top words** — most influential words for each sentiment class.
9. **Custom predictions** — five hand-written sentences tested with confidence scores.
10. **Word-order demo** — proof that BoW gives identical predictions for reordered sentences.
11. **Summary** — strengths and limitations of the BoW approach and so on.

All randomness is seeded (`random_state = 42`) so results are can be tried by you as well.
