# N8N-Automations

## Overview
A curated collection of 195 n8n workflow templates (JSON files) sourced from the internet, organized into 9 categories. This is a template library, not an application — there is no build system, runtime, or tests.

## Repository Structure
```
├── AI_Research_RAG_and_Data_Analysis/   (38 workflows)
├── Database_and_Storage/                (5 workflows)
├── Discord/                             (3 workflows)
├── Gmail_and_Email_Automation/          (20 workflows)
├── Google_Drive_and_Google_Sheets/      (17 workflows)
├── Instagram_Twitter_Social_Media/      (10 workflows)
├── OpenAI_and_LLMs/                     (81 workflows)
├── PDF_and_Document_Processing/         (17 workflows)
├── WhatsApp/                            (4 workflows)
└── README.md                            (catalog with descriptions and links)
```

## Workflow JSON Format
Each `.json` file is an n8n workflow export containing:
- `meta` — instance metadata
- `nodes` — array of workflow nodes (triggers, AI models, tools, actions)
- `connections` — wiring between nodes
- `pinData` — pinned test data (if any)

Nodes reference credentials by ID (e.g., `openAiApi`, `serpApi`) which are instance-specific and won't work without reconfiguration.

## Conventions
- File names match the workflow title (spaces and special characters included)
- Categories are top-level directories with underscores replacing spaces
- README.md contains a markdown table per category with title, description, department, and GitHub link
- No `.gitignore`, no license file, no CI/CD

## Working with This Repo
- To add a workflow: export from n8n as JSON, place in the appropriate category folder, and add an entry to README.md
- To review: validate JSON structure, check for hardcoded secrets or credentials leaking beyond ID references
- All templates are third-party — none are authored by the repo owner
