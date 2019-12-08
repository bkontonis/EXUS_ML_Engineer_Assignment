# Book Recommender - Vasilis Kontonis

In this assignment I built a model for book recommendation. The datasets used is the [Book-Crossing](hhttp://www2.informatik.uni-freiburg.de/~cziegler/BX/).<br> The task was to implement at least some version of collaborative filtering that takes into account the books a user has read.

## Requirements
This project ran on Python 3.7.4

```$ pip install -r requirements.txt```

## Files:
This repository contains the following files:
 - "Book Recommender.ipynb", which is the requested Notebook that reflects my workflow (i.e the steps I took to complete the project, from data analysis to training, evaluation and model export). <br>
 - requirements.txt, where are listed all the modules required to run the Notebook.


## Results

**Data Exploration**
* Loaded the three datasets (`BX-Users.csv`, `BX-Books.csv`, `BX-Book-Ratings.csv`)
* Explore each one and familiarizing myself with the available information
            
**Define the methodology to follow**
* After exploring the data I decided to continue only with `BX-Book-Ratings.csv` data and build a FunkSVD model in order to make predictions of the ratings for each user-book combination.
* I split the data to train and test in order to be able to evaluate the model.
* I conduct two experiments, one using only the explicit ratings and one using the implicit as well. According to the evaluation scores I decide to contonue only with explicit ratings, because this model achieved better results. It is also known that implicit ratings need to be treated separately. 
* Tuned the model using GridSearchCV
* The final model has RMSE 1.66
* Created a function that returns the top 5 recommendations for a given user.
* Exported the final model `final_svd_model.sav`


