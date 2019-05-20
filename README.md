keyword-extraction
==================

Kaggle [Keyword Extraction](https://www.kaggle.com/c/facebook-recruiting-iii-keyword-extraction) competition by Facebook. Implemented in Python.

Features: known kws, multi-word kws, unknown kws in title<br />
Scoring: Naive Bayes probability, tf-idf<br />
Heuristics: #Tags >= 1, 'tag-dash-kws' == 'tag dash kws', c#<br />

---

### Instructions

0. Clone repository
0. Create virtual environment `virtualenv env`
0. Install required libraries `pip install -r requirements.txt`
0. Download NLTK resources using `load_nltk.py`
0. Download `Train.zip` from the [Kaggle site](https://www.kaggle.com/c/facebook-recruiting-iii-keyword-extraction/data) to local folder `data`
0. Split training data into new train and test files using `split_data.py` - creates train and test csvs (94 sec)
0. Train models using `train.py` - creates json models in `classifiers/` (161 sec)
0. Generate predictions using `predict.py` - creates prediction csv `data/Pred.csv`
0. Evaluate predictions using `evaluate.py` - outputs mean precision, recall, and F1 score

#### Notes

* Input data files (Train, Test, Pred) are in a local folder `data`
* Test file generated from random sample of Train file due to inability to score Test file on Kaggle
* Mean F1 scoring based on Kaggle's [wiki](https://www.kaggle.com/wiki/MeanFScore)
