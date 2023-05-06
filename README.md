# CSE450Team02
Team 2 work 


Module 02 
Dataset
Spend some time with your team evaluating the data. Be sure to look at data types, ranges, and meanings of each feature from the data dictionary.

Links 
- [RAW Data](https://raw.githubusercontent.com/byui-cse/cse450-course/master/data/bank.csv)
- [Data Dictionary](https://byui-cse.github.io/cse450-course/module-02/bank-dictionary.txt)

#Stakeholders 
The core task we're interested in is identifying those customers most likely to subscribe to a term deposit.
- find any actionable patterns in our results. 
    - Should we only call single people on Saturdays?
    - Does it make sense to call students at all?
- does contacting people too frequently for these marketing campaigns have an adverse affect on the outcome?

One last thing, there are a bunch of social and economic indicators in the data.
- We may want to see separate models for times when, for example, the consumer confidence index is high compared to when it is low.

We'll definitely want to know if it's better to use a particular model during different economic situations.

once you have the models trained and tested, that you persist those trained models to a file so we can load them into our production systems.

run the list through your model and make some predictions for us?
[Data](https://raw.githubusercontent.com/byui-cse/cse450-course/master/data/bank_holdout_test.csv)

Then, please submit a csv file that has a single column, with the header "predictions" and a prediction (one per row) for each individual in this file. If we should contact the individual, predict a 1.
If we shouldn't contact the individual, predict a 0 for that row. There should be 4,119 predictions in the csv file when completed.

DATA DICTIONARY

Our database analyst put together this data dictionary to help explain the values and sources of different columns in the bank dataset, so be sure to review that.

TARGET VARIABLE

One oddity here is that our target feature is simply labled y, but it's a boolean indicating "y" or "n", did the client subscribe to a term deposit.

BINNING

Just as you did with the Titanic dataset when you reduced the number of titles, you may find it useful to "bin" categorical features into discrete groups in order to address some of the questions above. There are multiple ways to do this, but previously we used the map() function.

DECISION TREES

You can find documentation on how to use decision trees with sci-kit learn on these pages:

User Guide Entry for Decision Trees
API Reference for DecisionTreeClassifier
Tips for Practical Use, from the User Guide
MODEL PERSISTENCE

When you train a model, a large amount of information is stored in memory. That model can then be used to make predictions for new instances at a later time.

You'll want to save these trained models using python's pickle module, as shown here.

However, rather than using pickle's default protocol version, you should use protocol version 5, which was introduced in Python 3.8 and is optimized for dealing with structures that contain numpy arrays and pandas data frames.

MODEL ENSEMBLES, BAGGING, AND BOOSTING

Often, we can get better results by using a set of models, each using a slightly different set of training data, or other parameters. These are called "Model Ensembles" and it's very common to use an ensemble of decision trees (often called a "Random Forest") rather than a single tree.

Two popular techniques used in the creation of ensembles are "boosting" and "bagging". You can read more about these topics on pages 163 - 167 of your textbook.

For details on how to use these techniques with Sci-Kit Learn, see this page.

AVOIDING OVERFITTING THROUGH PRUNING

It is very easy to overfit a decision tree. The text discusses strategies to avoid this problem in section 4.4.4 (pages 158 - 163).

In SciKit-Learn, you can use parameters such as max_depth and min_samples_leaf to control tree complexity and overfitting.

Alternatively, you can use something more elaborate, such as cost complexity pruning.


JOHNNY, THE DATA SCIENCE INTERN, DROPS BY YOUR HOTEL ROOM AROUND MIDNIGHT:
Okay, just one last thing, if you need any more help at all, I put together this collection of Google Colab notebooks that might be useful.
