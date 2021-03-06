# cricket-world-cup2019-[fall-of-wicket-prediction-regression-pyspark-MLlib]


This is a demonstration of Spark ML Libraries capabilities for which I have tried implementing Logistic Regression Model to predict wicket fall on World Cup Semi Final
(between India and New Zealand) held in Old Trafford, Manchester, England. 

Scrapped data of Players and Matches can be retrieved from the below link, which we will use in our notebook-

https://drive.google.com/drive/folders/1IQCUKo1zBkVKM1b9NPMl2EApVb00cpXn?usp=sharing

Steps - 

1.Load the scrapped data of matches and player

2.Prepare semi finals data set [from the scrapped matches data] - -46th Match in Cricket World Cup 2019

3.Prepare Player Bowling Styles Data [from the scrapped players data]

4.Generate Data of wicket falls[FoW] pattern for Team - India in Semi Finals

5.Create wicket falls data for team India in semifinals by merging bowling style data with semifinal data

6.Preprocess data -
  - Add new columns -
      -balls_faced
      -cumruns[total runs a team score on a particular ball]
      -cumrunsbyballsfaced[derived variable calculated from cummulative runs / balls faced]- this value will decrease with more and more unplayed balls during the match
      
7.Implement logistic regression using pyspark MLlib modules to predict wicket falls


References:

https://spark.apache.org/docs/3.1.1/api/python/reference/api/pyspark.ml.feature.VectorAssembler.html

https://spark.apache.org/docs/latest/api/python/reference/api/pyspark.ml.evaluation.BinaryClassificationEvaluator.html

https://scikit-learn.org/stable/modules/generated/sklearn.metrics.confusion_matrix.html
