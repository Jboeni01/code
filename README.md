# code
code for master thesis
three different codes
1) "prepare_data_CE.ipynb":\\
-downloads the raw data from the consumer expenditure survey for the necessary time periods
-generates consumption variables and captures demographic variables such as income, age etc,
-generates rebate variables
-generate mortgage variables
-merges all data and generates a csv file fs08.csv

2) "analysis.ipynb":
2.1) further refines the sample based on fs08.csv by:
-generating mean beate per household
-impute values for financial liquidity by iterative imputation
-generates treatment and control groups
-caps the sample by dropping all values with a z-score >3 for consumption variables
-saves data as fs08_cap.csv
2.2) statistical analysis:
-run random forest algorithm for different treatment and control groups
-generate function for predicted consumption responses with the two model uplift approach and run it on the data, save as pickle
-OLS regression to check accuracy of consumption responses
-combine treat1 and treat2 groups to calculate cumulative consumption responses based on predicted consumption responses, save as csv file
-generate function for partial dependency with two model uplift approach on numerical and categorial variables and run it on the data, save a csv files
-refine function for partial dependency for two model uplift approach such that the number of explanatory variables between treat and cont differ and run it on the data, save as csv files

3)"figures_tables.ipynb"
-generate figures and tables based on analysis section
