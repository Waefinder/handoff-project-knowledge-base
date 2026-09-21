---
name: handoff-project-knowledge-base
description: Handoff project knowledge to new team members or sessions.
category: productivity
version: 1.0.0
author: Secretary Kim
license: MIT
tags: [handoff, knowledge-transfer, project-documentation, onboarding]
hermes:
  tags: [handoff, knowledge-transfer, project-documentation, onboarding]
  related_skills: [multi-bot-orchestration, session-librarian]
---

# Handoff: Project Knowledge Base

## Overview
Standardized procedure for handing off project knowledge to new team members, sessions, or bots. Ensures no critical context is lost during transitions.

## When to Use
- New team member joining the project
- Switching between bot sessions
- Transferring work mid-project
- Creating project documentation for first time

## Handoff Checklist

### 1. 📁 Project Structure
- [ ] Document folder hierarchy
- [ ] Identify key files and their purposes
- [ ] Note any auto-generated files vs hand-written
- [ ] List configuration files and their locations

### 2. 🏗️ Architecture Overview
- [ ] System diagram (ASCII or link to visual)
- [ ] Key components and their relationships
- [ ] Data flow description
- [ ] External dependencies/APIs

### 3. 📋 Code Conventions
- [ ] Naming conventions (variables, functions, files)
- [ ] Code style (formatting, linting rules)
- [ ] Comment/documentation standards
- [ ] Testing requirements

### 4. 🔧 Development Setup
- [ ] Prerequisites and dependencies
- [ ] Installation steps
- [ ] Environment variables needed
- [ ] Local development commands

### 5. 🚀 Deployment
- [ ] Build process
- [ ] Deployment targets
- [ ] Environment configurations
- [ ] Rollback procedures

### 6. 📚 Key Documentation
- [ ] README location and contents
- [ ] API documentation
- [ ] User guides
- [ ] Troubleshooting guides

## Handoff Template

```markdown
# Project Handoff: [Project Name]

## Date: [YYYY-MM-DD]
## From: [Previous Owner]
## To: [New Owner]

## Quick Start
1. Clone repo: `git clone [repo-url]`
2. Install deps: `[install command]`
3. Run locally: `[run command]`

## Critical Files
- `src/main.py` - Main application entry
- `config/settings.py` - Configuration
- `tests/` - Test suite

## Known Issues
- [List any current bugs or limitations]

## Next Steps
- [What needs to be done next]

## Contacts
- [Who to ask for help]
```

## Verification Steps

After handoff, verify:
1. ✅ Can access all project files
2. ✅ Can run the project locally
3. ✅ Understands the architecture
4. ✅ Knows where to find documentation
5. ✅ Has necessary credentials/access

## Common Pitfalls

⚠️ **Don't assume knowledge** - Document everything explicitly
⚠️ **Include context** - Not just WHAT but WHY decisions were made
⚠️ **Version control** - Ensure all docs are in repo
⚠️ **Test the handoff** - Have recipient verify they can follow steps

## Tools for Handoff

- `session_search` - Find previous discussions
- `read_file` - Access documentation
- `search_files` - Locate project files
- `skill_view` - Load related skills