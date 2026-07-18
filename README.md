# AI Lead Qualification & CRM Automation

Automatically qualify incoming leads using AI, store them in Supabase CRM, notify the sales team about high-value opportunities, and return structured API responses.

---

# Overview

This workflow demonstrates a complete AI-powered lead qualification pipeline.

Instead of manually reviewing every inquiry, the workflow automatically:

- Receives new leads via Webhook
- Uses Gemini AI to extract structured information
- Validates extracted data
- Calculates lead quality
- Routes leads based on score
- Stores all leads in Supabase
- Sends Telegram alerts for high-priority leads
- Sends email notifications
- Returns JSON API responses

---

# Business Problem

Sales teams receive many inquiries every day.

Manually reviewing every lead wastes time and delays responses.

This automation instantly identifies valuable leads and alerts the team only when immediate attention is required.

---

# Solution

Incoming Lead

↓

Webhook

↓

Gemini AI

↓

Parse JSON

↓

Validate Lead

↓

Lead Score

↓

Switch

├── High Priority
│      ↓
│   Save to Supabase
│      ↓
│   Telegram Alert
│      ↓
│   Gmail Notification
│      ↓
│   Respond to Webhook
│
├── Medium Priority
│      ↓
│   Save to Supabase
│      ↓
│   Respond to Webhook
│
└── Low Priority
       ↓
    Save to Supabase
       ↓
    Respond to Webhook

---

# Technologies

- n8n
- Google Gemini API
- Supabase
- Gmail API
- Telegram Bot API
- JavaScript
- REST API
- JSON
- Webhooks

---

# Features

- AI lead extraction
- Automatic lead validation
- Lead scoring
- Priority routing
- CRM integration
- Telegram notifications
- Gmail notifications
- JSON API responses
- Error handling

---

# Workflow

## 1. Receive Lead

Webhook receives lead information.

---

## 2. AI Processing

Gemini extracts:

- Name
- Email
- Company
- Job Title
- Employees
- Budget
- Business Need
- Timeline
- Lead Score

---

## 3. Validation

JavaScript validates required fields before processing.

---

## 4. Lead Routing

High Priority (80+)

- Save to CRM
- Telegram notification
- Email notification

Medium Priority (50–79)

- Save to CRM

Low Priority (<50)

- Save to CRM

---

## 5. CRM Storage

All leads are stored in Supabase for future tracking.

---

# Screenshots

## Complete Workflow

![Workflow](screenshots/01-workflow4.png)

---

## Webhook Test

![Webhook](screenshots/02-testrequest.png)

---

## Supabase Database

![Supabase](screenshots/05-supabase.png)

---

## Telegram Notification

![Telegram](screenshots/06-telegram.png)

---

# API Response Example

```json
{
  "success": true,
  "priority": "High",
  "lead_score": 85,
  "message": "High priority lead has been saved. Sales team has been notified.",
  "company": "Swift Logistics",
  "contact": "John Smith"
}
```

---

# Skills Demonstrated

- AI Automation
- Workflow Design
- API Integration
- Prompt Engineering
- Data Validation
- CRM Automation
- Database Integration
- Business Process Automation
- JavaScript
- REST APIs

---

# Author

Built by Bek Sultan as part of an AI Automation Engineer portfolio.
