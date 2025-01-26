# Student_Quiz_Performance_Analysis

## Table of Contents
- [Project Overview](#project-overview)
- [Technologies Used](#technologies-used)
- [Setup Instructions](#setup-instructions)
- [Features](#features)
- [Code Workflow](#code-workflow)
- [File Outputs](#file-outputs)
- [Future Enhancements](#future-enhancements)

## Project Overview
This project focuses on:
- Extracting relevant quiz details, such as questions and options, from JSON APIs.
- Analyzing question-level data, including correct/incorrect options and difficulty levels.
- Normalizing historical user quiz performance for further analysis.

## Technologies Used
- Python
- Pandas for data manipulation
- Requests for API communication
- Jupyter Notebook for code execution

## Setup Instructions
### Prerequisites:
- Ensure Python 3.x is installed on your machine.

### Install the required libraries:
```bash
pip install pandas requests
```
### Clone or Download the Project:
```bash
git clone https://github.com/PRANAYBHUMAGOUNI/Student_Quiz_Performance_Analysis  
cd personalized-Student_Recommendations
```
### Run the Script:
Execute the script in your Jupyter Notebook.

# Features

## Loading Current Quiz Data
- Fetches quiz data from an external API: [https://www.jsonkeeper.com/b/LLQT](https://www.jsonkeeper.com/b/LLQT).
- Normalizes JSON into a DataFrame for easy manipulation.

## Extracting Relevant Quiz Details
- Extracts columns such as:
  - Quiz ID
  - Title
  - Topic
  - Difficulty level
  - Question count
  - Detailed questions

## Detailed Question Analysis
- Extracts each question's:
  - ID
  - Description
  - Options
- Analyzes:
  - Number of correct options
  - Number of incorrect options
  - Total options
- Adds metadata like difficulty level and topics.

## Loading and Analyzing Historical Quiz Data
- Fetches user quiz performance data from another API: [https://api.jsonserve.com/XgAgFJ](https://api.jsonserve.com/XgAgFJ).
- Normalizes historical data into a DataFrame for accuracy and score analysis.

## Code Workflow
### Importing Libraries
```bash
import pandas as pd  
import requests  
```
## Fetching Current Quiz Data

The script fetches the current quiz JSON data from the API and converts it into a Pandas DataFrame.  
**Example API used**: [https://www.jsonkeeper.com/b/LLQT](https://www.jsonkeeper.com/b/LLQT)

## Extracting Relevant Columns
- Extracted columns:
  - `quiz.id`
  - `quiz.title`
  - `quiz.topic`
  - `quiz.questions_count`
  - `quiz.questions`

## Analyzing Question Details
- Iterates through `quiz.questions` to compute details such as:
  - Correct/Incorrect options
  - Detailed solutions
  - Question difficulty

## Loading Historical Quiz Data
- **Historical data API**: [https://api.jsonserve.com/XgAgFJ](https://api.jsonserve.com/XgAgFJ).
- Extracts and normalizes columns like:
  - Avg_Score
  - Avg_Accuracy
  - Recommendation
  - Student Persona

## Output Generation
- Outputs cleaned and structured data as Pandas DataFrames for easy export.

### File Outputs
- **questions_df**: DataFrame containing detailes about student present details about Quizs.
- **historical_quiz_df**: DataFrame containing student previous quiz performances.

## Future Enhancements
- **Visualization**: Add support for visualizing quiz performance metrics using libraries like Matplotlib or Seaborn.
- **Data Export**: Enable automatic export of processed data to CSV or Excel.
- **API Integration**: Include support for live updates from APIs.
- **Error Handling**: Enhance error handling for API failures or JSON parsing issues.











