# Observable Job Agent Diagrams

Architecture diagrams and visual documentation for the Observable Job Agent.

## Diagram

- [Open the Job Scout overview (HTML)](https://file+.vscode-resource.vscode-cdn.net/d%3A/AI%20Job/Job_agent_archify_diagram/diagrams/job-scout-overview.html)
- [View the diagram data (JSON)](https://file+.vscode-resource.vscode-cdn.net/d%3A/AI%20Job/Job_agent_archify_diagram/diagrams/job-scout-overview.delivery.json)

To open the interactive diagram after cloning the repo:

```powershell
git clone --recurse-submodules https://github.com/tech-believer/Job_agent_archify_diagram.git

cd Job_agent_archify_diagram

start .\diagrams\job-scout-overview.html
```

If you want to open the same page directly from a local file URL, use:

```powershell
start "" "file:///D:/AI%20Job/Job_agent_archify_diagram/diagrams/job-scout-overview.html#focus=profile"
```

The HTML diagram is interactive. To display a static preview directly in this README, add a PNG or SVG export under `diagrams/` and link it with Markdown image syntax.

## Project relationship

The application is linked in `observable-job-agent/` as a Git submodule pointing to [`tech-believer/Job_agent_open_src`](https://github.com/tech-believer/Job_agent_open_src). This keeps the application source in its own repository; this repository stores the diagrams and records the exact application commit it references.

Clone this repository with its submodule:

```powershell
git clone --recurse-submodules https://github.com/tech-believer/Job_agent_archify_diagram.git
cd Job_agent_archify_diagram/observable-job-agent
```

## Test and run on Windows

Requires Python 3.12 and [uv](https://docs.astral.sh/uv/).

```powershell
uv sync --all-groups
uv run pytest
```

My test run completed with **229 passed, 1 skipped, 1 warning**. `make` was unavailable in my Windows environment, so I used `uv` directly.

To launch the application, create `.env`, add an LLM API key, and run:

```powershell
Copy-Item .env.example .env
uv run python -m job_scout.app
```
