# SupervisedML
train machine learning models to predict the “Quality of Experience” of YouTube video streaming sessions using network level measurements
Training machine learning models to predict the “Quality of Experience” (an indicator that denotes how much the user is satisfied)
of YouTube video streaming sessions using network level measurements
The dataset is built by controlled experimentation and consists of around 100k experiments of YouTube video playout . In each experiment, network measurements (such as network bandwidth, packet delay and packet loss rate) and application-level measurements such as the initial startup delay of the video are collected. Your job is to build machine learning models and evaluate their performance 

Input features for training the machine learning algorithm: All features whose name starts with “outbandQoS” and “pcapStats”, and the features of totalDuration and totalPacketCount. A brief meaning of the abbreviations used in the features is in given in the appendix.

Output labels:
 Regression: 	The output label/class is “QoE_ITU_046” for classification. “QoE_ITU_046“ is a real number ranging from 1 to 5 and corresponds to user Quality of Experience. Rows with -1 values can be ignored. 
Classification:	 The output label/class is “QoE_JT” for classification. “QoE_JT “ is a binary variable and indicates whether the video starts to play within 30 seconds (QoE_JT = 1) or times out and does not play (QoE_JT = 0)


Question 1.1 Plot the correlation matrix (correlogram) of the dataset. Only use the input features as shown on the previous page and use “QoE_ITU_046” Which features have the highest correlation with QoE_ITU_046?	

Question 1.2 Build regression models using Linear Regression and Random Forest (any other algorithm is also allowed) with default parameters to predict the QoE of YouTube video streaming using network level measurements. Use training and test split ratio of 80:20. On the test set, report the Root Mean Squared Error (RMSE) for both models. Which algorithm performs better and why?

Question 2.1 Build a classification model using Random Forest (any other algorithm is also allowed) with default parameters to predict the whether the video starts to play or times out (QoE_JT ). Use training and test split ratio of 80:20. On the test set, provide the Confusion Matrix. With what precision does the model predict the video to timeout (positive class will be 0 in this case)? You can use all the features or use a subset of the features as obtained using the approaches in Q1.
Question 2.2 Plot the ROC curve and provide the Area under the Curve (AUC) of the model.

Question 3.1: Plot the CDF (Cumulative distribution function) for the variable “join_time”. This variable gives the startup delay (in milliseconds) for every YouTube video session. What percentage of videos play with join_time of less than 10 seconds?

DL: DownLink/DownLoad 
TP: ThroughPut (bandwidth)
 UL: UpLink/UpLoad 
QoS: Quality of Service 
pXX: Xth percentile. 
For example pcapStats_stats_p20_DL_TP corresponds to 20th percentile for network download throughput _t: packet interarrival time
