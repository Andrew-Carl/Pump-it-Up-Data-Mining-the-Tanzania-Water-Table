# Pump it Up, Data Mining the Tanzania Water Table

note: This project is technically finished, but I am trying to optimize my models and make the best predictions possible. 

![pumping](https://user-images.githubusercontent.com/35437820/38469963-9c9f9da4-3b2a-11e8-8e20-78438207577d.jpg)

** Photo from(https://www.flickr.com/photos/christophercjensen/3559607145)

# Background:

Currently Tanzania has a poor system for clean water access throughout their country. Approximately 47% of all Tanzanian citizens do not have access to clean drinking water. Over $1.4 billion dollars in foreign aid has been giving to Tanzania in an attempt to help fix the freshwater crisis. However, the Tanzanian government is failing to fix this problem. Many people are left to drink dirty, pathogen filled water, or walk miles on end to the closest functional ground water pump. 

# How the data was acquired:

Data was aquired from the Tanzania Ministry of Water and the Taarifa Platform. The Taarifa Plateform is an open source API 
designed to use citizen feedback on local problems. 

# How the data was transformed and cleaned:

I used PandasProfiling to explore all of the columns in the data. The data had a few columns with a large amount of missing 
values. I chose to immediately drop those columns, due to the high volume of missing values. Imputing data or filling 
missing values would've altered the data too much. It was better to just drop them. Looking further into the data, there was 
also a decent amount of columns that were very similiar to one another. I examined these columns using value counts. If the 
columns were too similar, I chose to keep whichever one I thought was better and drop the other. Some columns were completely identical. I also grouped the contruction years by decade since there were unique values for every year from 1960-2013. This would help later on when I needed to make  dummy variables for my classification models. Luckily from there, the data was pretty clean and I was comfotable to start running some models. 

# Outcome Variable:

My outcome variable is the status and functionallity of all of the ground water pumps found in Tanzania. My goal is to predict 
whether the thousands of water pumps in Tanzania are functional, need repairs or are completely non-functional. If my 
models are accurate, this could help save the Tanzanian government a lot of time and money.

# Models:

So far I have run five models on the data. I have run a K-Nearest Neighbors model, a Logistic Regression, a Random Forest with balanced classes, a Random Forest with a gridsearch, and a Gradient Boosting Classifier. My scores so far have been:

- KNN = 0.662
- Logistic Regression = 0.736
- Random Forest with Balanced Classes = 0.786  
- Random Forest with Gridsearch = 0.807  
- Gradient Boosting Classifier = 0.809

Confusion Matrix:

![screen shot 2018-04-06 at 8 32 21 am](https://user-images.githubusercontent.com/35437820/38469726-73328790-3b27-11e8-99a6-bc3344e59a00.png)
![screen shot 2018-04-06 at 8 33 50 am](https://user-images.githubusercontent.com/35437820/38469868-6c016796-3b29-11e8-9c41-3e66851dc129.png)


As noted above I am still trying to optimize these models and make these numbers more accurate. I am also going to run a logisitic regression and a gradient boosting classifier. Hopefully these will create better predictions. 

I also created a short presentation of my progress so far. A longer and more technical presentation will be posted in the near future.  
https://docs.google.com/presentation/d/11blM6ZlFcipx6VkIs_21kOYRaZd8ofzsYdOS5HxPe3s/edit?usp=sharing

