# handoff-project-knowledge-base

Hermes Agent skill for handing off project knowledge to new team members or sessions.

## Overview

Standardized procedure for handing off project knowledge to new team members, sessions, or bots. Ensures no critical context is lost during transitions.

## Features

- **Handoff Checklist** — 6 sections covering project structure, architecture, code conventions, dev setup, deployment, and documentation
- **Handoff Template** — Ready-to-use markdown template for knowledge transfer
- **Verification Steps** — 5-point checklist to confirm successful handoff
- **Common Pitfalls** — Tips to avoid knowledge loss
- **Tools for Handoff** — Related Hermes tools

## Installation

1. Copy `handoff-project-knowledge-base/` to your Hermes skills directory:
   ```
   ~/.hermes/profiles/<your-profile>/skills/productivity/
   ```

2. Restart Hermes or reload skills.

## Usage

Load the skill in your Hermes session:
```python
skill_view(name="handoff-project-knowledge-base")
```

## License

MIT
