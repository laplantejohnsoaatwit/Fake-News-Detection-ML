# Fake-News-Detection-ML

## Introduction
The objective of this project was to practice using all of the skills and tools that we have learned over the past semester and implement them into a functional program. I decided that a great way to accomplish this would be to create a fake news detection program using machine learning. This project has been done many times, but for good reason. It showcases all that we have learned so far in our class, as well as using some libraries and techniques that were not fully covered in our discussions. This project provided a great challenge while also helping me to compile my datascience skills together and create something useful.

I decided to do a fake news detection program while reading an article on what makes a good data science project. This project is great for machine learning, as it is boolean based and has over 40,000 articles to work with.

The main question I had after choosing this project is which subject of news would have the most fake articles. I had a large hunch that it would be political, but I was curious to see the results.

## Selection of Data
For the data, I used a dataset from Kaggle (https://www.kaggle.com/clmentbisaillon/fake-and-real-news-dataset). It contains two CSV files, Fake and True. These datasets are labeled with a title (title), the entire text in the article (text), the date (date), and the source/subject of the article (subject). Each dataset also contained over 20,000 articles each. 

Heres an example of the fake news dataset:
![png](fake_snippit.PNG)

Some of these columns (date, title) were dropped because they were not used in any part of the program.

There had to be a lot of cleaning up of the data for this specific project because the articles all contain phrases that would mess up the accuracy of our program. To do this, I implemented a method that cycles through the article and removes unwanted characters.
![png](unwanted_char.PNG)

I also merged the two dataframes into one, and added another column to that merged dataframe called 'Indicator' which hold a 1 or 0 that represent true and false respectively. 

## Methods
Tools used:
  - NumPy, Scikit-learn, Pandas, re, nltk, matplotlib
  - Jupyter Notebook as IDE
Scikit:
  - Logistic Regression for ML
  - Accuracy score, classification report, TfidVectorizer
  - Wordcloud for visualization
## Results
The Logistic Regression worked great for the fake news detection program, and achieved a 99% accuracy score.

![PNG](acc.PNG)

Our LR model worked just as expected, as LR models work great with booleans.
 
![png](visual1.PNG)
![png](viz2.PNG)

After the visualizations , we arrive at the user input portion.

![png](sedondfake.PNG)
![png](thisfake.PNG)

## Discussion
While completing this project, the skills I learned earlier in the semester were placed firmly back into my memory, and the topics that were fresh in my mind before starting this project are now even more refined. The choice to go with Logistic Regression was a good choice, as it achieved a 99% accuracy score every time. The average score that I saw on the original Kaggle post (https://www.kaggle.com/clmentbisaillon/fake-and-real-news-dataset) were from 95-99%, so that is great! 

The user input section is very simple, but it works for most political articles. In the future, I would love to implement a way for a user to type in the web address of an article instead of requiring them to copy and paste the entire string. Nevertheless, the user input program works great for how simple it is!

My question of which subject of news would have the highest percent of fake news was answered and I found the results to be very interesting. Not only was political news the most fake, but it was
miles ahead of any others. Granted, there were not many subjects to pick from, but it is still interesting to see the visualization of it. It brings up the question; what is happening to our media in our society? Why is there so much fake political news that this program is actually necessary? I found this and the rest of the visualizations to be very thought-provoking. 

## Summary
This project uses a supervised Logistic Regression model that predicts whether or not an article is true or fake. After running countless trials, the program achieved a 99% accuracy score and worked extremely well.

The program contains a way to input your own articles to test, as well as various visualizations that showcase information I found to be relevant and interesting. There are many things that I would love to add to this project in the future. Fake news seems to be an ongoing problem and programs like these are a great starting place to reduce the growth of fake news.

