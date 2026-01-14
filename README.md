# n8n Contact Form AI Spam Filter

This repository contains a **fully implemented n8n automation workflow** designed to filter website contact form submissions using **AI-powered spam detection** and automatically store results in **Google Sheets**.

The workflow was **designed, configured, tested, and documented end-to-end** as a practical automation project for handling real-world lead generation challenges.

---

## Project Overview

Website contact forms are a common target for spam, test submissions, and low-quality messages.  
This workflow solves that problem by automatically:

- Validating incoming form submissions
- Detecting spam using AI
- Separating spam from genuine enquiries
- Persisting results in structured Google Sheets

The result is a clean, automated lead intake system that reduces manual review and improves operational efficiency.

---

## What This Workflow Does

1. Receives contact form submissions
2. Filters out empty or invalid messages
3. Analyses message content using an AI model
4. Classifies each submission as **Spam** or **Genuine**
5. Routes spam messages to a dedicated spam sheet
6. Stores genuine enquiries separately for follow-up

---

## Workflow Logic

