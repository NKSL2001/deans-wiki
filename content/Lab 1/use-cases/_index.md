+++
title = "Use Cases"
description = ""
weight = 1
+++

## Revision History
Name | Date | Reason For Changes | Version
---- | ---- | ------------------ | -------
-- | -- | -- | 1.0

## Use Case Diagram
![Use Case Diagram](/images/Use Case Models.png)

## Use Case List
Primary Actor | Use Cases
------------- | ---------
Web User | 1.1 View Singapore Real-time Crisis Status In Web Client System
Web User | 2.1 Report Crisis Using Crisis Report Form
Public User | 2.2 Report Crisis to Call Center Operator
Call Center Operator | 2.3 Report Crisis From Public Call
Call Center Operator | 3.1 View Unresolved Reported Crisis
Call Center Operator | 3.2 Edit Crisis Information
Call Center Operator | 3.3 Dispatch Crisis Interventions
Call Center Operator | 3.4 Resolve Crisis
Admin User | 4.1 Edit System Settings
Admin User | 4.2 Manage User Accounts
Prime Minister’s Office | 5.1 Receive Singapore Crisis Status Summary Report
Emergency Agencies | 5.2 Receive Crisis Intervention Request via SMS
Public User | 5.3 Receive Civil Defence Shelter Locations From Facebook and Twitter


## Use Case Description
#### 1.1
-|-
----|----
Use Case ID: | 1.1
Use Case Name: | View Singapore Real-time Crisis Status In Web Client System
Created By: | Liu Mingyu
Last Updated By: | Liu Mingyu
Date Created: | 09/09/2018
Date Last Updated: | 09/09/2018

-|-
----|----
Actors: | Web User
Description: | Allow Web User to view real-time crisis status of Singapore
Trigger: | User enters the Web Client System
Preconditions: | Web User has entered the website
Postconditions: | Web User is able to view real-time crisis status of Singapore
Normal Flow: | 1. User enters the website<br>2. Website fetches real-time weather conditions, dengue hotspot information, haze information, emergency situation (reported by user) from API Service System<br>3. Website presents the fetched data on a map of Singapore<br>4. User may refresh the map to see real time status
Alternative Flows: | -
Exceptions: | 2a. Website fails to fetch one or more types of data<br><br>1. Website displays successfully fetched data<br>2. Website displays message that informs user of which type of data failed to load<br>3. User may request fetching again by clicking Retry
Includes: | -
Priority: | High
Frequency of Use: | High
Business Rules: | -
Special Requirements: | -
Assumptions: | -
Notes and Issues: | -

#### 2.1
-|-
----|----
Use Case ID: | 2.1
Use Case Name: | Report Crisis Using Crisis Report Form
Created By: | Liu Mingyu
Last Updated By: | Liu Mingyu
Date Created: | 09/09/2018
Date Last Updated: | 09/09/2018

-|-
----|----
Actors: | Web User
Description: | Allow Web User to report crisis by submitting forms
Trigger: | -
Preconditions: | -
Postconditions: | User has reported crisis
Normal Flow: | 1. User goes to Crisis Report section in Web Client System<br>2. User fills in Crisis Report form with name, mobile number, location, type of assistance requested (emergency ambulance, rescue, and evacuation, fire-fighting, gas leak control) and Crisis description<br>3. User click submit button<br>4. Website validates crisis report form<br>5. Website sends Crisis details to API Service System<br>6. Website shows confirmation
Alternative Flows: | -
Exceptions: | 4a. Website fails to validate Crisis Report form due to incompleteness<br><br>1. Website displays message that informs user of incompleteness of content<br>2. User may re-fill Crisis Report form<br>3. User may re-submit Crisis Report form, return normal flow at step 4<br><br>5a. Website fails to send Crisis Report form to API Service System<br><br>1. Website displays message that informs user of failed submission<br>2. User may re-submit crisis report form, return to normal flow at step 4
Includes: | -
Priority: | High
Frequency of Use: | Low
Business Rules: | -
Special Requirements: | -
Assumptions: | -
Notes and Issues: | -

#### 2.2
-|-
----|----
Use Case ID: | 2.2
Use Case Name: | Report Crisis to Call Center Operator
Created By: | Liu Mingyu
Last Updated By: | Liu Mingyu
Date Created: | 09/09/2018
Date Last Updated: | 09/09/2018

-|-
----|----
Actors: | Public User
Description: | Allow Public User to report crisis through Call Center Operator
Trigger: | -
Preconditions: | -
Postconditions: | User has reported crisis
Normal Flow: | 1. User goes to Crisis Report Page<br>2. User looks up phone number for crisis report<br>3. User dials the phone number<br>4. User reports crisis through Call Center Operator
Alternative Flows: | -
Exceptions: | -
Includes: | -
Priority: | High
Frequency of Use: | Low
Business Rules: | -
Special Requirements: | -
Assumptions: | -
Notes and Issues: | -

#### 2.3
-|-
----|----
Use Case ID: | 2.3
Use Case Name: | Report Crisis From Public Call
Created By: | Liu Mingyu
Last Updated By: | Liu Mingyu
Date Created: | 09/09/2018
Date Last Updated: | 09/09/2018

-|-
----|----
Actors: | Call Center Operator
Description: | Allow Call Center Operator to report crisis received from public call
Trigger: | Call Center Operator received crisis report from public call
Preconditions: | Call Center Operator has logged in
Postconditions: | Call Center Operator has reported crisis
Normal Flow: | 1. User goes to Call Center Operation Page<br>2. Website authenticates user<br>3. Call Center Operator fills in crisis report form (name, mobile number, location, type of assistance requested (emergency ambulance, rescue, and evacuation, fire-fighting, gas leak control)<br>4. Website validates crisis report form<br>5. Website sends crisis report to API Service System<br>6. Website shows confirmation
Alternative Flows: | -
Exceptions: | 2a. Authentication fails due to user not logged in<br><br>1. Website redirects user to login page<br>2. User may log in, return to normal flow at step 2<br><br>4a. Website fails to validate crisis report form due to incompleteness<br><br>1. Website displays message that informs user of incomplete form<br>2. User may re-fill crisis report form<br>3. User may re-submit crisis report form, return to normal flow at step 4<br><br>5a. Website fails to send crisis report to API Service System<br><br>1. Website displays message that informs user of failed attempt<br>2. User may retry, return to normal flow at step 5
Includes: | -
Priority: | High
Frequency of Use: | Low
Business Rules: | -
Special Requirements: | -
Assumptions: | -
Notes and Issues: | -

#### 3.1
-|-
----|----
Use Case ID: | 3.1
Use Case Name: | Receive Singapore Crisis Status Summary Report
Created By: | -
Last Updated By: | -
Date Created: | 09/09/2018
Date Last Updated: | 09/09/2018

-|-
----|----
Actors: | Prime Minister's Office
Description: | Allow Prime Minister's Office to receive crisis status summary report every 30 minutes
Trigger: | Check ever 30 minutes
Preconditions: | -
Postconditions: | Prime Minister's Office has received crisis status summary report
Normal Flow: | 1. API Service System checks whether 30 minutes have elapsed since last report<br>2. API Service System generates crisis status summary report<br>3. API Service System stores crisis status summary report into database<br>4. API Service System sends crisis status summary report to Prime Minister's Office through Notification System
Alternative Flows: | -
Exceptions: | 1a. 30 minutes have not elapsed<br><br>1. Wait 5 minutes and check again
Includes: | -
Priority: | High
Frequency of Use: | High (every 30 minutes)
Business Rules: | -
Special Requirements: | -
Assumptions: | -
Notes and Issues: | -

#### 3.2
-|-
----|----
Use Case ID: | 3.2
Use Case Name: | Receive Crisis Intervention Request via SMS
Created By: | -
Last Updated By: | -
Date Created: | 09/09/2018
Date Last Updated: | 09/09/2018

-|-
----|----
Actors: | Emergency Agencies
Description: | Allow emergency agencies to receive crisis intervention request via SMS
Trigger: | Assistance is requested
Preconditions: | -
Postconditions: | Emergency agencies have received SMS
Normal Flow: | 1. Notification System sends SMS to emergency agencies
Alternative Flows: | -
Exceptions: | -
Includes: | -
Priority: | High
Frequency of Use: | Low (when assistance is requested)
Business Rules: | -
Special Requirements: | -
Assumptions: | -
Notes and Issues: | -

#### 3.3
-|-
----|----
Use Case ID: | 3.3
Use Case Name: | Receive Civil Defence Shelter Locations From Facebook and Twitter
Created By: | -
Last Updated By: | -
Date Created: | 09/09/2018
Date Last Updated: | 09/09/2018

-|-
----|----
Actors: | Public User
Description: | Allow Public User to see latest civil defence shelter locations on Facebook and Twitter
Trigger: | Check 2 hours
Preconditions: | -
Postconditions: | Latest civil defence shelter locations have been posted on Facebook and Twitter
Normal Flow: | 1. API Service System checks whether 2 hours have elapsed since last update<br>2. API Service System fetches latest civil defence shelter locations<br>3. API Service System posts latest civil defence shelter locations to Facebook and Twitter through Notification System
Alternative Flows: | -
Exceptions: | 1a. 2 hours have not elapsed<br><br>1. Wait 20 minutes and check again
Includes: | -
Priority: | Medium
Frequency of Use: | High (every 2 hours)
Business Rules: | -
Special Requirements: | -
Assumptions: | -
Notes and Issues: | -
