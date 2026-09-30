# 6. Project Testing

## Testing Overview

Testing was performed to verify that the EduGenie application works correctly at the frontend, backend and API levels.

## 1. Browser Testing

The application can be tested through:

http://127.0.0.1:8000

Example test:

Task:
Explain a Topic

Level:
Beginner

Topic:
What is Python?

Expected Result:

The generated explanation should appear in the result section.

## 2. API Testing

FastAPI provides interactive API documentation through Swagger UI.

Open:

http://127.0.0.1:8000/docs

The following endpoints can be inspected and tested:

- POST /qa
- POST /explain
- POST /quiz
- POST /summarize
- POST /learn/recommendations

## 3. Automated Testing

The project contains:

tests/
└── test_api.py

Automated tests can be executed using:

python -m pytest -q

## 4. Frontend Testing

The following frontend features should be checked:

- Page loads correctly
- CSS loads correctly
- JavaScript loads correctly
- Task selection works
- Input field works
- Generate button works
- Results are displayed
- Copy button works

## 5. Backend Testing

The following backend functionality should be checked:

- FastAPI starts correctly
- Uvicorn starts correctly
- API routes respond correctly
- JSON responses are returned
- Errors are handled correctly

## 6. Gemini Testing

Gemini integration should be checked for:

- API key configuration
- Model configuration
- Successful content generation
- Empty responses
- Temporary service failures

## 7. Error Testing

The application handles possible issues such as:

- Missing API key
- Missing Gemini package
- Gemini 503 errors
- Backend errors
- Failed frontend requests
- Missing CSS
- Missing JavaScript

## Testing Checklist

### Environment

- Python 3.12 installed
- Virtual environment created
- Virtual environment activated
- Dependencies installed

### Configuration

- .env created
- Gemini API key configured
- Gemini model configured
- .env excluded from Git

### Backend

- FastAPI starts
- Uvicorn starts
- / works
- /docs works
- /explain works
- /qa works
- /quiz works
- /summarize works
- /learn/recommendations works

### Frontend

- Page loads
- CSS loads
- JavaScript loads
- Task selection works
- Input works
- Generate button works
- Results display correctly
- Copy button works

### Testing

- pytest executed
- API errors checked
- Gemini errors handled
- Empty responses handled
