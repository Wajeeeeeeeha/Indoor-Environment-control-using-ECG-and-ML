# Modelling The Combined Effect of Indoor 
Environmental Condition on Neurobehavioral Trends of 
Individuals Through Electrocardiogram

#Objectives
Mainly there are three objectives of this research study. Firstly, to determine the correlation between noise, light and 
temperature and their combine effect on human using cognitive task performance as well as with ECG. Secondly, to 
investigate correlation of combined effect of noise, light, temperature depending on human age, gender and profession. 
Thirdly, to implement various Machine Learning algorithms such as K-Nearest Neighbors (KNN), Support Vector 
Machine (SVM), Logistic Regression (LR) to predict the combined effect of IEQ on human

# Introduction
The current study is aimed at evaluating the combined effects of indoor noise, light and temperature on human
neurophysiological responses. This study included 34 individuals who were exposed to varying temperatures (16 
degrees Celsius, 22 degrees Celsius, and 31 degrees Celsius), light (150 lumens per meter square, 250 lumens per 
meter square, and 500 lumens per meter square), and noise levels (20 decibels, 50 decibels, and 90 decibels) in 27 
sessions in a simulated indoor setting. 67% accuracy was achieved for KNN model. Accuracy can be increased with 
increasing amount of data of participants. Furthermore, the effects of temperature on heart rate were more substantial 
than the effects of noise. Overall, noise for longer duration has a stronger negative impact on working memory of 
male, whereas temperature has a more severe influence on neurophysiological response of female. On other hand, 
male performed well in high temperature than female. To the best of our knowledge, this is the first study to examine 
the relationship between ECG and IEQ. The study culminated with directions for further studies.

# Data pre-processing
This is very interesting step of our methodology. As we captured ECG in the form of images contain 12 lead 
information. Along with ECG we gathered information through questionnaire which contain in words and sentences. 
We used machine learning to convert ECG paper records into a 1- D signal. All personal information was removed 
from input image of our ECG data. Next step was to divide input image into 13 leads for additional information. 
Further processing applied on each individual leads (1-13) by eliminating gridlines, changing to grayscale, applying 
Gaussian filtering, and performed thresh holding to convert to binary image. Using the contour approach, the modified 
image was traced to extract only the signals and the values are scaled using the Min-Max Scalar. 
The normalized output is stored as a 2D signal in Comma Separated Value (CSV) format. The X-axis refers to the 
high and low points, whereas the y axis corresponds to the curve/shape. We concentrated on the low/high points in 
our study, the X-axis will be stored separately as a normalized scaled 1D signal in a CSV file. In questionnaire we 
have numeric data which contain memory score of each participant. Professional information was replaced with 0, 1 
and 2 for admin staff, teachers and students respectively. For gender we give 1 value for female and 0 for male. Finally, 
we add these values along with noise, temperature and light values for respective participants in our csv file.

# Data 
See the copy of data detail.csv file. Its just a sample data. Orignal data is not shared due to privacy contract with patients. 

# Run code
# step 1
Run final-ECg-preprocessing file to convert ECG paper records into a 1- D signal. All personal information was removed 
from input image of our ECG data. Next step was to divide input image into 13 leads for additional information. 
Further processing applied on each individual leads (1-13) by eliminating gridlines, changing to grayscale, applying 
Gaussian filtering, and performed thresh holding to convert to binary image. Using the contour approach, the modified 
image was traced to extract only the signals and the values are scaled using the Min-Max Scalar. 
The normalized output is stored as a 2D signal in Comma Separated Value (CSV) format.

# step 2
Run ML on ECG.ipynb file to execute to implement various Machine Learning algorithms such as K-Nearest Neighbors (KNN), Support Vector 
Machine (SVM), Logistic Regression (LR) to predict the combined effect of IEQ on human.

