# Governance & Compliance Protocol

## Overview
This document defines the rules for maintaining the integrity, security, and scalability of the Gemini Multi-Agent System (MAS). **All changes must adhere to these standards.**

## 1. Structural Standards (Folder Organization)
To maintain a clean namespace, roles must be categorized into sub-directories:

*   `roles/core/`: Essential engineering roles (Team Lead, Dev, QA, Analyst).
*   `roles/game/`: Game Development Extension roles.
*   `roles/[extension]/`: Future extensions (e.g., `web`, `mobile`, `data`).

**Rule:** Never place a role file directly in the root of `roles/`. Always use a sub-directory.

## 2. Role Definition Standards (The Template)
Every new role MUST be created using the `_TEMPLATE.md` file as a base.

### Required Frontmatter
*   **Role Name:** Clear, descriptive title.
*   **Model:** The recommended Gemini model (e.g., Gemini 3 Pro Preview).
*   **Trigger:** The command that activates this role (e.g., `x7`, `xGame`).

### Required Sections
*   **Mission:** What is the agent's "Prime Directive"?
*   **Capabilities:** What can it do?
*   **Directives:** 3-5 hard rules it must never break.

## 3. Security Protocols
*   **No Secrets:** Never hardcode API keys, passwords, or tokens in role definitions.
*   **Read-Only Default:** Agents should default to "Research First" before "Execution".
*   **Sandboxing:** Agents should only modify files within the user's workspace context.

## 4. Documentation Compliance
*   **Sync Rule:** If you add a role, you MUST add it to:
    1.  `TECHNICAL_DOC.md` (Technical registry).
    2.  `README.md` (Feature list).
    3.  `SKILL.md` (Orchestration logic).

## 5. Review Process (Manual Linter)
Before committing changes, ask:
1.  Does the file structure match the standard?
2.  Does the role use the correct template?
3.  Is the documentation updated?

*Adherence to these rules ensures the system remains robust without complex automation scripts.*
