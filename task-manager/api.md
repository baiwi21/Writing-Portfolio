# Task Manager API

## Overview

This API allows developers to interact with the Task Manager system.

---

## Base URL

```
https://api.taskmanager.com
```

---

## Authentication

All requests require an API key.

```
Authorization: Bearer YOUR_API_KEY
```

---

## Endpoints

### Get All Tasks

**Request:**

```
GET /tasks
```

**Response:**

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

**Request:**

```
POST /tasks
```

**Body:**

```json
{
  "title": "Learn API documentation",
  "completed": false
}
```

**Response:**

```json
{
  "id": 2,
  "title": "Learn API documentation",
  "completed": false
}
```

---

### Update Task

**Request:**

```
PUT /tasks/{id}
```

**Body:**

```json
{
  "completed": true
}
```

---

### Delete Task

**Request:**

```
DELETE /tasks/{id}
```

---

## Status Codes

* 200 — Success
* 201 — Created
* 400 — Bad Request
* 401 — Unauthorized
* 404 — Not Found
