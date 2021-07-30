# Data-Regeration-using-distribution
First I have tried to test the funtionality and limitations of ks test in the file "kstest_tests" and found out that number of data affects the P value output.

In "data_rec_dval" I have tried to use d value of ks test to find the distribution best suited for the feature and then recreate it.
which is then tested with random forest classifier. First tested with originall data and then trained with recreated data. to find the accuracy and the recreated dat have been plotted with original data to see the recreation

Then I have batched the data in batches of 100 and used p value.Then maximum occuring distribution is chosen to represent the feature from all the batches. the recreated data is tested with the model and then tested with refined recreated dataset in "rec_data_inbatch testing".

To increase the efficiency the data is ordered as per the priginal data in "data rec with order" and "rec_data_davl with order" using batch recreation and dvalue respectively.

The recreated data is validated by predicting the labels of recreated data by putting them in a trained model in "data validation with batch recreation" and "data_validation with max distribution". In both the cases the data is first trianed with original data and then label are predicted(there are two methods used to train the model to predict the data. the dierct mehtod and one with equalised number of labels. model can be trained using bith and then labels can be predicted usin the same). Skip label equalisation steps and directly go to prediction for the direct appraoch.
