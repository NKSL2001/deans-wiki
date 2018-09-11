+++
title = "Analysis Models"
description = ""
weight = 100
+++

#### Data Flow Diagram
`TODO`

#### Entity-Relationship Diagram (ER Diagram)
`TODO`

#### Dialog Map

<iframe frameborder="0" style="width:100%;height:597px;" src="https://www.draw.io/?lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=Dialog%20Map.html#Uhttps%3A%2F%2Fdrive.google.com%2Fuc%3Fid%3D1PPxpYY9XT-8TiFQFEEy5Drvb61QO1U6r%26export%3Ddownload"></iframe>

#### Decision Tables

|Condition\\Requirement Number| 1 | 2 | 3 | 4 | 5 | 6 | 
|-----------------|---|---|---|---|---|---| 
| isOperator      | F | T | T | T | T | T | 
| isAdmin         | - | F | F | F | T | T | 
| isDispatched    | - | T | T | F | T | T | 
| isResolved      | - | F | T | F | F | T | 
| Action          |   |   |   |   |   |   | 
| Accept Dispatch |   |   |   | X |   |   | 
| Reject Dispatch | X | X | X |   | X | X | 
