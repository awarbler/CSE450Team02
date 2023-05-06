# CSE450Team02
Team 2 work 


# Module 02 
# Dataset
Spend some time with your team evaluating the data. Be sure to look at data types, ranges, and meanings of each feature from the data dictionary.

Links 
- [RAW Data](https://raw.githubusercontent.com/byui-cse/cse450-course/master/data/bank.csv)
- [Data Dictionary](https://byui-cse.github.io/cse450-course/module-02/bank-dictionary.txt)

# Stakeholders 
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

# DATA DICTIONARY

Our database analyst put together this [data dictionary](https://byui-cse.github.io/cse450-course/module-02/bank-dictionary.txt) to help explain the values and sources of different columns in the [bank dataset](https://raw.githubusercontent.com/byui-cse/cse450-course/master/data/bank.csv), so be sure to review that.

# BINNING

There are multiple ways to do this, but previously we used the [map() function](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.Series.map.html).

# DECISION TREES

You can find documentation on how to use decision trees with sci-kit learn on these pages:

[User Guide Entry for Decision Trees](https://scikit-learn.org/stable/modules/tree.html)
[API Reference for DecisionTreeClassifier](https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeClassifier.html)
[Tips for Practical Use, from the User Guide](https://scikit-learn.org/stable/modules/tree.html#tips-on-practical-use)

# MODEL PERSISTENCE


You'll want to save these trained models using python's pickle module, [as shown here](https://scikit-learn.org/stable/modules/model_persistence.html).

However, rather than using pickle's default protocol version, you should use [protocol version 5]([https://byui-cse.github.io/cse450-course/module-02/project.html#:~:text=However%2C%20rather%20than%20using%20pickle%27s%20default%20protocol%20version%2C%20you%20should%20use%20protocol%20version%205%2C%20which%20was%20introduced%20in%20Python%203.8%20and%20is%20optimized%20for%20dealing%20with%20structures%20that%20contain%20numpy%20arrays%20and%20pandas%20data%20frames](https://docs.python.org/3/library/pickle.html#data-stream-format)), which was introduced in Python 3.8 and is optimized for dealing with structures that contain numpy arrays and pandas data frames.

# MODEL ENSEMBLES, BAGGING, AND BOOSTING


For details on how to use these techniques with Sci-Kit Learn, [see this page](https://scikit-learn.org/stable/modules/ensemble.html).

 We will need this [collection of Google Colab notebooks](https://byui-cse.github.io/cse450-course/module-02/hints.html) that might be useful.
