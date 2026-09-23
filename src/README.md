# Mergington High School Activities API

A simple FastAPI application that allows students to view, join and leave extracurricular activities.

## Features

- View all available extracurricular activities
- Sign up for activities
- Remove a student from an activity

## Getting Started

1. From the repository root, install the dependencies:

   ```
   pip install -r requirements.txt
   ```

2. Run the application:

   ```
   uvicorn src.app:app --reload
   ```

3. Open your browser and go to:
   - API documentation: http://localhost:8000/docs
   - Alternative documentation: http://localhost:8000/redoc

## API Endpoints

| Method | Endpoint                                                          | Description                                                         |
| ------ | ----------------------------------------------------------------- | ------------------------------------------------------------------- |
| GET    | `/activities`                                                     | Get all activities with their details and current participant count |
| POST   | `/activities/{activity_name}/signup?email=student@mergington.edu` | Sign up for an activity                                             |
| DELETE | `/activities/{activity_name}/signup?email=student@mergington.edu` | Remove a student from an activity                                   |

## Tests

Run the backend tests from the repository root:

```
pytest
```

To run only the API tests:

```
pytest tests/test_app.py -q
```

Activity data is stored in memory, so it resets when the server restarts.
