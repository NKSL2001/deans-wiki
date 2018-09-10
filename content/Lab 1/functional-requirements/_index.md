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
        3.2.4. Web Users must provide the type of assistance required, i.e. emergency ambulance, rescue and evacuation, fire-fighting and gas leak control.
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
        5.2.4. Call Center Operators must provide the type of assistance required, i.e. emergency ambulance, rescue and evacuation, fire-fighting and gas leak control.
    5.3. Call Center Operators must be able to submit Crisis Report Form.
        5.3.1. Call Center Operators must be able to see a success message when submit succeeds.
        5.3.2. Call Center Operators must be able to see a failure message when submit fails.
</pre>

#### API Service System
<pre class="white">
6. API Service System must be able to provide a real-time status update of Singapore.
    6.1. API Service must be able to provide the weather conditions.
    6.2. API Service must be able to provide dengue hotspots as coordinates.
    6.3. API Service must be able to provide haze information as numeric values.
7. API Service System must be able to process crisis report.
    7.1. API Service System must be able to store crisis report into database.
8. API Service System must be able to generate crisis status summary report every 30 minutes.
9. API Service System must be able to provide civil defence shelter locations.
    9.1. API Service System must be able to fetch civil defence shelter locations.
</pre>

#### Notification System
<pre class="white">
10. Notification System must be able to send crisis status summary report to Prime Minister’s Office via Email.
11. Notification System must be able to post civil defence shelter locations to Facebook and Twitter.
12. Notification System must be able to send SMS to emergency agencies.
</pre>