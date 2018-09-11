+++
title = "Functional Requirements"
description = ""
weight = 10
+++

#### Web Client System
<pre class="white">
1. Web Client System must be able to display real-time status update on a map of Singapore.
    1.1. Web Client System must be able to fetch weather conditions.
    1.2. Web Client System must be able to fetch dengue hotspot information.
    1.3. Web Client System must be able to fetch haze information.
    1.4. Web Client System must be able to display fetched information on a map of Singapore.
2. Web Client System must display phone number for crisis report.
3. Web Users must be able to report crisis using Crisis Report Form.
    3.1. Web Users must be able to see the Incident Report Form in the Crisis Report Page.
    3.2. Web Users must be able to fill in the Crisis Report Form.
        3.2.1. Web Users must provide their name.
        3.2.2. Web Users must provide their contact number.
        3.2.3. Web Users must provide the location of the crisis.
        3.2.4. Web Users must be able to see nearby crisis reported on the same day upon entering location.
        3.2.5. Web Users must provide crisis type.
        3.2.6. Web Users may provide crisis description.
        3.2.7. Web Users may provide one or many types of assistance required, i.e. emergency ambulance, rescue and evacuation, fire-fighting and gas leak control.
    3.3. Web Users must be able to submit Crisis Report Form.
        3.3.1. Web Users must be able to see a success message when submit succeeds.
        3.3.2. Web Users must be able to see a failure message when submit fails.
4. Call Center Operators must be able to login.
    4.1. Call Center Operators must provide their username.
    4.2. Call Center Operators must provide their password.
5. Call Center Operators must be able to input information received from calls.
    5.1. Call Center Operators must be able to login using username and password.
    5.2. Call Center Operators must be able to fill in the Crisis Report Form.
        5.2.1. Call Center Operators must provide the name.
        5.2.2. Call Center Operators must provide the contact number.
        5.2.3. Call Center Operators must provide the location of the crisis.
        5.2.4. Call Center Operators must be able to see nearby crisis reported on the same day upon entering location.
        5.2.5. Call Center Operators must provide crisis type.
        5.2.6. Call Center Operators may provide crisis description.
        5.2.7. Call Center Operators may provide one or many types of assistance required, i.e. emergency ambulance, rescue and evacuation, fire-fighting and gas leak control.
    5.3. Call Center Operators must be able to submit Crisis Report Form.
        5.3.1. Call Center Operators must be able to see a success message when submit succeeds.
        5.3.2. Call Center Operators must be able to see a failure message when submit fails.
6. Call Center Operators must be able to see a list of reported crisis.
    6.1. Call Center Operators must be able to see the type, location, status (active, dispatched, resolved) of each crisis listing.
7. Call Center Operators must be able to edit crisis listing information.
8. Call Center Operators must be able to dispatch crisis interventions for a crisis listing.
9. Admin User must be able to login.
    6.1. Admin User must provide their username.
    6.2. Admin User must provide their password.
10. Admin User must be able to change system settings.
    7.1. Admin User must be able to update predefined crisis type.
    7.2. Admin User must be able to update predefined assistance type.
    7.3. Admin User must be able to update predefined social media account.
    7.4. Admin User must be able to update phone number of emergency agencies.
    7.5. Admin User must be able to update summary reporting Email.
11. Admin User must be able to manage user accounts.
    7.1. Admin User must be able to create new user account.
        7.1.1. Admin User must provide username.
        7.1.2. Admin User must provide password.
        7.1.3. Admin User must provide role (Call Center Operator or Admin User).
    7.2. Admin User must be able to edit user account.
        7.1.1. Admin User may edit username.
        7.1.2. Admin User may edit password.
        7.1.3. Admin User may edit role (Call Center Operator or Admin User).
    7.3. Admin User must be able to delete user account.
</pre>

#### API Service System
<pre class="white">
8. API Service System must be able to provide a real-time status update of Singapore.
    8.1. API Service must be able to provide the weather conditions.
    8.2. API Service must be able to provide dengue hotspots as coordinates.
    8.3. API Service must be able to provide haze information as numeric values.
9. API Service System must be able to process crisis report.
    9.1. API Service System must be able to store crisis report into database.
10. API Service System must be able to return a list of reported crisis.
11. API Service System must be able to handle request of updating crisis listing information.
12. API Service System must be able to handle request of authenticating user with username and password.
13. API Service System must be able to handle request of dispatching crisis interventions.
14. API Service System must be able to handle request of updating system settings.
15. API Service System must be able to handle request of creating new user account.
16. API Service System must be able to handle request of updating user account.
17. API Service System must be able to handle request of deleting user account.
    17.1. API Service System must be able to send crisis interventions request to Notification System.
18. API Service System must be able to generate crisis status summary report every 30 minutes.
    18.1. API Service System must be able to send crisis status summary report to Notification System.
19. API Service System must be able to provide civil defence shelter locations.
    19.1. API Service System must be able to fetch civil defence shelter locations.
    19.2. API Service System must be able to send civil defence shelter locations to Notification System.
</pre>

#### Notification System
<pre class="white">
20. Notification System must be able to send crisis status summary report to Prime Minister’s Office through Email.
21. Notification System must be able to post civil defence shelter locations to Facebook and Twitter.
22. Notification System must be able to send SMS to emergency agencies.
</pre>
