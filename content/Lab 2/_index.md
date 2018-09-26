+++
title = "Lab 2"
description = ""
weight = 2
alwaysopen = true
+++

Requirements Elicitation and Analysis

Deliverables

#### Main System

<iframe frameborder="0" style="width:100%;height:618px;" src="https://www.draw.io/?lightbox=1&highlight=0000ff&layers=1&nav=1&title=Main%20Architecture#Uhttps%3A%2F%2Fdrive.google.com%2Fuc%3Fid%3D13DF7Dh65iVmQL1D55idVs3AoGyOkym7z%26export%3Ddownload"></iframe>

##### Design Reason

- Modifiability by decoupling the computation

Each subsystem comply with predefined interfaces, which make each subsystem interchangable.

- Concurrent execution and Scalability

Each subsystem is ralativelly independent, which makes duplication of save module possible. By introducing duplications, the system could be highly availuable, and effieient.

- Easy Integration

#### Subsystems

- [Web client subsystem]({{%relref "web-client" %}})
- [API Subsystem]({{%relref "api-subsystem" %}})
- [Notification Subsystem]({{%relref "notification-subsystem" %}})
