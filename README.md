# NPS2001Project
NPS2001Project - forecasting hospital waiting times using MOH provided data
ReadMe File (Milestone Report 1)


Which real world problem have you chosen to work on? Why is it an important problem?

There is currently a lack of information with regards to the admission capacity for public hospitals in Singapore. For public hospitals, data for bed occupancy rate and waiting time to be warded is published and updated daily at midnight. However, though the information is available and up-to-date, most patients lack access to or awareness of this data and are ultimately subject to substantial waiting times, often ranging from six to fourteen hours (range provided by MOH statistics). Should the published data be both readable and accessible to patients, patients could assess if another hospital has a lower occupancy rate, potentially choosing a hospital with shorter waiting times. 

What will your app do and how will it help solve or mitigate the problem?

We propose to implement time series forecasting algorithms into an app by utilising publicly available waiting time and bed occupancy rate data. Ultimately, the app aims to optimise hospital selection, minimising waiting times for patients and improving their overall healthcare experience by providing better recommendations. Our solution hence addresses existing inefficiencies in hospital selection by leveraging a data-driven approach and obtains data from reputable sources such as the Ministry of Health (MOH). 

What is the central algorithm or class of algorithms that will enable this app to work?

Time Series Forecasting: The time series forecasting aspect of the algorithm takes into account the temporal nature of the data. By analysing historical waiting time and bed occupancy rate trends over time, the algorithm can extrapolate future patterns. This enables it to anticipate fluctuations in demand and resource availability, allowing for more accurate recommendations. In the context of hospital waiting times, ARIMA (AutoRegressive Integrated Moving Average) is a widely used time series forecasting algorithm that can be employed to predict future waiting times based on historical data. ARIMA is particularly effective when dealing with data that exhibits patterns, trends, and seasonality, which are common characteristics of hospital waiting time data.
 
What would the algorithm need to do (you can illustrate this with a flow chart) in your app? 









The ARIMA (AutoRegressive Integrated Moving Average) time forecasting algorithm comprises several crucial steps. It starts with "Data Input," where historical time series data is collected, followed by "Data Processing," (Decomposition) which includes tasks like handling missing data and outliers. The algorithm (Algorithmic formulation) then checks for "Stationarity," ensuring that statistical properties remain constant over time, a crucial assumption in ARIMA modelling. If the data isn't stationary, it undergoes "Differencing" iteratively to achieve stationarity. Once stationary or made so, the algorithm identifies significant patterns such as "seasonality" (repeating patterns over fixed intervals) and "trends" (gradual changes in data) in the "Pattern Recognition" step. "Parameter Estimation" then estimates model parameters (Abstraction), leading to the construction of the final ARIMA model in "Final Model." Predictions are generated in "Prediction Results" based on the model, aiding in decision-making and planning.

What resources have you found explaining the algorithm that you will use? What are the prerequisites to understand these resources and how easily do you think you will be able to understand them?

Resource
Explanation of Resource
Prerequisites
Time series Forecasting — ARIMA models
Introduction and explanation to ARIMA modelling & forecasting.
NIL
Time series forecasting of hospital Inpatients and Day case waiting list using ARIMA, TBATS and Neural Network Models
MSc Research Project that aims to provide the forecasting of patients waiting list in different time bands over all Ireland’s Hospitals using ARIMA, TBATS and NNM. Conclusion is that ARIMA is the best forecasting algorithm amongst the three models. 
Understanding of ARIMA and time forecasting models.
What Is Arima Model In Time Series | How Arima Model Works | Time Series Forecasting | 
A Youtube video that details how the ARIMA model is set up and how it functions. The video describes the Box-Jenkins method to iterate 3 steps to build the ARIMA model and discusses Unit Root Tests needed for stationarity, Autocorrelation Function (ACF) and Partial Autocorrelation Function (PACF). 
NIL


Under what circumstances do you expect users to use your app? What is (are) the target demographic(s) for your app? What issues, if any, might your users run into while using your app and which you have to keep in mind?

Our target demographic will be patients who, in emergencies, urgently need to go to the hospital to be admitted as an inpatient. One potential issue is that, using only a time forecasting algorithm, users may want more personalised data-based  recommendations such as crowd density and current location to provide better estimates of waiting times. Should we go a step further to include such personalised recommendations, consent of users will be required to obtain their location data. This is in contrast to the use of publicly available statistics from the MOH website, which will not bring about any privacy concerns. Another issue we may encounter is that the accuracy of forecasts relies on and is subject to the quality of historical waiting time and occupancy rate data. Inaccurate or incomplete data could lead to unreliable predictions. 
