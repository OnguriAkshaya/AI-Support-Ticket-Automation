# AI Support Ticket Automation

An AI-powered support ticket automation system built using n8n, Google Gemini, Google Sheets, and email automation.

## 📌 Project Overview

This project automates the process of receiving, analyzing, tracking, and responding to IT support tickets.

A user submits a support issue through a form. The workflow automatically sends the ticket to Google Gemini for analysis, generates a professional support response, stores the ticket and response in Google Sheets, and sends the response to the user by email.

## 🔄 Workflow

The automation follows these steps:

1. **Support Ticket Form**
   - User submits an IT support issue through the n8n form.

2. **Edit Fields**
   - The submitted ticket is mapped into a clean `ticket_text` field.

3. **Wait**
   - The workflow waits for the configured time interval before continuing.

4. **Google Gemini AI**
   - Gemini analyzes the support ticket.
   - It identifies the priority and issue.
   - It generates troubleshooting steps and a professional response.

5. **Google Sheets**
   - The ticket, AI-generated response, and status are recorded in Google Sheets.

6. **Email Response**
   - The generated support response is automatically sent to the user by email.

## 🧠 AI Processing

Google Gemini is used to analyze incoming support tickets and generate helpful responses.

Example ticket:

> My VPN keeps disconnecting every 5 minutes while I'm working from home. I can't access the company network and I have a deadline today.

The AI analyzes the issue and produces a structured response containing:

- Priority
- Issue summary
- Suggested troubleshooting steps
- Professional email response

## 🛠️ Technologies Used

- n8n
- Google Gemini
- Google Sheets
- SMTP / Email
- JavaScript
- Automation workflows

## 📊 Data Tracking

Each support ticket is stored in Google Sheets along with:

| Field | Description |
|---|---|
| Ticket | Original support request |
| Gemini Response | AI-generated support response |
| Status | Current ticket status |

## 📧 Automated Email

After the AI generates the response, n8n automatically sends the response through email.

This removes the need to manually read every ticket and prepare an individual response.

## 🎯 Benefits

- Automated ticket processing
- AI-assisted troubleshooting
- Centralized ticket tracking
- Automated email responses
- Reduced manual support work
- Consistent response format

## 📸 Screenshots

Screenshots demonstrating the workflow and its output are included in this repository.

## 🚀 How It Works

```text
User
  ↓
Support Ticket Form
  ↓
Edit Fields
  ↓
Wait
  ↓
Google Gemini
  ↓
Google Sheets
  ↓
Email Response
