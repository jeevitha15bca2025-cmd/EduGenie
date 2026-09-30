# 8. Project Demonstration

## Project Name

EduGenie – Generative AI Based Personalized Learning Assistant

## Demonstration Objective

The purpose of the demonstration is to show how EduGenie provides AI-powered educational assistance through a web interface.

## Demonstration Flow

### Step 1 – Start the Application

Activate the virtual environment:

.venv\Scripts\activate.bat

Start the FastAPI server:

python -m uvicorn main:app --reload

Open the application:

http://127.0.0.1:8000

## Step 2 – Select Learning Activity

The user can select one of the available learning activities:

- Q&A
- Explain
- Quiz
- Summary
- Learning Path

## Step 3 – Enter Educational Content

The student enters a question, topic or educational content into the input field.

## Step 4 – Select Learning Level

For applicable activities, the student selects a learning level such as:

Beginner

## Step 5 – Generate Result

The student clicks the Generate button.

The frontend JavaScript creates the appropriate JSON request and sends it to the FastAPI backend.

## Step 6 – Backend Processing

FastAPI receives the request and calls the appropriate learning module.

For example:

/explain

calls:

explain_topic(topic, level)

## Step 7 – AI Processing

The learning module creates an educational prompt.

The Gemini client sends the prompt to Google Gemini.

## Step 8 – Result Generation

Google Gemini generates the requested educational content.

The response is returned through:

Gemini
↓
Gemini Client
↓
Learning Module
↓
FastAPI
↓
JavaScript
↓
Browser

## Step 9 – Display Result

The generated educational content is displayed to the student in the result section.

## Example Demonstration

### Input

Topic:

What is Artificial Intelligence?

Learning Level:

Beginner

### Processing

Student Input
↓
/explain
↓
explain_topic()
↓
Educational Prompt
↓
Gemini
↓
AI Response

### Expected Output Structure

1. Simple Definition
2. Why It Is Important
3. Step-by-Step Explanation
4. Simple Example
5. Real-World Example
6. Key Points to Remember

## Features to Demonstrate

During the project demonstration, the following features can be shown:

1. Question Answering
2. Topic Explanation
3. Quiz Generation
4. Text Summarization
5. Learning Recommendations
6. Learning level selection
7. Generated result display
8. Copy result functionality

## API Demonstration

The FastAPI documentation can also be demonstrated using:

http://127.0.0.1:8000/docs

This provides an interactive interface for testing the available API endpoints.

## Final Demonstration Flow

EduGenie
↓
Student
↓
Web Frontend
↓
FastAPI Backend
↓
Learning Module
↓
Gemini Client
↓
Google Gemini AI
↓
Generated Educational Result
↓
Student
