# Job_Search_Automation_Make

Automate job listing analysis and tracking with OpenAI and Airtable using Make (formerly Integromat). This project helps job seekers save time by summarizing and organizing job opportunities automatically.

## Introduction

This project aims to assist individuals actively searching for job opportunities by automating the collection, analysis, and classification of job listings from various sources. By leveraging **Make.com**, **OpenAI's ChatGPT**, and **Airtable**, the system allows the user to:

- Collect job offers from RSS feeds
- Summarize and analyze job descriptions using GPT
- Store and manage results in a structured Airtable database

It streamlines the job search process, making it easier to track and prioritize the most relevant opportunities.

**1. Business Question**

• How can a job seeker reduce time spent reviewing job offers and increase focus on relevant opportunities?

• Can AI help summarize long job descriptions and assess compatibility with the user’s profile?

• Is it possible to automatically store and organize opportunities for follow-up, filtering, and documentation?

**2. Dataset**

Job data is pulled from RSS feeds of job boards and enriched using OpenAI and HTTP requests.

**1. Input: RSS Job Listings**

Each job listing contains:

- Title  
- Company Name  
- Description (HTML or plain text)  
- URL  

**2. Output: Airtable Table**

Example output fields stored in Airtable:

![image](https://github.com/user-attachments/assets/5f594310-6153-4c0c-a970-d7437a324920)


**3. Method: Automation Workflow**

The following steps are automated using Make:

1. **Trigger (Scheduler):** Run daily to check new listings
2. **Router (Connect):** Connects multiple job sources (via different RSS feeds)   
3. **RSS Feed:** Pull job postings from selected RSS URLs  
4. **Airtable Search (Filter):** Prevent duplicates by checking if a job already exists  
5. **HTTP Request:** Retrieve full job descriptions  
6. **Sleep (Delay):** Add delay to avoid API throttling  
7. **ChatGPT Prompt (1):** Summarize job description with key informations
8. **ChatGPT Prompt (2):** Assess match with candidate profile 
9. **Airtable Create:** Save all results into a job tracker table
10. **Ignore Module:** Skips some iterations to manage OpenAI usage limits  

## Data Visualization

This scenario is visualized in Make as a no-code flow:

![image](https://github.com/user-attachments/assets/5e253265-6e6c-4057-bb53-32827d250bc5)

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
