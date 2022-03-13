# Jigsaw-Rate-Severity-of-Toxic-Comments
Rate the toxicity of Wikipedia Talk page comments.

The Purpose:

  -> 4.55 billion social media users worldwide

  -> Equating to 57.6% of total global population

  -> The social media platforms are not highly moderated

  -> Post and share fake news, misinformation, and explicit content

  -> Potential to create chaos and harm the society


About dataset:

  -> 159,571 Wikipedia comments 

  -> The expert human raters have scored the comments

  -> There are 6 predefined classes
     Toxic, Severe_toxic, Obscene, Threat, Insult, identity_hate

  -> The training set, the test set

Data Preprocessing & Data Cleaning:

  -> Removed words and characters that has not much prediction power aka Stop words

  -> Cleaned noise - removed punctuation, special characters, numbers

  -> Removed the user  handles and URLS

  -> Normalize the text data - reducing terms like loves, loving, and lovable to their base word, i.e., ‘love’. 

  -> Tokenizing the text - Easy for feature extraction

Feature Extraction using TF-IDF:

  -> Word with the highest frequency may have low prediction power

  -> TF-IDF evaluates how relevant a word is to a document in a collection of documents

  -> Calculated by multiplying two different metrics:
     Matrix 1- The term frequency of a word in a document
     Matrix 2 - How common or rare a word is in the entire document set.  Log (The total number of documents / the number of documents that contain a word)

  -> If the word is very common and appears in many documents, this number will approach 0. Otherwise, it will approach 1

sklearn Ridge Mode:

  -> Linear least squares with l2 regularization.

  -> Minimizes the objective function:
     ||y - Xw||^2_2 + alpha * ||w||^2_2

  -> Solves a regression model where the loss function is the linear least squares function and regularization is given by the l2-norm

  -> This estimator has built-in support for multi-variate regression

