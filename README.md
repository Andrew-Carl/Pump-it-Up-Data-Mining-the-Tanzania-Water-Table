# Pump it Up, Data Mining the Tanzania Water Table

![pumping](https://user-images.githubusercontent.com/35437820/38469963-9c9f9da4-3b2a-11e8-8e20-78438207577d.jpg)

** Photo from(https://www.flickr.com/photos/christophercjensen/3559607145)

# Background:

Currently, the people of Tanzania have poor access to clean drinking water throughout the entire country. Approximately 47% of all Tanzanian citizens do not have access to clean drinking water. Over $1.4 billion dollars in foreign aid has been giving to Tanzania in an attempt to help fix the freshwater crisis. However, the Tanzanian government is failing to fix this problem. A good proportion of the water pumps are completely non-functioning or barely functional and also in need of repair. Many people are left to drink dirty, pathogen filled water, or walk miles on end to the closest functional ground water pump. 

# Task/Goal

- Use machine learning models to predict the functionality of all ground water pumps found throughout the country of Tanzania.
- If models are accurate, this could help save the Tanzanian government a lot of time and money.
- Accurate models can help to cut the cost on needing workers drive out to every water pump to inspect them.
- The government can use this study to know exactly which pumps are working, need repair and which ones aren’t working at all.

# How the data was acquired:

This project was for a competition on datadriven.org. The website describes itself as: 

"DrivenData works on projects at the intersection of data science and social impact, in areas like international development, health, education, research and conservation, and public services."

Companies, non-profits and governments of high paid prizes in order to have data scientist compete in order to figure out real world problems.The data for this project was acquired from the Tanzania Ministry of Water and the Taarifa Platform. The Taarifa Platform is an open source API designed to use citizen feedback on local problems. The competition and the data can be found at the link below:

https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/

# How the data was transformed and cleaned:

I used PandasProfiling to explore all of the columns in the data. The data had a few columns with a large amount of missing 
values. I chose to immediately drop those columns, due to the high volume of missing values. Imputing data or filling 
missing values would've altered the data too much. It was better to just drop them. Looking further into the data, there was 
also a decent amount of columns that were very similiar to one another. I examined these columns using value counts. If the 
columns were too similar, I chose to keep whichever one I thought was better and drop the other. Some columns were completely identical. I also grouped the contruction years by decade since there were unique values for every year from 1960-2013. This would help later on when I needed to make  dummy variables for my classification models. Luckily from there, the data was pretty clean and I was comfotable to start running some models. 

# Outcome Variable:

My outcome variable is the status and functionality of all of the ground water pumps found in Tanzania. My goal is to predict whether the thousands of water pumps in Tanzania are functional, need repairs or are completely non-functional. If my models are accurate, this could help save the Tanzanian government a lot of time and money. 

# Models:

So far I have run five models on the data. I have run a K-Nearest Neighbors model, a Logistic Regression, a Random Forest with balanced classes, a Random Forest with a grid-search, and a Gradient Boosting Classifier. My score so far have been:

- KNN = 0.662
- Logistic Regression = 0.736
- Random Forest with Balanced Classes = 0.786  
- Random Forest with Gridsearch = 0.872  
- Gradient Boosting Classifier = 0.809

I used the Gradient Boosting model and the Random Forest with grid-search to make my predictions since they had the best scores. Using these models I created two confusion matrices to see how my predictions came out. Below are the two confusion matrices:

Confusion Matrix using Gradient Boosting Classifier:

![screen shot 2018-04-06 at 8 32 21 am](https://user-images.githubusercontent.com/35437820/38469726-73328790-3b27-11e8-99a6-bc3344e59a00.png)
![screen shot 2018-04-06 at 8 33 50 am](https://user-images.githubusercontent.com/35437820/38469868-6c016796-3b29-11e8-9c41-3e66851dc129.png)

Confusion Matrix using Random Forest with Gridsearch:

![screen shot 2018-05-31 at 9 24 46 pm](https://user-images.githubusercontent.com/35437820/40816138-2cf6a75e-6519-11e8-9bb1-16aab189b190.png)
![screen shot 2018-05-31 at 9 24 57 pm](https://user-images.githubusercontent.com/35437820/40816197-85ff6160-6519-11e8-85ad-27fde64fd1ba.png)

# Predictions Map

![screen shot 2018-12-13 at 11 09 40 am](https://user-images.githubusercontent.com/35437820/49951347-af6e7980-fec7-11e8-9882-2fcb4e818d6a.png)

I created a blog post for this project on my personal website. Please visit the link below for a better look at the project:
http://www.andrewcarl.nyc/tanzania.html

