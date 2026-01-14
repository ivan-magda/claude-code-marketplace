# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Claude Code plugin marketplace ("claude-superpowers") containing plugins that extend Claude Code with specialized capabilities. Currently includes the **swift** plugin for Swift development tooling.

## Repository Structure

```
.claude-plugin/marketplace.json     # Marketplace metadata (plugins listed here)
plugins/
  swift/
    .claude-plugin/plugin.json      # Plugin metadata
    README.md                       # Plugin documentation
    skills/                         # AI skills (SKILL.md files)
.claude/skills/                     # Marketplace-level skills
.github/workflows/validate-plugins.yml  # CI validation
```
