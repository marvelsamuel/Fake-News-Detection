# Fake-News-Detection
This repository contains the code and resources for a Fake News Classification project using Natural Language Processing (NLP) and Machine Learning models. The goal of this project is to develop a system that can distinguish between real and fake news articles automatically.

### 1. Data Preprocessing

> The data is balanced

-  Dropped the first column (ID)
-  Deleted all rows that includes more than 3 columns. 
-  Deleted rows that doesn’t have words (real or fake) in the third column.
-  Changed the value of (real – fake) to (1 – 0) respectively
-  Used regular expressions (re.sub) to remove any non-alphabetic characters from the text and replaces   them with a space.
-  Converts the text to lowercase.
-  Splits the text into a list of individual words.
-  Iterates over each word in the list and performs lemmatization.


### 2. Feature Extraction

- TF-IDF vectorizer is used where:

  - Maximum features are 8000

  - Both unigrams and bigrams are included

- The resulting TF-IDF matrix is converted to a dense matrix format.
- The transformed matrix is then converted to a panda DataFrame.



### 3. Models 

> Data is divided to 75% Training and 25% Testing

1. SVM (Kernel is linear)

   Accuracy: 0.9404686510449651

   Precision: 0.9487870619946092

   Recall: 0.9263157894736842 

   F1 Score: 0.9374167776298269


2. Passive Aggressive Classifier 

   Accuracy: 0.9373020899303357

   Precision: 0.9412550066755674 

   Recall: 0.9276315789473685 

   F1 Score: 0.9343936381709742


   

3. SVM ( kernel is Sigmoid , C=2)

   Accuracy: 0.9303356554781508

   Precision: 0.9380053908355795 

   Recall: 0.9157894736842105 

   F1 Score: 0.9267643142476697

   

   4. Gradient Boosting Classifier

      Accuracy: 0.9252691576947435

      Precision: 0.9409340659340659 

      Recall: 0.9013157894736842 

      F1 Score: 0.9206989247311828

     

   5. Random Forest Classifier(n_estimators=100, random_state=42)

      Accuracy: 0.9062697910069665

      Precision: 0.9047619047619048 

      Recall: 0.9 

      F1 Score: 0.9023746701846965

     

   6. Multinomial Naïve Bayes

      Accuracy: 0.8822039265357822

      Precision: 0.8816489361702128 

      Recall: 0.8723684210526316 

      F1 Score: 0.876984126984127

      

   7. Bernoulli Naïve Bayes

      Accuracy: 0.8074730842305257

      Precision: 0.8392857142857143 

      Recall: 0.7421052631578947 

      F1 Score: 0.7877094972067039


