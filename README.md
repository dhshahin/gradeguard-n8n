
# GradeGuard n8n
GradeGuard is an AI-assisted essay grading and feedback workflow built with n8n. It automates the first-pass assessment of written assignments using instructor-defined rubrics, objective writing metrics, and a large language model.

The project is designed to reduce feedback delays while maintaining instructor oversight. The current version is a working prototype, and the next development phase will add confidence-based routing and structured human review.

## Current Workflow

1. A student submits an essay through a custom HTML portal.
2. The submission is sent to an n8n webhook.
3. Required fields, email format, and essay length are validated.
4. The matching assignment rubric is retrieved from Google Sheets.
5. A JavaScript node calculates objective writing metrics.
6. An LLM evaluates the essay against the rubric.
7. The structured result is parsed and validated.
8. Results are logged and feedback is sent to the student.
9. The instructor receives operational alerts through Telegram.
10. A separate global error workflow records unexpected failures.

## Key Features

- Rubric-based essay assessment
- Structured per-criterion scoring
- Automated writing metrics
- Personalised student feedback
- Input validation and rejection handling
- Google Sheets logging
- Email feedback delivery
- Telegram instructor alerts
- Global workflow error handling
- Sanitized and reusable n8n workflow templates

## Repository Structure

```text
gradeguard-n8n/
├── frontend/
│   └── essay-submission-portal.html
├── workflow/
│   ├── README.md
│   ├── gradeguard-main-workflow.template.json
│   └── gradeguard-global-error-handler.template.json
├── .gitignore
├── LICENSE
└── README.md
