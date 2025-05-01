# Job_Search_Automation_Make

Automate job listing analysis and tracking with OpenAI and Airtable using Make (formerly Integromat). This project helps job seekers save time by summarizing and organizing job opportunities automatically.

## Introduction

This project aims to assist individuals actively searching for job opportunities by automating the collection, analysis, and classification of job listings from various sources. By leveraging **Make.com**, **OpenAI's ChatGPT**, and **Airtable**, the system allows the user to:

- Extract job listings from RSS feeds
- Summarize and analyze job descriptions using GPT
- Store and manage results in a structured Airtable database

This workflow minimizes manual effort and ensures no opportunity is missed during the search.

**1. Business Question**

• How can a job seeker reduce time spent reviewing job offers and increase focus on relevant opportunities?

• Can AI help summarize long job descriptions and assess compatibility with the user’s profile?

• Is it possible to automatically store and organize opportunities for follow-up, filtering, and documentation?

**2. Dataset**

The system processes job posts from RSS feeds (e.g., job boards) and extracts key information using HTTP and AI tools.

**1. Input: RSS Job Listings**

Each job listing contains:

- Title  
- Company Name  
- Description (HTML or plain text)  
- URL  

**2. Output: Airtable Table**

Example output fields stored in Airtable:

| Job Title      | Company      | GPT Summary                     | Link                    | Tags     | Match Score         |
|----------------|--------------|----------------------------------|-------------------------|----------|----------------------|
| Data Analyst   | BackMarket   | Short summary (3 bullet points)  | www.example.com/job123  | Python   | Strong match (GPT)   |

**3. Method: Automation Workflow**

The following steps are automated using Make:

1. **Trigger (Scheduler):** Run daily or hourly to check new listings  
2. **RSS Feed:** Pull job postings from selected RSS URLs  
3. **Airtable Search:** Prevent duplicates by checking if a job already exists  
4. **HTTP Request:** Retrieve full job descriptions  
5. **Sleep (Delay):** Add delay to avoid API throttling  
6. **ChatGPT Prompt (1):** Summarize job description into short bullet points  
7. **ChatGPT Prompt (2):** Assess match with candidate profile or extract key skills  
8. **HTTP File:** (Optional) Retrieve company logo or attachment  
9. **Airtable Create:** Save all results into a job tracker table  

## Data Visualization

This scenario is visualized in Make as a no-code flow:

![Scenario Screenshot](https://your-upload-link-or-local-path.png)

The green modules represent OpenAI prompts used to generate summaries and analyze matches.

## Insights

**1. Time Savings and Focus:**

• The scenario reduces time spent reading long job descriptions  
• It helps the user focus on high-potential opportunities  

**2. AI-Powered Classification:**

• GPT summarizes roles in human-readable form  
• It evaluates alignment with your personal profile, saving mental energy  

**3. Job Management System:**

• Airtable serves as a lightweight job CRM (pipeline tracker)  
• Records are easily filterable by tags, match score, or date  
