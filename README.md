# Multi-Agent Advertisement System

An n8n workflow system for taking a client ad brief through validation,
research, creative direction, copywriting, storyboard approval, and
AI-assisted media production. The project includes the workflow exports, a
Vercel-hosted client console, documentation, examples, and screenshots of the
complete workflow.

The application and its complete screenshot walkthrough live in
[`ai-automation/multi-agent-ads-system/`](ai-automation/multi-agent-ads-system/).
Start with that project's [README](ai-automation/multi-agent-ads-system/README.md),
then follow its [setup guide](ai-automation/multi-agent-ads-system/docs/setup.md)
to import and configure the workflows.

## Workflow at a glance

```text
Client brief
  -> validation and research
  -> creative direction
  -> copy and storyboard approval
  -> production planning
  -> image, video, music, SFX, and voice generation
  -> editing, render checks, and completion response
```

The system uses n8n and Supabase, with optional Vercel serverless routes and
Upstash Redis for the web console and long-running status updates. Workflow
exports must be configured with your own credentials and service accounts.

## Screenshots

See the project's [full screenshot walkthrough](ai-automation/multi-agent-ads-system/README.md#screenshots-complete-workflow), which covers the
orchestration, client approval loops, media generators, editing, and
completion path.