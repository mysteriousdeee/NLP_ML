# HOW I LEARNT NLP FOR MACHINE LEARNING FROM A LINKEDIN COURSE BY DEREK

I found this help well explained course on LinkedIn with follow along
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

#### Creating the features
Some features can be extracted from the data to help the model predict better, for this particular dataset we like to look 
at the legnth of text and percentage of punctuation in the text which we was believed to have significance in the 
classfication of the text as 'spam' or 'ham'

#### Evaluate the Features


___
### Others
" " > /dev/null

### Thank you
welcome to my non-pythonic world
