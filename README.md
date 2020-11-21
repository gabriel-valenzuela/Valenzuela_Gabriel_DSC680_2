# Chopped Injuries Analysis

## Applied Data Science Project 

![Kickstarter Name](https://github.com/gabriel-valenzuela/gabriel-valenzuela.github.io/blob/master/images/ChoppedBanner.jpg)

### Objective

With this data set, I am proposing that it be analyzed to determine the success rate after being injured on the show. At the same time, if the ingredients have any correlation with these injuries as well as if profession has a factor of injury. The formal research questions are as follows:

What basket ingredients have a higher chance of a contestant injuring themselves while competing?

Does experience or chef title have an influence on the possibility of injuries?

If you are injured on the show, what are the chance of you winning the competition as a whole?

When it comes to this data set, it allows for an individual to sort throughout all of the basket ingredients, the notations of injuries under episode notes, and the title of the competitors under chef info to see if it has any influence on a chef being injured on accident during each round. With determining the possibility of injury, the data provides dates of the episodes to also examine if the occurrences are trending down or up as the show continues. 

### Data Source

https://www.kaggle.com/jeffreybraun/chopped-10-years-of-episode-data

### Methodology

Decision Tree Model (Preview of Model)

To see entire code for analysis, look into project folder.

```python

#train the mdodel
X_train, X_test, y_train, y_test = train_test_split(chopped_df_foodless_ip_scaled_ftrs, chopped_df_foodless_ip[response], test_size=0.30)

# Create and fir Decision Tree Model
model = DecisionTreeClassifier()
model.fit(X_train, y_train)
    
# Predicition of model
y_pred = model.predict(X_test)

# Accuracy of Model
accuracy = np.mean(cross_val_score(model, X_test, y_test, scoring='accuracy')) * 100
print("Accuracy: {}%".format(accuracy))
```

### Conclusion

Even though there is not a high rate of injuries on the show, is it a smaller chance of winning the
entire episode once you have been injured. When an injury is presented, it is addressed by the
medical team at the time which will handle it for you. However, this does not mean the clock
stops ticking for the injured chef or the other competitors causing a hurdle for those that are hurt.
It may simply be out of their hands once it happens. Therefore, from this analysis, I think it will
provide an insight on the likelihood of success if you happen to injure yourself and if your
professional cooking experience will play a role in this possible chance of still winning

