# muladigest

Optimized Daily Email Digest Script for Google Apps Script

---

## Overview

This repo provides a modular, production-ready Google Apps Script for generating daily email digests using OpenAI and Pinecone. It includes:
- Full source code for the digest script (see `muldadigest.js`)
- Workflow automation files: `@create-prd.mdc`, `@generate-tasks.mdc`, `@process-task-list.mdc`
- Setup instructions and configuration tips

## Features
- Modular architecture (config, logging, error handling, OpenAI, Pinecone, email, etc.)
- Robust error handling and retry logic
- Categorizes threads (meetings, support, partners)
- HTML email output with clean styling
- Easily extensible for your own use cases

## Requirements
- Google Apps Script environment (Gmail, MailApp, PropertiesService, etc.)
- OpenAI API key
- (Optional) Pinecone API key for historical context

## Setup
1. Copy `muldadigest.js` into your Google Apps Script project.
2. Run `SETUP_DAILY_SUMMARY_SCRIPT_PROPERTIES()` to initialize required script properties.
3. Update the script properties with your actual API keys and email recipient.
4. Set up a daily time-based trigger to run `sendDailyEmailSummary`.

## Workflow Automation
This repo also includes `.mdc` files for structured AI-driven development:
- `@create-prd.mdc`: Generate a Product Requirement Document
- `@generate-tasks.mdc`: Break down PRD into tasks
- `@process-task-list.mdc`: Guide the AI through implementation, one task at a time

## License
Apache-2.0

---

For more details, see the comments in `muldadigest.js` and the original workflow inspiration at [lorenzlk/ai-dev-tasks](https://github.com/lorenzlk/ai-dev-tasks).

---

## Quickstart Example

1. Open Google Apps Script (https://script.google.com/).
2. Create a new project and copy `muldadigest.js` into the script editor.
3. Run `SETUP_DAILY_SUMMARY_SCRIPT_PROPERTIES()` to initialize properties.
4. Update the script properties with your API keys and recipient email.
5. Set a daily trigger for `sendDailyEmailSummary`.
6. Check your inbox for the daily digest!

---

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for bug fixes, improvements, or new features. For major changes, please discuss them in an issue first.

---

## Code of Conduct

This project follows the [Contributor Covenant](https://www.contributor-covenant.org/) Code of Conduct. By participating, you are expected to uphold this code.

---

## Contact

For questions, suggestions, or support, open an issue or contact the maintainer at [your.email@example.com].

---

## Project Structure

- `muldadigest.js` — Main Google Apps Script for the daily digest
- `create-prd.mdc` — AI workflow: create Product Requirement Document
- `generate-tasks.mdc` — AI workflow: generate implementation tasks from PRD
- `process-task-list.mdc` — AI workflow: stepwise task processing
- `.gitignore` — Standard ignore file for node, env, and editor junk
- `.editorconfig` — Coding style consistency across editors
- `.markdownlint.jsonc` — Markdown linting rules
- `LICENSE` — Apache-2.0 license
- `CONTRIBUTING.md` — Contribution guidelines
- `CODE_OF_CONDUCT.md` — Community standards
- `SECURITY.md` — Security policy and reporting
