---
name: web-design-guidelines
description: Review UI code for Web Interface Guidelines compliance. Use when asked to review UI, check accessibility, audit design, review UX, or check a site against best practices.
metadata:
  author: vercel
  version: "1.0.0"
  argument-hint: <file-or-pattern>
---

# Web Interface Guidelines

Review files for compliance with the latest Vercel Web Interface Guidelines.

Before each review, fetch:
https://raw.githubusercontent.com/vercel-labs/web-interface-guidelines/main/command.md

Then:
1. Read the specified files.
2. Apply all current rules.
3. Output concise findings grouped by file using file:line.
4. Include exact issue + location and skip explanations unless a fix is non-obvious.
5. If the UI passes, output ✓ pass for the file.

Key areas include accessibility, focus states, forms, reduced motion, typography, content handling, images, performance, navigation/state, touch interaction, safe areas, dark mode, locale/i18n, hydration safety, hover states, and semantic HTML.

Never substitute stale local rules for the fetched source.
