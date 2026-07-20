# Automated Daily Tech News Briefing

An end-to-end automation workflow built with **n8n**, **Airtable**, and **Gmail** that collects subscribers through a form and automatically delivers a personalized tech news briefing every morning at **8:00 AM**.

## Overview

This project automates the entire newsletter process—from subscriber registration to daily email delivery—without requiring any manual intervention.

### Features

* 📋 Collect subscribers through an n8n-hosted form
* 🗄️ Store subscriber information in Airtable
* 📰 Fetch the latest technology news from an RSS feed
* ✉️ Generate personalized HTML newsletters
* 📧 Send emails using the Gmail API
* 📅 Track the last email sent for each subscriber
* ⏰ Fully automated daily execution at 8:00 AM

---

## Workflow Architecture

```text
Subscriber Signup

[n8n Form]
      │
      ▼
[Airtable]


Daily Newsletter (8:00 AM)

[Schedule Trigger]
        │
        ▼
[Search Subscribers]
        │
        ▼
[RSS Read]
        │
        ▼
[Code Node]
        │
        ▼
[Send Email (Gmail)]
        │
        ▼
[Update Airtable]
```

---

## Tech Stack

* **n8n** – Workflow automation
* **Airtable** – Subscriber database
* **Gmail API** – Email delivery
* **RSS Feed** – News source
* **JavaScript** – HTML email generation and data processing

---

## Project Structure

```text
.
├── workflow.json          # Exported n8n workflow
├── README.md
└── screenshots/
    ├── workflow.png
    ├── signup-form.png
    └── sample-email.png
```

---

## How It Works

### 1. Subscriber Registration

Visitors submit their name and email through an n8n form.

The workflow automatically creates a new subscriber record in Airtable.

---

### 2. Daily Automation

Every day at **8:00 AM**, the workflow:

1. Retrieves all subscribers from Airtable.
2. Fetches the latest articles from an RSS feed.
3. Formats the news into a responsive HTML email.
4. Personalizes each email using the subscriber's name.
5. Sends the newsletter through Gmail.
6. Updates Airtable with the latest delivery date.

---

## Airtable Fields

| Field           | Description                        |
| --------------- | ---------------------------------- |
| Name            | Subscriber's name                  |
| Email           | Subscriber's email address         |
| Last Email Sent | Date of the most recent newsletter |

---

## Setup

### Prerequisites

* n8n
* Airtable account
* Gmail account
* Google OAuth credentials
* RSS feed URL

### Installation

1. Clone this repository.

```bash
git clone https://github.com/yourusername/daily-tech-news-automation.git
```

2. Import the `workflow.json` file into n8n.

3. Configure your credentials:

   * Airtable
   * Gmail OAuth

4. Update the Airtable Base ID and Table.

5. Replace the RSS feed URL if desired.

6. Activate the workflow.

---

## Possible Improvements

* Support multiple news categories
* Allow subscribers to choose their interests
* Add unsubscribe functionality
* Track email opens and clicks
* Send weekly or monthly digests
* Integrate AI-generated news summaries
* Store email logs for analytics

---

## Contributing

Contributions, suggestions, and improvements are welcome.

Feel free to fork the repository, submit issues, or open a pull request.

---

## Subscribe

Want to receive the daily tech news briefing?

**Subscription Form:** *http://localhost:5678/form/678e897e-1968-4bcf-9c19-350dfafc389c*

---

# Daily-News-Briefing
An automated, end-to-end news newsletter pipeline built with n8n, Airtable, and Gmail. Automatically captures subscriber signups via webform, aggregates daily RSS updates, and dispatches personalised email briefings.
