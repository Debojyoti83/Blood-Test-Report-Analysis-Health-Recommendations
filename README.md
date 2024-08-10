# Blood-Test-Report-Analysis-Health-Recommendations

Problem Statement:
1) Take a sample blood test report. (Sample report: Blood Test Report)
2) Understand what's inside it.
3) Search the internet for articles that fit the person's needs.
4) Make health recommendations based on what they find.

Overview:

This project is part of an AI internship assignment. The goal is to create a system using the CrewAI framework that analyzes a blood test report, searches the web for relevant health articles, and provides health recommendations based on the findings.

Approach:

1. Input: The system takes a blood test report in PDF format.
2. Analysis: The blood test report is analyzed using a custom agent (`Blood Report Analyst`), which summarizes the key health indicators and findings.
3. Web Search: A custom tool (`CustomGoogleSearchTool`) is used to search the internet for articles related to the blood test findings.
4. Recommendations: A `Health Advisor` agent then provides health recommendations based on the analysis and relevant articles, including URLs for further reading.

Requirements:

- Python 3.x
- Libraries:
  - crewai
  - crewai_tools
  - requests
  - json

Setup:

1. Install Required Libraries:
   pip install crewai crewai_tools requests
2. Set API Keys:
     - GOOGLE_API_KEY
     - CUSTOM_SEARCH_ENGINE_ID
     - OPENAI_API_KEY ( using a dummy key to bypass the check because using free api )


3. File Paths:
   - Update the “pdf_path” variable in the code to point to the location of  sample blood test PDF file.
   - Specify the output path where the JSON results will be saved.

How to Run:

1. Execute the Script:
   Run the script using Python:
   python script_name.py
   Replace `script_name.py` with the name of Python file. Ex: health_recommendation_system.py

2. Results:
   - The script analyzes the blood report and saves the health recommendations and related articles to the specified output file in JSON format.

Output:

The output is a JSON file containing:

- A summary of the key findings from the blood test report.
- Health recommendations based on the findings.
- URLs to relevant articles for further reading.
