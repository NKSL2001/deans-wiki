+++
title="Design Rationale"
description=""
weight=80
+++

*By designing a combination of Client-Server Architecture and MVC pattern.*

*The whole system contains three main components with Client-Server architecture.*
*MVC pattern are used in API Service Subsystem Logic.*

*Rationale and advantages are as followed:*
*First of all, by selecting Client-Server Architecture overhead:*

#### Advantages:
1. Centralization of control:

Access, resources and integrity of the data are controlled by the dedicated server so that a program or unauthorized client cannot damage the system. This centralization also facilitates task of updating data or other resources (better than the networks P2P).

2. Scalability:

You can increase the capacity of clients and servers separately. Any element can be increased (or enhanced) at any time, or you can add new nodes to the network (clients or servers).

3. Easy maintenance: 

distribute the roles and responsibilities to several standalone computers, you can replace, repair, upgrade, or even move a server, while  customers will not be affected by that change (or minimally affect). This independence of the changes is also known as encapsulation.

There are technologies sufficiently developed, designed for the paradigm of C / S to ensure security in transactions, interface friendliness, and ease of use.


*Thus, over all, by using Independent Components, we will be able to:*


1. Modifiability by decoupling the computation


Each subsystem comply with predefined interfaces, which make each subsystem interchangeable.

2. Concurrent execution and Scalability


Each subsystem is relatively independent, which makes duplication of save module possible. By introducing duplications, the system could be highly available, and efficient.
 
*To explore more detailed design, by selecting MVC for API Service System:*

It divides a given software application into three interconnected parts, so as to separate internal representations of information from the ways that information is presented to or accepted from the user. With advantages: 


1.  Faster development process: MVC supports rapid and parallel development. With MVC, one programmer can work on the view while other can work on the controller to create business logic of the web application. The application developed using MVC can be faster than application developed using other development patterns.

2.  Ability to provide multiple views: In the MVC Model, you can create multiple views for a model. Code duplication is very limited in MVC because it separates data and business logic from the display.

3. Support for asynchronous technique: MVC also supports asynchronous technique, which helps developers to develop an application that loads very fast.

4. Modification does not affect the entire model: Modification does not affect the entire model because model part does not depend on the views part. Therefore, any changes in the Model will not affect the entire architecture.

5. MVC model returns the data without formatting: MVC pattern returns data without applying any formatting so the same components can be used and called for use with any interface.




 

