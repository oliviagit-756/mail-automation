# mail-automation
Send minute-precise emails with a short, original quote on the chosen topic.
Built in Python with MySQL for storage, Gmail SMTP for delivery, and OpenAI for 1-line quotes (with a safe local fallback).

## Features
\n
Exact-minute scheduler: checks every minute and sends at HH:MM in your app timezone. \n
Topic → 1-line quote: calls OpenAI to generate a ≤120-char line; falls back to a local quote bank if the API fails.  \n
Once-per-day protection: prevents duplicate sends for the same reminder on the same day. \n
Simple CLI insert: add a user + reminder via prompts. \n
Timezone aware: set APP_TZ (e.g., Asia/Kolkata) via .env. \n
Gmail SMTP: supports STARTTLS (587) and SSL (465) using a Gmail App Password. \n
\n
## Requirements
\n
Python 3.10+ (for zoneinfo) \n
MySQL 8.x (or compatible) \n
A Gmail account + App Password (not your regular password) \n
OpenAI API key (optional; the app falls back to local quotes if missing) \n

