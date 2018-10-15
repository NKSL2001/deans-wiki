+++ 
title = "API Specification" 
description = "" 
weight = 30
+++

#### Fetch real-time crisis list

```
GET /api/crisis/get_real_time_crisis_list
```

Responses

|name|type|
|----|----|
|status_code|integer|
|error_message|?string|
|data|array|

```
data: [
  {
    id: 1,
    location: {
      lat: 59.95,
      lng: 30.33
     },
    crisis_type: ["Fire", "Injury"]
    crisis_description: "Fire in the whole!"
  },
  {
    id: 2,
    location: {
      lat: 59.35,
      lng: 30.53
     },
    crisis_type: ["Gas Leak Control", "Rescue and Evacuation"]
    crisis_description: "Help!"
  }
...
]
```

#### Staff login

```
POST /api/auth/login
```

Parameters

|name|type|
|----|----|
|username|string|
|password|string|

Responses

|name|type|
|----|----|
|status_code|integer|
|error_message|?string|
