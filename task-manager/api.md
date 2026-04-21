# Task Manager API

## Overview

The Task Manager API allows developers to interact with the task management system programmatically.

It supports creating, retrieving, updating, and deleting tasks.

---

## Base URL

```
https://api.taskmanager.com
```

---

## Authentication

All requests require an API key passed in the header:

```
Authorization: Bearer YOUR_API_KEY
```

---

## Endpoints

### Get All Tasks

**Request**

```
GET /tasks
```

**Example (cURL)**

```
curl -X GET https://api.taskmanager.com/tasks \
  -H "Authorization: Bearer YOUR_API_KEY"
```

**Response**

```json
[
  {
    "id": 1,
    "title": "Buy groceries",
    "completed": false
  }
]
```

---

### Create Task

**Request**

```
POST /tasks
```

**Body**

```json
{
  "title": "Write documentation",
  "completed": false
}
```

**Response**

```json
{
  "id": 2,
  "title": "Write documentation",
  "completed": false
}
```

---

### Update Task

**Request**

```
PUT /tasks/{id}
```

**Body**

```json
{
  "completed": true
}
```

---

### Delete Task

**Request**

```
DELETE /tasks/{id}
```

---

## Common Errors

| Code | Description |
|------|------------|
| 401 | Invalid API key |
| 404 | Task not found |

---

## Error Example

---
### Query Parameters

| Parameter | Type | Description |
|----------|------|------------|
| completed | boolean | Filter tasks by  status |

GET /tasks?completed=true

```json
{
  "error": "Unauthorized",
  "message": "Invalid API key"
}
```
