# Movie Reviews Sentiment Analysis

## Dataset
The used dataset is the [Sentiment polarity datasets v2.0](http://www.cs.cornell.edu/people/pabo/movie-review-data/). The dataset contains 1000 positive and 1000 negative processed reviews that is stored in the `review_polarity` folder.

- Inside the `review_polarity` folder, `txt_sentoken` contains 2000 processed down-cased text files, seperated into to category sub-folder, namely `neg` (i.e. negative) and `pos` (i.e. positive). Each sub-folder contains 1000 review text files in that category. 

- `poldata.README.2.0` stores all the meta information of this dataset.


## Models
Reviews were preprocessed using Bag-of-Words model and were represented in 3 vectorization methods: **Count, Binary** and **TF-IDF**.
Logistic Regression was used to train the models. The models were train in 3 different approaches, each with a distinct set of features presentation. 
The models were 10-fold validated with **accuracy score** to see which approach has the best performance and robustness.

<p align="center">
  <img src="https://github.com/tringuyenbao/Movie-Reviews-Sentiment-Analysis/blob/main/images/10-folds-models-accuracy.png?raw=true" alt="10-folds-models-accuracy"/>
</p>
=> Logistic Regression with binary features had the highest score overall.

#### Logistic Regression with binary features detailed report
<p align="center">
  <img src="https://github.com/tringuyenbao/Movie-Reviews-Sentiment-Analysis/blob/main/images/logistic-regression-binary-vectors-report.png?raw=true" alt="logistic-regression-binary-vectors-report"/>
</p>

#### Words importance to each sentiment]

<p align="center">
  <img src="https://github.com/tringuyenbao/Movie-Reviews-Sentiment-Analysis/blob/main/images/words-importance-for-each-sentiment.png?raw=true" alt="words-importance-for-each-sentiment"/>
</p>

- Reviews that had these words `bad, worst, nothing, plot, awful, waste, supposed, unfortunately, boring, mess` were most likely to be **negative**.

- Reviews that had these words `sometimes, memorable, perfectly, one_best, performance, others, excellent, town, overall, hilarious` were most likely to be **positive**.

These words semantic do reflect the relative emotion.
