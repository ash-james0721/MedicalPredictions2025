# Reducing Missed Appointments: Data Analysis and Predictive Modeling of Patient No-Shows

## Problem Statement:
Missed appointments costs healthcare systems millions yearly. This project identifies key behavioral and demographic patterns behind patient no-shows using real clinical data.

## Objectives:
Cleaning and structuring raw clinical data from appointment dashboard
Performing EDA in finding operational issues
Performing Logistic Regression, Random Forest, and XGBoost in prediction analysis
Coming up with recommendations in lowering the No-Show rates

## Research Question(s):
* Which features are most important in predicting patient no-shows?
* Are patients more likely to show up when the appointment is scheduled closer to the actual appointment date?

## Key Results:
* The XGBoost was the best model with a threshold of 0.488, compared to the Logistic Regression model (threshold of 0.46) and the Random Forest model(threshold of 0.49). The recall for patients who were labelled as 'no shows'(Class 1) was 0.78. This means out of all the no-shows the model correctly labelled those as no-show 78% of the time. The Logistic Regression model correactly labelled patients who were a no-show 68% of the time, and the Random Forest model it ws 24% of the time. This ultimately meant the XGBoost model was the best out of the three models. 
* The features that were most important in the XGBoost model (from most important to least) were:
  * Days Between (Days_Btwn)
  * Age
  * Texts Received (SMS_Received)
  * Poor/Working neighbourhood class (Neighbourhood_Class_Poor)
* The features that were most important in the Logistic Regression model (from most important to least) were:
  * Appointments on Saturdays (AppoinmentDOW_Saturday)
  * Appointment scheduled on Saturdays (ScheduledDOW_Saturday)
  * Days Between 
  * Days in Advance (Days_in_Advanced)
* The features that were most important in the Random Forest model (from most important to least) were:
  * Age
  * Days in Advance 
  * Days Between
  * SMS Recieved

## Operational Recommendations:
* Limit long lead times between scheduling and appointment day, or introduce dynamic reminders (SMS/phone) that increase in frequency as the gap increases
* Ensure that all patients receive timely text reminders (May consider A/B testing different reminder messages to identify the most effective phrasing and timing)
* Provide extra follow-up for patients scheduled on Saturdays
* Consider extra assistance such as transportation and childcare support for patients in poorer neighborhoods
