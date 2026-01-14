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

Form Submission
↓
Empty Message Filter
↓
AI Spam Checker
↓
Is Spam?
├─ Yes → Spam Sheet (Google Sheets)
└─ No → Genuine Enquiries (Google Sheets)


---

## Files in This Repository

- `n8n-contact-form-ai-spam-filter.json`  
  Exported n8n workflow containing the complete automation logic.

- `README.md`  
  Project documentation.

- `LICENSE`  
  MIT License.

---

## Requirements

To run this workflow, you will need:

- An **n8n instance** (cloud or self-hosted)
- An **AI provider** configured in n8n (e.g. OpenAI)
- A **Google account** with access to Google Sheets
- Google Sheets credentials configured in n8n

---

## Google Sheets Setup

Create a spreadsheet with **two tabs**:

### Genuine Enquiries
Columns:


EMAIL | MESSAGE


### Spam
Columns:


Email | Message


Column names must match exactly to ensure correct mapping.

---

## How to Import and Use the Workflow

1. Open n8n
2. Go to **Workflows**
3. Click **Import**
4. Upload `n8n-contact-form-ai-spam-filter.json`
5. Reconnect credentials:
   - AI provider
   - Google Sheets
6. Activate the workflow
7. Submit test form entries to verify routing

---

## AI Classification Logic

The AI component is configured to evaluate submissions in the context of a **web development agency enquiry form**.

Messages are classified as spam if they:
- Are unrelated to business enquiries
- Contain test or placeholder content
- Use fake or dummy email addresses
- Are promotional, malicious, or irrelevant

The AI returns a strict binary output (`yes` or `no`) to ensure reliable routing logic.

---

## Security Considerations

- No API keys or secrets are stored in this repository
- Credentials are managed securely within n8n
- The workflow is suitable for further hardening using:
  - Webhook secret headers
  - Rate limiting
  - Firewall or proxy rules

---

## Use Cases

- Website contact forms
- Agency lead management
- Spam reduction for enquiry pipelines
- Automation and AI workflow demonstrations
- Portfolio and learning projects

---

## Author

This workflow was designed, implemented, and tested as a hands-on automation project demonstrating practical use of **n8n**, **AI integration**, and **cloud-based data handling**.

---

## License

This project is licensed under the **MIT License**.
