# 🤖 AI-Powered HR Recruitment & Resume Screening Workflow

An end-to-end **AI Recruitment Automation System** built with **n8n** that automates candidate intake, resume management, AI-powered resume analysis, applicant tracking, and communication throughout the hiring process.

This workflow demonstrates how modern companies can replace repetitive HR tasks with intelligent automation while maintaining a structured recruitment pipeline.

---

# 🚀 Features

* 📄 Candidate application form
* 🆔 Automatic Candidate ID generation
* 📁 Resume upload and validation (PDF only)
* ☁️ Resume storage in Google Drive
* 📊 Applicant Tracking System (Google Sheets)
* 📄 Resume text extraction
* 🤖 AI-powered resume evaluation
* 🎯 Candidate scoring and recommendation
* ✉️ Automated Interview Invitation emails
* ❌ Automated Rejection emails
* 📢 Slack notifications for shortlisted candidates
* 📈 ATS updates with AI insights
* ⚠️ Built-in error handling and logging

---

# 🏗 Workflow Architecture

```
Candidate Application
        │
        ▼
Generate Candidate ID
        │
        ▼
Validate Resume Upload
        │
        ▼
Upload Resume to Google Drive
        │
        ▼
Create ATS Record (Google Sheets)
        │
        ▼
Download Resume
        │
        ▼
Extract Resume Text
        │
        ▼
AI Resume Analysis
        │
        ▼
Candidate Score Decision
      /           \
     /             \
Shortlisted      Rejected
     │               │
     ▼               ▼
Interview Email   Rejection Email
     │
     ▼
Update ATS
     │
     ▼
Slack Notification
```

---

# 🧠 AI Capabilities

The workflow leverages an AI model to analyze resumes and generate:

* Candidate Score (0–100)
* Resume Summary
* Technical Strengths
* Weaknesses
* Hiring Recommendation
* Suggested Recruitment Stage

This allows recruiters to review AI-assisted evaluations instead of manually screening every resume.

---

# ⚙️ Technologies Used

* n8n
* Google Drive API
* Google Sheets API
* Gmail API
* Slack API
* AI/LLM Integration
* JavaScript (n8n Code Nodes)

---

# 📋 Workflow Steps

## 1. Candidate Application

Candidates submit:

* Full Name
* Email
* Phone Number
* LinkedIn Profile
* Portfolio Website
* Resume (PDF)

---

## 2. Candidate ID Generation

A unique Candidate ID is automatically generated.

Example:

```
CAND-1720138492038-john-doe
```

---

## 3. Resume Validation

The workflow verifies:

* Resume exists
* PDF format only
* Proper binary formatting

Invalid uploads are rejected immediately.

---

## 4. Resume Storage

Uploaded resumes are stored in Google Drive using standardized filenames:

```
<Candidate-ID>-resume.pdf
```

---

## 5. ATS Record Creation

Candidate information is automatically stored inside Google Sheets.

Stored fields include:

* Candidate ID
* Contact Information
* Resume Link
* Application Date
* Current Stage

---

## 6. Resume Text Extraction

The PDF resume is downloaded from Google Drive and converted into plain text for AI processing.

---

## 7. AI Resume Analysis

The AI evaluates the candidate and returns:

* Resume Score
* Summary
* Technical Skills
* Strengths
* Weaknesses
* Hiring Recommendation

---

## 8. Candidate Decision

Candidates are automatically routed based on their AI score.

Example logic:

```
Score > 70
      │
      ├── Shortlist Candidate
      │
      └── Send Interview Invitation

Score ≤ 70
      │
      └── Send Rejection Email
```

---

## 9. Automated Candidate Communication

### Shortlisted Candidates

Receive:

* Personalized Interview Invitation
* AI Assessment Summary
* Candidate Reference ID

### Rejected Candidates

Receive:

* Professional rejection email
* Appreciation message
* Candidate Reference ID

---

## 10. ATS Update

The workflow updates Google Sheets with:

* AI Score
* Resume Summary
* Strengths
* Weaknesses
* Recommended Stage

Recruiters always have an up-to-date hiring dashboard.

---

## 11. Slack Notifications

When a candidate is shortlisted, HR receives an instant Slack notification containing:

* Candidate Name
* Email
* Score
* Resume Link
* AI Summary
* Candidate ID

---

## 12. Error Handling

A dedicated error workflow captures failures and:

* Logs errors to Google Sheets
* Sends email alerts to HR
* Records execution details for debugging

This ensures workflow reliability and easier maintenance.

---

# 📊 Business Benefits

* Eliminates repetitive HR tasks
* Accelerates resume screening
* Reduces manual data entry
* Standardizes candidate evaluations
* Improves hiring consistency
* Provides instant recruiter notifications
* Creates a centralized Applicant Tracking System

---

# 🔮 Future Improvements

* Interview scheduling automation
* Calendar integration
* Multi-stage hiring pipeline
* AI-generated interview questions
* Candidate chatbot
* Technical assessment automation
* Hiring analytics dashboard
* Integration with LinkedIn Jobs
* Multi-language support

---

# 📂 Repository Structure

```
HR-Team-Hiring-Workflow/
│
├── README.md
├── workflow.json
├── screenshots/
│   ├── workflow-overview.png
│   ├── ai-analysis.png
│   └── slack-alert.png
└── docs/
    └── architecture.md
```

---

# 🎯 Use Cases

* HR Automation
* Resume Screening
* Applicant Tracking Systems
* AI Recruitment
* Talent Acquisition
* Recruitment Operations
* Hiring Automation
* Business Process Automation

---

# 📜 License

This project is released under the MIT License.

---

# 👤 Author

**AI Automation Engineer**

Building intelligent workflow automation using AI, APIs, and low-code platforms to streamline business operations and increase productivity.

