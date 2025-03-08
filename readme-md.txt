# Resume Evaluator

A Flask-based web application that evaluates resumes against job descriptions using Google's Gemini AI, and suggests relevant interview questions for shortlisted candidates.

## Features

- Upload and analyze resumes (PDF, DOC, DOCX formats supported)
- Compare resumes against job descriptions for match percentage
- Identify missing keywords and skills
- AI-generated candidate profile summaries
- AI-generated interview questions (both technical and non-technical)
- User feedback system
- Evaluation and feedback history

## Fixed Issues

- Fixed database issue where user feedback was not being saved after submission
- Added new AI-generated candidate questions feature

## Prerequisites

- Python 3.8+
- Google Gemini API key

## Installation

1. Clone the repository:
```
git clone https://github.com/yourusername/resume-evaluator.git
cd resume-evaluator
```

2. Create and activate a virtual environment:
```
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install the dependencies:
```
pip install -r requirements.txt
```

4. Create a `.env` file based on `.env.template` and add your Google API key:
```
SECRET_KEY=your_secret_key_here
GOOGLE_API_KEY=your_google_api_key_here
```

## Running the Application

1. Start the Flask development server:
```
python app.py
```

2. Access the application in your web browser at:
```
http://localhost:5000
```

## Directory Structure

```
resume-evaluator/
├── app.py                 # Main application file
├── requirements.txt       # Python dependencies
├── .env                   # Environment variables (create from .env.template)
├── uploads/               # Directory for uploaded resumes (created automatically)
├── resume_evaluator.db    # SQLite database (created automatically)
└── templates/             # HTML templates
    ├── base.html          # Base template with layout
    ├── index.html         # Homepage with upload form
    ├── history.html       # Evaluation history page
    └── feedback_history.html  # Feedback history page
```

## Usage

1. Upload a resume (PDF, DOC, or DOCX format)
2. Enter the job title and job description
3. Click "Evaluate Resume"
4. View the results including:
   - Match percentage
   - Profile summary
   - Missing keywords
   - Additional information
   - AI-generated interview questions (technical and non-technical)
5. Provide feedback on the evaluation
6. View previous evaluations and feedback in the history pages
