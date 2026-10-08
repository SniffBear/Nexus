---
name: web-design-guidelines
description: Review UI code for Web Interface Guidelines compliance.
metadata:
  author: vercel
  version: "1.0.0"
---

# Web Interface Guidelines

Review specified UI files against the latest Vercel Web Interface Guidelines.

Before each review, fetch:
https://raw.githubusercontent.com/vercel-labs/web-interface-guidelines/main/command.md

Then read the specified files, apply every current rule, and output concise findings grouped by file using file:line format. Report ✓ pass when a file has no findings.

This skill is the final accessibility and web-interface audit for Nexus.
