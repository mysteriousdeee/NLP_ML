# HOW I LEARNT NLP FOR MACHINE LEARNING FROM A LINKEDIN COURSE BY DEREK
### Thank you for stopping by
Welcome to my non-pythonic world

I found this helpful well explained course on LinkedIn with follow along
exercise, so i decided to flex it and practice towards my phishing research

So much fun.
___

## Descrption

### Dataset 
`SMSSpamCollection.tsv` is a tsv file that is delimited by "\t"

### Enttry point
`data_cleaning.ipynb` is the jupyter notebook file for the build and practice of NLP, find a suitable
name much later.

## Preparing the dataset

### Procedure for cleaning data
1.  Import libraries {pandas, re, string, nltk}.
2.  Read the data into dataframe.
3.  View the raw dataset to determine what next.
4.  Start organising the dataset into rows, using re.
5.  Check for missing data "understand isnull and findall"
6.  Remove, special char, tokenise data, drop stopwords
7.  Perform stemming, perform lemmatising, study the difference.

#### Change those text to some binaries
This particular task was carried out in the file `vectorisation.ipynb` as we tokenised here in
a more pythonic way

#### Procedure for vectoriation
##### Count vectorisation
Perform count vectorisation on the text by fiting and transform, import from nltk lib.
Convert the array back to dataframe to see the document fit matrix, all the tokenised words and their
count across the dataset. Here the analyser with the cleaning function is used when parsing the text 
during instatantion.

#### N_gram vectorisation
Perform N_gram vectorisation on the text by fiting and transform, import from nltk lib
Convert the array back to dataframe to see the document fit matrix, all the tokenised words and their
count across the dataset. Here no analyser with the cleaning function is used when parsing the text during instatantion

`For both processes above notice a smaller chunk of the data was used to give a proper overview of what it looks like.`

### Feature Engineering
Here the real thing kind of commence.
Create new features or tranform exisiting features to be used to train the model. What else can we extra?
i.e. length of message, percent of characters that are punctuation, or percent of text uppercase.

Power transformation: taking square root, squaring data
Transformation can be done to make the model more well behaved. i.e. if we have a very skewed data
with a very long right tail, log transformation pulls those outliers data back towards the bulk of the data
helps model draw correlation and understand the data without overfitting.

Standardisation
Transforming data to make the feature on same scale. get creative, extra much helpful features as possible.

#### Creating the Features
Some features can be extracted from the data to help the model predict better, for this particular dataset we like to look 
at the legnth of text and percentage of punctuation in the text which we was believed to have significance in the 
classfication of the text as 'spam' or 'ham'

#### Evaluate the Features
Perform log transformation to make the model better by it not chasing outliers
determine range of exponents to test. commonly its from -2 to +2
Apply each transformation to each value of the chosen feature
use some criteria to determine which of the transformations will yield the best distribution
Box-Cox power transformatioin is very useful for sskewed data, to help model make prediction in a cleaner way.
Study more on why when and how to do advance transformation on data.


#### Building Machine Learning Classifiers
##### K-Fold Cross Validation
Before actual building it's good to understand the concept of Cross validation. Here the dataset is split into k number of subsets
ie if we have 10,000 instance, and k=5, it would be broken down to 2,000 in 5 place, how the test set for prediction k-1 will be one
portion which will be 2,000 while the other 4 will be used for training, this iteratio will be repeated using each of the subset for
prediction to have a well built function model.

##### Evaluation Metrics
Accuracy =  # predicted correctly / total # of observations

Precision =  # predicted as spam that are actually spam / total # predicted as spam

Recall =     # predicted as spam that are actually spam / total # that are actually spam

### Random Forest
Utilise Ensemble Method which uses multiple models to make a stronger metamodel for better prediction.

RF: Uses ensemble method by creating multiple trees which are weaker trees that would combine to form a strong tree {of decision} 
ie out of a 100 trees, 60 classify data as 'spam' and 40 classify data as 'ham' them model will classify such data as 'spam'

#### Benefit
- Can be used for classification or regression problems, where independent variable is either categorical or continous
+ Easily handles outliers, missing value, etc
* Accepts several input (i.e. continous, ordinal, etc)
- Less likely to overfit
- Outputs feature importance

Set relevant hyperparameter and carry out k-fold cross validation

#### Cross Validation
Divide the dataset into k subsets and repeat the holdout method k times where a different subset each time is used as
holdout set (test) in each of the iteration.

#### Grid-search
Exhastively search all parameter combinations in a guven grid to determine the best model. Set different hyperparameter values.

___
### Others
$ echo "project" > /dev/null


