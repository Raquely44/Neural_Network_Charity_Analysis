# Neural_Network_Charity_Analysis

## Overview
We are using Neural Networks Machine Learning Algorithms to develop a neural network to predict if applicates for Alphabet Soup (a nonprofit foundation) will be successful or not. We have a csv containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. We hope to ensure Alphabet Soup's money is used effectively. 

### Resources
Dataset Resources/charity_data.csv
Software Jupyter Notebook
Language Python
Libraries Scikit-learn, TensorFlow, Pandas


## Results
Results: Using bulleted lists and images to support your answers, address the following questions.

Data Preprocessing
What variable(s) are considered the target(s) for your model?
The "IS_SUCCESSFULL" column is the target.

What variable(s) are considered to be the features for your model?
The rest of the dataset's columns are the features with the expection of the "EIN" and "NAME" column which were dropped.

What variable(s) are neither targets nor features, and should be removed from the input data?
I determined the "EIN" and "NAME" should be removed because they seemed to be indepentent of an applicate being successful or not.

Compiling, Training, and Evaluating the Model
How many neurons, layers, and activation functions did you select for your neural network model, and why?
- For the first iteration there were two layers used and 80 neurons were in the first layer and 30 in the second. relu and sigmoid were used as the data used was no less than 0 and we were only looking to predict if an applicant was successful.
<img scr="Resources/first_summary" with=300>

- For the trial to improve the accuracy of the model three layers were added and the number of neurons was increased as noted in the images below. I found that adding layers did not improve the accuracy, rather it stayed the same about 72%. For my last attempt I removed the third layer and increased the neurons to 200 for the first layer and 80 for the second layer. I increased the neurons for each attempt because there was a larger distribution of data points with in each feature.

<img scr="Resources/second_summary" with=300>
<img scr="Resources/second_result" width=300>
<img scr="Resources/third_summary" with=300>
<img scr="Resources/third_result" width=300>
<img scr="Resources/fourth_summary" with=300>
<img scr="Resources/fourth_result" width=300>

Were you able to achieve the target model performance?
no

What steps did you take to try and increase model performance?
I reprocess the data and adjusted the bins to accomodate for the wide range of values. I also added a new layer, which did not work. In the end, increasing the number of neurons helped the most.

## Summary
Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.
Overall this model did not achieve a 75% accuracy rating which maypoint to the need to more data that pertains to the success of an applicate or more historical data. There also could be the need for a different model, like a random forest, that can handle complex data that is not linear.

