# Autonomous Lead Prospector & Web Scraper (n8n)

This repository contains the n8n workflow definition for an **Autonomous B2B Lead Generator and Web Scraper**. It watches folders for lead files, scrapes company data, normalizes names, and drafts cold outreach emails.

## Key Technical Features
* **Drive Excel Parser:** Watches folders for incoming Lead Excel spreadsheets, downloads files, and converts xlsx arrays into JSON.
* **Data Loop Batching:** Employs n8n `Split In Batches` to loop through leads and manage API rate-limits.
* **Serper REST API Scraper:** Agent calls Google Serper API to crawl the web for ads running, CRM tools, marketing size, and budget signals.
* **JavaScript JSON Normalization:** Custom JS code normalizes contact names and filters out generic corporate addresses (e.g., support@, info@).
* **Personalized Outreach Writer:** Deploys GPT-4o to write contextual icebreaker email drafts, logging leads directly to Google Sheets.

## Workflows Included
1. `autonomous-lead-prospector-web-scraper.json` (Lead research and email writer engine)

## Deployment Instructions
1. Import `autonomous-lead-prospector-web-scraper.json` into n8n.
2. Configure credentials for Google Drive, Google Sheets, OpenRouter/OpenAI, and Groq.
3. Replace the Serper API Key with your own credential header.
