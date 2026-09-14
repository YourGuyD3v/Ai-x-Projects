# AI Job Search Copilot

AI-powered workflow that discovers relevant jobs, normalizes raw listings, checks for duplicates, compares each opportunity against the candidate profile, and delivers a concise shortlist with resume and cover-letter support.

## Overview

AI Job Search Copilot is an automation system designed to reduce the time spent manually researching jobs and filtering irrelevant results.

The workflow combines n8n, Perplexity, Gemini, Google Sheets, and Telegram to automate or assist with:

- web-based job discovery across multiple sources
- extraction and normalization of job details
- duplicate detection and category routing
- candidate-to-job fit scoring and reasoning
- tailored resume and cover-letter content
- final review and reporting via Telegram and stored job logs

The project is designed for semi-automated execution, with a human review loop at the final decision stage.

## Problem

Job searching is repetitive, time-consuming, and noisy. Candidates often face:

- too many irrelevant listings
- duplicate postings across multiple sources
- inconsistent job data across job boards
- difficulty matching postings to personal experience and skills
- manual work to tailor applications and track follow-up

This creates a bottleneck between finding opportunities and deciding which ones are worth pursuing.

## Solution

The workflow:

1. receives a search request from Telegram or another trigger
2. researches current openings using a web search layer
3. extracts and normalizes job metadata into a structured schema
4. detects duplicates and routes jobs into the correct job category
5. evaluates fit using resume and profile context
6. writes new jobs to Google Sheets and prepares application-ready output
7. sends a concise report to Telegram for human review

## Architecture

```text
Telegram / User Request
   ↓
Perplexity Web Search
   ↓
Normalize + Extract Jobs
   ↓
Deduplicate + Classify
   ↓
Candidate Resume / RAG Context
   ↓
AI Agent Match + Fit Scoring
   ↓
Google Sheets Job Log
   ↓
Tailored Resume / Cover Letter
   ↓
Telegram Report + Human Approval
```

## What the workflow produces

Each job is reviewed and stored with fields such as:

- title, company, location, and source
- job URL and application URL
- remote status and employment type
- skills and key requirements
- technical match and experience match
- strengths, skill gaps, and recommendation
- tailored resume bullets or cover-letter draft
- application status and date found

## Typical use case

A user can ask for roles such as:

- AI automation engineer
- n8n workflow automation
- AI agent engineer
- low-code automation specialist
- data or process automation roles

The system will collect active opportunities, filter out weak matches, and return a shortlist that is easier to act on.

## Repository structure

- `workflow/` — sanitized n8n workflow export
- `docs/` — architecture, data model, setup, and testing notes
- `examples/` — sample input and output JSON files
- `screenshots/` — UI and workflow captures
- `demo/` — demo or walkthrough references
- `assets/` — static files and supporting materials

## Notes

This project is intended as a practical AI-assisted job research and triage workflow, not just a raw scraper. The design focuses on quality filtering, better candidate alignment, and clearer human decision-making.
