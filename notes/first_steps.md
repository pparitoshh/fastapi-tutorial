# FastAPI First Steps

## Basic Setup
1. Create a file `main.py` with the following code:
```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
async def root():
    return {"message": "Hello World"}
```

## Running the Application
- Use the command: `fastapi dev main.py`
- The server will start at http://127.0.0.1:8000
- Interactive API docs available at http://127.0.0.1:8000/docs
- Alternative API docs at http://127.0.0.1:8000/redoc

## Key Components Explained

### 1. FastAPI Import
- `FastAPI` is a Python class that provides all API functionality
- It inherits from Starlette, so you can use all Starlette features

### 2. FastAPI Instance
- Create an instance: `app = FastAPI()`
- This instance is the main point of interaction for creating your API

### 3. Path Operations
- Path: The last part of the URL (e.g., `/items/foo`)
- Operation: HTTP methods (GET, POST, PUT, DELETE, etc.)
- Common HTTP methods and their typical uses:
  - POST: Create data
  - GET: Read data
  - PUT: Update data
  - DELETE: Delete data

### 4. Path Operation Decorator
- Use `@app.get("/")` to define a GET operation at path "/"
- Other decorators available:
  - `@app.post()`
  - `@app.put()`
  - `@app.delete()`
  - And more: `@app.options()`, `@app.head()`, `@app.patch()`, `@app.trace()`

### 5. Path Operation Function
- The function below the decorator handles the request
- Can be defined as async or normal function:
```python
@app.get("/")
async def root():  # async version
    return {"message": "Hello World"}

@app.get("/")
def root():  # normal version
    return {"message": "Hello World"}
```

### 6. Return Content
- Can return various types:
  - Dictionaries
  - Lists
  - Single values (str, int, etc.)
  - Pydantic models
  - Many other objects that can be automatically converted to JSON

## OpenAPI Integration
- FastAPI automatically generates an OpenAPI schema
- View raw schema at http://127.0.0.1:8000/openapi.json
- This schema powers the interactive documentation
- Can be used to generate client code automatically

## Recap
1. Import FastAPI
2. Create an app instance
3. Write path operation decorators
4. Define path operation functions
5. Run the development server

[Source: FastAPI Documentation](https://fastapi.tiangolo.com/tutorial/first-steps/) 