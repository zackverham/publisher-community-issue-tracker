# Posit Publisher — Community Issue Tracker

A Quarto report that tracks community-filed issues on [posit-dev/publisher](https://github.com/posit-dev/publisher), providing visibility into response times, stale issues, and overall engagement.

## What the report covers

- **Summary dashboard** — open/closed counts, new issues this week, median response time
- **New issues this week** — community-labeled issues from the last 7 days
- **Response time tracking** — bar chart of time-to-first-team-response per issue, measured against a 24-hour target
- **Close-the-loop audit** — open issues with linked PRs that may be ready to close, plus stale issues with no recent activity
- **Full issue list** — every community-labeled issue with status, author, and assignee

## Setup

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Rendering the report

Set a `GITHUB_TOKEN` environment variable (optional but recommended to avoid rate limits), then render with Quarto:

```bash
export GITHUB_TOKEN="ghp_..."
quarto render report.qmd
```

This produces a self-contained `report.html`.
