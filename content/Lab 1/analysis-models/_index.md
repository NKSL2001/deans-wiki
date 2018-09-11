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
`TODO`

#### Decision Tables

|Condition\Requirement Number| 1 | 2 | 3 | 4 | 5 | 6 | 
|-----------------|---|---|---|---|---|---| 
| isOperator      | F | T | T | T | T | T | 
| isAdmin         | - | F | F | F | T | T | 
| isDispatched    | - | T | T | F | T | T | 
| isResolved      | - | F | T | F | F | T | 
| Action          |   |   |   |   |   |   | 
| Accept Dispatch |   |   |   | X |   |   | 
| Reject Dispatch | X | X | X |   | X | X | 
