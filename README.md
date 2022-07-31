# Charity Analysis

## Overview of the analysis
Charity Analysis program uses Deep Learning Models to analyze over 34,000 organizations that have received funding from business team will be successful. We use dataset features and target to help foundation predict the company's investment. Our goal is to optimize the Neural Network Deep Learning Model to achieve a target predictive accuracy more than 75%. 

## Results
1st Attempt has improved **4.47%** for predict accuracy, 2nd and 3rd attempt only improved total **0.3%**, and final attempt improved performance by **0.21%**.

### Data Preprocessing
- Target: 'IS_SUCCESSFUL' that predict whether applicants will be successful if funded by Alphabet Soup Business.
- Features: 
   - 'NAME' that will be binned, considered as not feature.
   - 'APPLICATION_TYPE' that will be binned
   - 'AFFILIATION'
   - 'CLASSIFICATION'that will be binned
   - 'USE_CASE'
   - 'ORGANIZATION' that will be considered as not feature.
   - 'INCOME_AMT'
   - 'ASK_AMT' that will be considered to bin.
- Neither Targets nor Features: 
   - 'EIN'
   - 'STATUS'
   - 'SPECIAL_CONSIDERATIONS' 
   
  (**Dataset has 2 unique values in each columns will be removed for data analysis**)

### Compiling, Training, and Evaluating the Model
#### First Attempt: Accuracy *76.91%* 
In order to achieve a target predictive accuracy that over 75%, we adjust the input data to ensure that there are no variables or outliers that might confuse in the model.
- Drop few more columns such as 'ORGANIZATION', 'STATUS', 'SPECIAL_CONSIDEATIONS'.
   - Create 2 Bins for feature ASK_AMT. 
   - Add additional feature and make 122bins.
   - Decrease the number of values for CLASSIFICATION Bins from 6 to 4.
   - Decrease the number of values for APPLICATION_TYPE Bins from 9 to 8
- Add more hidden layers & Using different activation functions
   - Add additional layers by using sigmoid activation, which improve the performance of accuracy. And sigmid activation is better to identified by a characteristics. Through this process, it will help the model with classification.
   - Total params from 5,981 increased to 56,601


      See attachment for more details:
<p align=center>
  <img src='Resources/images/1st_att_5.PNG' width=500 height=400 >

   </p>
   
- Evauation for 1st attempt: 
We plot the history accuracy data to visualize the result. Accuracy is 76.91%.
<p align=center>
   <img src='Resources/images/Attemp_1.PNG'  width=450 height=300 >
</p>

#### Second Attempt: achieved the target model accuracy. Accuracy *77.13%*
- Adjusting the input data
   - Increase input features
   - Unbinned features ASK_AMOUNT
- Adding more neurons to a hidden layer.
   - layer 1 increased 100 by using relu activation
   - layer 2 increased 100 by using sigmoid activation
   - layer 3 increased 50 by using relu activation that helps the model toassess input data differently and lower complexity features.
   - Total params to 128,401

      See attachment for more details:
      
<p align=center>
   
  <img src='Resources/images/2nd_att.PNG' width=500 height=400 >
 
</p>
  
- Evauation for 2st attempt: 
We plot the history accuracy figure to visualize the result. We increased the accuracy by 0.22%.
<p align=center> 
<img src='Resources/images/Attemp_2.PNG'  width=500 height=300 >
</p>   

#### Third Attempt: achieved the target model accuracy. Accuracy *77.21%*
- Adding or reducing the number of epochs to the training regimen.
   - Decrease epochs from 100 to 50 
- Evauation for 3st attempt:
As we see the hisotry of accuracy, the figure shows the accuracy imporved by 0.08%.
<p align=center>
<img src='Resources/images/Attemp_3.PNG'  width=500 height=300 >
</p>

#### Final Attempt: achieved the target model accuracy. Accuracy *77.42%*
- Adjusting the input data
   - Increase the number of bins for NAME to 100
- Optimize the numbers of hidden layers
  - layer 1: 200 by using 'relu' activation
  - layer 2: 100 by using 'relu' activation
  - layer 3: 50 by using 'sigmoid' activation
- Optimize the number of epochs to the training regimen.
   - Set epochs to 50
   - Total params: 57,801

- Evauation for final attempt: 
According to the figure, the final attempt increased the accuracy by **0.21%**, and total improved performance by **4.98%**.
<p align=center>
<img src='Resources/images/Final_Attemp.PNG'  width=500 height=300 >
</P>   
    

### Resources:
Explaination for each columns that capture metadata:
  - EIN and NAME — Identification columns
  - APPLICATION_TYPE — Alphabet Soup application type
  - AFFILIATION — Affiliated sector of industry
  - CLASSIFICATION — Government organization classification
  - USE_CASE — Use case for funding
  - ORGANIZATION — Organization type
  - STATUS — Active status
  - INCOME_AMT — Income classification
  - SPECIAL_CONSIDERATIONS — Special consideration for application
  - ASK_AMT — Funding amount requested
  - IS_SUCCESSFUL — Was the money used effectively

## Summary
According to the Charity analysis results, we adjust variables that consider to be the features which makes a big difference in our performance. In the 1st attempt, the model loss improved from *55.54%* to *47.75%* and accuracy have already achieve at *76.91%* after adding NAME feature, bins, and drop few noisy variables. In addition, we increase the number of neurons, hidden layers and activation to analyze the model that shows model improvements. Use different activation function will access the input data differently that might help the model to analyze data. Noisy variables, the number of neurons and hidden layers, activation function and epochs are the key factors to effect the model performance. Thus, we adjust those key factors on other attempts to optimize Neural Network. We are successful ultilize the model by almost 5% and acheive our target predictive accuracy at **77.42%**. In the future studies, we recommand to create for loop to find the best number of neurons, layers and activation functions to achieve the highest accuracy score for model optimization. 

_______________________________________________________________________________________________________________________________________________________________

- Project Contributor: Phoebe J. Miao
- Email: phoebem2021data@gmail.com
