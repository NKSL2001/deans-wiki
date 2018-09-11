+++
title = "Use Cases"
description = ""
weight = 1
+++

## Revision History
Name | Date | Reason For Changes | Version
---- | ---- | ------------------ | -------
Dean | 11/09/2018 | First update | 1.0

## Use Case Diagram

<iframe frameborder="0" style="width:100%;height:590px;" src="https://www.draw.io/?lightbox=1&highlight=0000ff&layers=1&nav=1&title=Use%20Case%20Models#Uhttps%3A%2F%2Fdrive.google.com%2Fuc%3Fid%3D1P9MAQzjLu2sLvzmR4YEDE0AGrVdYOJNA%26export%3Ddownload"></iframe>

## Use Case List
Primary Actor | Use Cases
------------- | ---------
Web User | 1.1 View Singapore Real-time Crisis Status In Web Client System
Web User | 2.1 Report Crisis Using Crisis Report Form
Public User | 2.2 Report Crisis to Call Center Operator
Call Center Operator | 2.3 Report Crisis From Public Call
Call Center Operator | 3.1 View Reported Crisis
Call Center Operator | 3.2 Edit Crisis Listing Information
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
Normal Flow: | 1. User goes to Control Portal Page<br>2. Website authenticates user<br>3. Call Center Operator fills in crisis report form (name, mobile number, location, type of assistance requested (emergency ambulance, rescue, and evacuation, fire-fighting, gas leak control)<br>4. Website validates crisis report form<br>5. Website sends crisis report to API Service System<br>6. Website shows confirmation
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
Use Case Name: | View Reported Crisis
Created By: | Liu Mingyu
Last Updated By: | Liu Mingyu
Date Created: | 09/09/2018
Date Last Updated: | 09/09/2018

-|-
----|----
Actors: | Call Center Operator
Description: | Allow Call Center Operator to view reported crisis
Trigger: | -
Preconditions: | Call Center Operator has logged in
Postconditions: | Call Center Operator has viewed reported crisis
Normal Flow: | 1. User goes to Control Portal Page<br>2. Website authenticates user<br>3. Website fetches reported crisis<br>4. Website displays a list of reported crisis
Alternative Flows: | -
Exceptions: | 2a. Authentication fails due to user not logged in<br><br>1. Website redirects user to login page<br>2. User may log in, return to normal flow at step 2<br><br>3a. Website fails to fetch reported crisis<br><br>1. Website displays message that informs user of failed fetch<br>2. User may reload page, return to normal flow at step 3
Includes: | -
Priority: | High
Frequency of Use: | High
Business Rules: | -
Special Requirements: | -
Assumptions: | -
Notes and Issues: | -

#### 3.2
-|-
----|----
Use Case ID: | 3.2
Use Case Name: | Edit Crisis Listing Information
Created By: | Liu Mingyu
Last Updated By: | Liu Mingyu
Date Created: | 09/09/2018
Date Last Updated: | 09/09/2018

-|-
----|----
Actors: | Call Center Operator
Description: | Allow Call Center Operator to edit crisis information
Trigger: | -
Preconditions: | Call Center Operator has logged in
Postconditions: | Call Center Operator has edited crisis information
Normal Flow: | 1. User goes to Control Portal Page<br>2. Website authenticates user<br>3. Website fetches reported crisis<br>4. Website displays a list of reported crisis<br>5. Call Center Operator edits a crisis listing<br>6. Call Center Operator submits edited crisis listing<br>7. Website sends updated crisis listing to API Service System<br>8. Website shows confirmation
Alternative Flows: | -
Exceptions: | 2a. Authentication fails due to user not logged in<br><br>1. Website redirects user to login page<br>2. User may log in, return to normal flow at step 2<br><br>3a. Website fails to fetch reported crisis<br><br>1. Website displays message that informs user of failed fetch<br>2. User may reload page, return to normal flow at step 3<br><br>7a. Website fails to send updated crisis listing to API Service System<br><br>1. Website displays message that informs user of failed submission<br>2. User may re-submit, return to normal flow at step 7
Includes: | -
Priority: | High
Frequency of Use: | Medium
Business Rules: | -
Special Requirements: | -
Assumptions: | -
Notes and Issues: | -

#### 3.3
-|-
----|----
Use Case ID: | 3.3
Use Case Name: | Dispatch Crisis Interventions
Created By: | Liu Mingyu
Last Updated By: | Liu Mingyu
Date Created: | 09/09/2018
Date Last Updated: | 09/09/2018

-|-
----|----
Actors: | Call Center Operator
Description: | Allow Call Center Operator to dispatch crisis interventions
Trigger: | -
Preconditions: | Call Center Operator has logged in
Postconditions: | Call Center Operator has dispatched crisis interventions
Normal Flow: | 1. User goes to Control Portal Page<br>2. Website authenticates user<br>3. Website fetches reported crisis<br>4. Website displays a list of reported crisis<br>5. Call Center Operator clicks "dispatch" on a crisis listing<br>6. Call Center Operator reviews crisis listing<br>7. Call Center Operator confirms dispatch<br>8. Website sends crisis intervention dispatch request to API Service System<br>9. Website shows confirmation
Alternative Flows: | -
Exceptions: | 2a. Authentication fails due to user not logged in<br><br>1. Website redirects user to login page<br>2. User may log in, return to normal flow at step 2<br><br>3a. Website fails to fetch reported crisis<br><br>1. Website displays message that informs user of failed fetch<br>2. User may reload page, return to normal flow at step 3<br><br>8a. Website fails to send crisis intervention dispatch request to API Service System<br><br>1. Website displays message that informs user of failed request<br>2. User may re-send, return to normal flow at step 8
Includes: | -
Priority: | High
Frequency of Use: | Medium
Business Rules: | -
Special Requirements: | -
Assumptions: | -
Notes and Issues: | -

#### 3.4
-|-
----|----
Use Case ID: | 3.4
Use Case Name: | Resolve Crisis
Created By: | Liu Mingyu
Last Updated By: | Liu Mingyu
Date Created: | 09/09/2018
Date Last Updated: | 09/09/2018

-|-
----|----
Actors: | Call Center Operator
Description: | Allow Call Center Operator to mark a crisis listing as resolved
Trigger: | -
Preconditions: | Call Center Operator has logged in
Postconditions: | Call Center Operator has marked a crisis listing as resolved
Normal Flow: | 1. User goes to Control Portal Page<br>2. Website authenticates user<br>3. Website fetches reported crisis<br>4. Website displays a list of reported crisis<br>5. Call Center Operator clicks "Resolve" on a crisis listing<br>6. Website sends crisis resolve request to API Service System<br>7. "Resolve" button becomes disabled
Alternative Flows: | -
Exceptions: | 2a. Authentication fails due to user not logged in<br><br>1. Website redirects user to login page<br>2. User may log in, return to normal flow at step 2<br><br>3a. Website fails to fetch reported crisis<br><br>1. Website displays message that informs user of failed fetch<br>2. User may reload page, return to normal flow at step 3<br><br>6a. Website fails to send crisis resolve request to API Service System<br><br>1. Website displays message that informs user of failed request<br>2. User may re-attempt, return to normal flow at step 6
Includes: | -
Priority: | High
Frequency of Use: | Medium
Business Rules: | -
Special Requirements: | -
Assumptions: | -
Notes and Issues: | -

#### 4.1
-|-
----|----
Use Case ID: | 4.1
Use Case Name: | Edit System Settings
Created By: | Liu Mingyu
Last Updated By: | Liu Mingyu
Date Created: | 09/09/2018
Date Last Updated: | 09/09/2018

-|-
----|----
Actors: | Admin User
Description: | Allow Admin User to edit system settings
Trigger: | -
Preconditions: | Admin User has logged in
Postconditions: | Admin User has edited system settings
Normal Flow: | 1. User goes to Control Portal Page<br>2. Website authenticates user<br>3. Admin User goes to Setting Page<br>4. Admin User edits system settings (crisis type, assistance type, social media account, emergency agencies, summary reporting Email)<br>5. Admin User clicks "Apply"<br>6. Website sends system setting update request<br>7. Website shows confirmation
Alternative Flows: | -
Exceptions: | 2a. Authentication fails due to user not logged in<br><br>1. Website redirects user to login page<br><br>3a. Setting Page is invisible due to insufficient user privilege<br><br>1. User may re-login using another account
Includes: | -
Priority: | Medium
Frequency of Use: | Low
Business Rules: | -
Special Requirements: | -
Assumptions: | -
Notes and Issues: | -

#### 4.2
-|-
----|----
Use Case ID: | 4.2
Use Case Name: | Manage User Accounts
Created By: | Liu Mingyu
Last Updated By: | Liu Mingyu
Date Created: | 09/09/2018
Date Last Updated: | 09/09/2018

-|-
----|----
Actors: | Admin User
Description: | Allow Admin User to manage user accounts
Trigger: | -
Preconditions: | Admin User has logged in
Postconditions: | Admin User has done user account management operations
Normal Flow: | 1. User goes to Control Portal Page<br>2. Website authenticates user<br>3. Admin User goes to User Page<br>4. Admin User may create, edit or delete accounts
Alternative Flows: | -
Exceptions: | 2a. Authentication fails due to user not logged in<br><br>1. Website redirects user to login page<br><br>3a. Setting Page is invisible due to insufficient user privilege<br><br>1. User may re-login using another account
Includes: | -
Priority: | Medium
Frequency of Use: | Low
Business Rules: | -
Special Requirements: | -
Assumptions: | -
Notes and Issues: | -

#### 5.1
-|-
----|----
Use Case ID: | 5.1
Use Case Name: | Receive Singapore Crisis Status Summary Report
Created By: | Nicholas
Last Updated By: | Liu Mingyu
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

#### 5.2
-|-
----|----
Use Case ID: | 5.2
Use Case Name: | Receive Crisis Intervention Request via SMS
Created By: | Nicholas
Last Updated By: | Liu Mingyu
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

#### 5.3
-|-
----|----
Use Case ID: | 5.3
Use Case Name: | Receive Civil Defence Shelter Locations From Facebook and Twitter
Created By: | Nicholas
Last Updated By: | Liu Mingyu
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
