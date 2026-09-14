# Data Model

## Core entities

### Job

A job record contains the raw and evaluated job information used by the workflow.

Key fields:

- `title`
- `company`
- `location`
- `source`
- `url`
- `application_url`
- `remote_status`
- `employment_type`
- `salary`
- `posted_at`
- `description`
- `key_requirements`
- `skills`
- `category`
- `storage_sheet`
- `initial_relevance`
- `technical_match`
- `experience_match`
- `overall_match`
- `strengths`
- `skill_gaps`
- `recommendation`
- `tailored_resume`
- `cover_letter_proposal`
- `application_status`
- `date_found`
- `is_new`

### Candidate profile

The candidate profile includes:

- resume context
- skills and strengths
- role preferences
- geographic and work constraints
- experience level

### Job log row

Each row in the job log stores:

- the job record
- category routing
- date found
- recommendation state
- human-review output
