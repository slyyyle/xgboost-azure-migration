# xgboost-azure-migration
 Training an xgboost model both locally and utilizing Microsoft Azure's Python SDK v2.  

## Main Takeaways:  

My main goal for this mini-project was gaining familiarity and demonstrating my ability to use Microsoft Azure to train a model for ultimate deployment to an API endpoint.  While fitting and finetuning was not a major goal of this project, I did spend some time analyzing feature importance and trying to pretend that this was a real world solution.  This resulted in me altering the prediction probability threshold, and balancing precision with recall for the diabetes class.  I ultimately decided on a probability threshold that was quite low, with the reasoning that this model would clearly not be used to diagnose diabetes, but may be used to identify patients that are high risk for diabetes.  Essentially, the idea is that I was willing to sacrifice precision for recall, as I considered the fact that labeling more patients as high risk for diabetes who were not in fact high risk as preferable to failing to label patients as high risk who were indeed high risk for diabetes diagnosis.  

## Contents:  

*xgboost_example.ipynb* - This example contains the code utilized to instantiate the model code, which was later adapted to be used on Microsoft Azure ML Studio.  

*xgboost train and deploy.ipynb* - This notebook was created using Azure ML Studio and a cloud compute cluster to pratice and demonstrate my ability to adapt local solutions to Azure.  While XGBoost does not require much scaling nor tons of compute, the idea was to gain experience in using MLFlow, become comfortable with using the Azure Python SDK v2 via creating training "jobs", and to begin operating under a more focused "ML Lifecycle" framework.  It also enables me to start to gain experience with deploying and consuming an API endpoint using Python as well as the .NET framework.  

*diabetes_prediction_dataset.csv* - This was the csv that was used to train the model locally.  I also practiced registering this as a data asset in Azure, which was then used to train the model using cloud compute as opposed to simply uploading the csv file to the Notebooks project folder.  
