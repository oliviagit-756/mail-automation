# mail-automation
Send minute-precise emails with a short, original quote on the chosen topic.
Built in Python with MySQL for storage, Gmail SMTP for delivery, and OpenAI for 1-line quotes (with a safe local fallback).

## Features

Exact-minute scheduler: checks every minute and sends at HH:MM in your app timezone.
Topic → 1-line quote: calls OpenAI to generate a ≤120-char line; falls back to a local quote bank if the API fails.
Once-per-day protection: prevents duplicate sends for the same reminder on the same day.
Simple CLI insert: add a user + reminder via prompts.
Timezone aware: set APP_TZ (e.g., Asia/Kolkata) via .env.
Gmail SMTP: supports STARTTLS (587) and SSL (465) using a Gmail App Password.

## Requirements

Python 3.10+ (for zoneinfo)
MySQL 8.x (or compatible)
A Gmail account + App Password (not your regular password)
OpenAI API key (optional; the app falls back to local quotes if missing)

