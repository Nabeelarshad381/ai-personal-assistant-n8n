# AI-Driven Personal Assistant with n8n

## Overview

This project demonstrates an Autonomous AI Agent built with n8n that can understand natural language instructions, select the appropriate tool, execute tasks across multiple Google services, and provide real-time WhatsApp notifications using SyncMate.

Unlike traditional rule-based automation, this workflow leverages Large Language Models (LLMs) to make decisions dynamically and automate tasks intelligently.

---

## Features

* Natural language task execution
* AI Agent powered by Gemini, OpenAI, and Groq models
* Google Tasks integration
* Google Sheets data processing
* Gmail email summarization
* Google Docs updates and note management
* Calculator-based expense calculations
* WhatsApp notifications via SyncMate
* Context-aware conversations using Window Buffer Memory

---

## Workflow Architecture

### Intelligence Layer

#### Webhook Trigger

Receives user prompts and starts the workflow.

#### AI Agent (LangChain)

Interprets user intent and determines which tool should be used to fulfill the request.

#### Window Buffer Memory

Provides short-term memory, enabling context-aware interactions and a more personalized assistant experience.

---

## Integrated Tools

### Google Tasks

* Create new tasks
* Manage to-do lists
* Set deadlines and reminders

### Google Sheets

* Read spreadsheet data
* Calculate expenses
* Append new records

### Gmail

* Access latest emails
* Generate AI-powered summaries

### Google Docs

* Store notes and logs
* Update documents automatically

### Calculator

* Perform accurate mathematical calculations
* Verify financial totals

### SyncMate (WhatsApp Notifications)

* Send instant notifications after task completion
* Deliver summaries and confirmations directly to users

---

## Use Cases

### 1. Task Management

User Prompt:

> Create a task called "Schedule a meeting for tomorrow"

Result:

* AI creates the task in Google Tasks
* WhatsApp confirmation is sent via SyncMate

### 2. Expense Calculation

User Prompt:

> Calculate the total expenses from Google Sheets

Result:

* Reads expense data
* Calculates total using Calculator Tool
* Sends result to WhatsApp

### 3. Google Docs Updates

User Prompt:

> Update the notes document with the latest expense total

Result:

* Retrieves calculated amount
* Updates Google Docs automatically
* Sends confirmation message

### 4. Gmail Summarization

User Prompt:

> Summarize my latest email

Result:

* Retrieves latest email
* Generates concise summary using AI
* Delivers summary through WhatsApp

---

## Challenges & Solutions

### OAuth2 Configuration Issue

Problem:
redirect_uri_mismatch error during Google authentication.

Solution:
Added the following callback URL in Google Cloud Console:

http://localhost:5678/rest/oauth2-credential/callback

### WhatsApp Integration

Instead of Twilio, SyncMate was selected because it offered a simpler and more direct solution for WhatsApp notifications during development and testing.

---

## Why n8n Instead of Selenium?

### Reliability

Selenium workflows often break when website interfaces change.

n8n relies on APIs, making integrations more stable and maintainable.

### Efficiency

Connecting multiple services through Selenium would require extensive custom coding.

n8n enables visual workflow orchestration with significantly less development effort.

### Scalability

API-first automation scales more effectively and is easier to maintain in production environments.

---

## Technologies Used

* n8n
* LangChain
* Google Gemini
* OpenAI
* Groq
* Google Tasks API
* Google Sheets API
* Gmail API
* Google Docs API
* SyncMate WhatsApp Integration

---

## Results

The project successfully demonstrates how AI agents can autonomously understand, reason, and execute tasks across multiple services while maintaining context and providing real-time user feedback.

By combining AI reasoning, workflow automation, and WhatsApp communication, this solution represents a practical implementation of Agentic AI and intelligent business automation.

---

## Author

Muhammad Nabeel Arshad

University of Central Punjab

Course: Tools & Techniques for Data Science
