🥗 AI-Based Personalized Diet Plan Generator

An AI-powered nutrition assistant that generates personalized 7-day diet plans based on user health information and medical reports.
The application allows users to either manually enter health details or upload medical reports (PDF/Image) which are analyzed using OCR and AI to generate a customized diet plan.

The system uses Groq LLM (LLaMA model) to analyze user health data and generate structured nutrition recommendations.

🚀 Features
1️⃣ Manual Diet Plan Generation

Users can generate a diet plan without uploading a medical report.

The user simply enters:

Age

Weight

Height

Fitness goal (Weight loss / Muscle gain / Maintain weight)

Diet preference (Vegetarian / Non-Vegetarian)

Activity level

The AI then:

Calculates health context

Analyzes user goals

Generates a personalized 7-day diet plan

Includes breakfast, lunch, dinner, snacks and calorie guidance.

2️⃣ Diet Plan Using Medical Report (Advanced Mode)

Users can upload their medical reports to generate a more accurate diet plan.

Supported formats:

PDF

JPG

PNG

JPEG

The system performs the following steps:

Report Upload

User uploads a medical report file.

Text Extraction

If the file is a PDF → extracted using pdfplumber

If the file is an image → processed using Tesseract OCR

Medical Data Analysis
The extracted medical text may contain values like:

Blood glucose

Cholesterol

Hemoglobin

Blood pressure

Vitamin levels

AI Health Interpretation
The extracted data is sent to the Groq LLM model, which:

Identifies potential health risks

Understands medical conditions

Adjusts nutrition recommendations accordingly.

Personalized Diet Plan Generation
The AI generates:

A structured 7-day meal plan

Breakfast, Lunch, Dinner, Snacks

Daily calorie suggestions

Health precautions

Nutrition advice.

🤖 AI Chatbot Logic

The diet planner works like an AI nutrition chatbot behind the scenes.

The workflow:

User Input
↓
Health Data Collection
↓
(Optional) Medical Report Extraction
↓
Prompt Engineering
↓
Groq LLM Processing
↓
Structured Diet Plan Output

The prompt contains:

User physical metrics

Activity level

Diet preference

Health goals

Extracted medical report text (if uploaded)

The AI then generates a structured nutrition response.

🖥️ Application Interface

The Streamlit application contains two main modes:

Manual Input Mode

Users directly enter their health data to generate a diet plan.

Report Upload Mode

Users upload a medical report and the system generates a more personalized diet plan using OCR and AI.

The interface includes:

Sidebar health input form

Report upload section

Extracted report preview

AI-generated diet plan display.

⚙️ Tech Stack
Programming Language

Python

Framework

Streamlit

AI / LLM

Groq API (LLaMA 3.1 model)

OCR

Tesseract OCR

PDF Processing

pdfplumber

Image Processing

PIL (Python Imaging Library)

Environment Management

python-dotenv


📊 Example Output

The AI generates a structured diet plan like:

Day 1
Breakfast – Oatmeal with fruits
Lunch – Brown rice, grilled vegetables
Dinner – Paneer / chicken with salad
Snacks – Nuts and yogurt

Daily Calories: ~2000 kcal

Health Notes:

Reduce sugar intake

Increase fiber-rich foods

Maintain hydration.

💡 Future Improvements

Possible enhancements:

Calorie tracking

Meal nutrition breakdown

AI health risk scoring

Mobile-friendly UI

Integration with fitness trackers.

📌 Use Cases

Personal health monitoring

Nutrition planning

Fitness coaching tools

Preventive healthcare applications

AI-powered health assistants


