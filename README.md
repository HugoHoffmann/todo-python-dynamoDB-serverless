# TODO List API

This project is a serverless TODO list API built with Python, the Serverless Framework, and AWS DynamoDB. The API allows you to create, read, update, and delete TODO items.

## Features

- **Create** a new TODO item
- **Read** a TODO item by ID
- **Update** an existing TODO item
- **Delete** a TODO item

## Prerequisites

- **Node.js** and **npm**
- **Python 3.9+**
- **AWS CLI** configured with appropriate credentials
- **Serverless Framework** installed globally:
  ```bash
  npm install -g serverless

## Install dependencies

```
pip install boto3
```

## Project structure
```
├── src/handler.py       # CRUD functions for the API
├── serverless.yml       # Serverless Framework configuration
└── README.md            # Project documentation
```

## Deploy the service

```serverless deploy```


## API Endpoints and Example Requests

### Create TODO
- **Method**: `POST`
- **Endpoint**: `/todos`
- **Request Body**:
  ```json
  {
    "task": "Your task name"
  }
- **Example**: 
```curl -X POST https://your-api-url/todos -H "Content-Type: application/json" -d '{"task": "Learn Serverless"}'```


### UPDATE TODO
- **Method**: `PUT`
- **Endpoint**: `/todos/{id}`
- **Request Body**:
  ```json
  {
    "task": "Your task name",
    "completed": true
  }
- **Example**: 
```curl -X PUT https://your-api-url/todos/{id} -H "Content-Type: application/json" -d '{"task": "Learn Serverless", "completed": true}'```


### DELETE TODO
- **Method**: `DELETE`
- **Endpoint**: `/todos/{id}`
- **Example**: 
```curl -X DELETE https://your-api-url/todos/{id}```

### GET TODO
- **Method**: `GET`
- **Endpoint**: `/todos/{id}`
- **Example**: 
```curl -X GET https://your-api-url/todos/{id}```
