# Company Jobs Finder

<img src="icon.png" width="96" height="96" alt="Company Jobs Finder icon">

Open jobs at the companies you name, read straight from their public careers boards, ranked for your profile with a resume checklist per job. Hosted and keyless.

Company Jobs Finder reads open roles from the public careers boards that companies publish on Greenhouse, Lever, Ashby, Workable and SmartRecruiters, filters them by keyword, location, remote, department, posting date or published salary, ranks the jobs at up to 3 companies for a person's profile, gives the facts of one job with a checklist for tailoring a resume, and compares recruiter keywords with a profile, headline or resume.

This repository holds the listing and install docs for a hosted MCP server run by OpenKrill.
The server source is not in this repository.
The server is free to call, needs no API key and no sign-up, and is read-only.

- MCP endpoint (Streamable HTTP): `https://jobs.openkrill.app/mcp`
- Web page: https://tools.openkrill.app/answers/company-jobs
- All OpenKrill tools: https://tools.openkrill.app
- Contact: support@openkrill.app

## Install

Any MCP client that supports remote Streamable HTTP servers can connect to `https://jobs.openkrill.app/mcp`.

Generic `mcpServers` config:

```json
{
  "mcpServers": {
    "openkrill-company-jobs": {
      "type": "streamable-http",
      "url": "https://jobs.openkrill.app/mcp"
    }
  }
}
```

Claude Code:

```bash
claude mcp add --transport http openkrill-company-jobs https://jobs.openkrill.app/mcp
```

Cline:

```bash
cline mcp install openkrill-company-jobs --transport http https://jobs.openkrill.app/mcp
```

LobeHub: open the listing on https://lobehub.com/mcp and use its install button, or add a custom MCP plugin of type Streamable HTTP with the URL above.

## Try it

- Remote backend jobs at Ramp and Linear
- Which of these Stripe jobs fit a senior data engineer?
- Does my LinkedIn headline have the right keywords for product design jobs?

## Tools

| Tool | What it does |
| --- | --- |
| `find_company_jobs` | Find open jobs at specific companies. |
| `rank_jobs_for_profile` | Rank the open jobs at up to 3 companies for a person's profile. |
| `job_fit_brief` | Get the facts of one job and a checklist for tailoring a resume to it. |
| `profile_keyword_check` | Compare recruiter keywords and LinkedIn search words with profile text, headline, About or resume. |
| `submit_feedback` | Send feedback to the maintainers about a missing tool, broken links, a bug, or stale data. |
| `get_feedback_reply` | Read the feedback reply for a ticket from submit_feedback. |
| `index_tools` | LinkedIn recruiter jobs feedback broken links: search openkrill MCP tools by task. |

`submit_feedback` and `get_feedback_reply` send a note to the maintainers and read the reply.
`index_tools` finds the right OpenKrill tool for a task.

## Data and privacy

The server reads public sources only and returns the source and date with each answer.
See https://tools.openkrill.app/privacy and https://tools.openkrill.app/terms.
