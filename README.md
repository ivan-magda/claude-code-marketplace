# Claude Superpowers

A personally curated collection of Claude Code plugins, skills, and development tools. This repository extends Claude Code with specialized capabilities for Swift development, code migration, and AI-assisted workflows.

[![GitHub stars](https://img.shields.io/github/stars/ivan-magda/claude-superpowers?style=social)](https://github.com/ivan-magda/claude-superpowers/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/ivan-magda/claude-superpowers?style=social)](https://github.com/ivan-magda/claude-superpowers/network/members)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Validate Plugins](https://github.com/ivan-magda/claude-superpowers/actions/workflows/validate-plugins.yml/badge.svg)](https://github.com/ivan-magda/claude-superpowers/actions/workflows/validate-plugins.yml)

## What This Repository Provides

This is not a community marketplace — it's a focused, maintained collection of plugins I use and develop for my own Claude Code workflows. Each plugin is validated through automated CI/CD and follows Claude Code plugin best practices.

**Current focus areas:**

- Swift 6 migration and concurrency tools
- Code modernization workflows
- Developer productivity skills

## Available Plugins

### Swift Plugin

Comprehensive Swift programming utilities for Claude Code, specializing in Swift 6 migration and concurrency adoption.

**Capabilities:**

- Swift 6 migration guidance with step-by-step concurrency adoption
- Data race safety detection and automated fix suggestions
- Sendable conformance analysis and implementation support
- Complete concurrency checking mode configuration
- Incremental migration strategies for large codebases

**Triggers automatically when:**

- Migrating Swift code to Swift 6
- Fixing data race safety issues
- Adopting async/await and actors
- Resolving Sendable conformance warnings

**Version:** 1.0.2

**Documentation:** [Swift Plugin Details](plugins/swift/README.md)

## Installation

### Prerequisites

- Claude Code installed and configured
- Git for repository access

### Quick Start

Add this plugin collection to Claude Code:

```
/plugin marketplace add ivan-magda/claude-superpowers
```

Install the Swift plugin:

```
/plugin install swift@claude-superpowers
```

Verify installation:

```
/plugin list
```

### Local Development Setup

Clone and test locally:

```bash
git clone https://github.com/ivan-magda/claude-superpowers.git
cd claude-superpowers
```

Add as local marketplace:

```
/plugin marketplace add ./
```

Install from local source:

```
/plugin install swift@claude-superpowers
```

## Usage Examples

Plugins activate automatically based on context. The Swift 6 migration skill engages when Claude Code detects relevant tasks.

**Swift migration prompts:**

```
Help me migrate this Swift code to Swift 6
```

```
Check this code for Swift 6 concurrency issues
```

```
Fix the Sendable conformance warnings in this file
```

```
Enable strict concurrency checking for this target
```

## Repository Structure

```
claude-superpowers/
├── .claude-plugin/
│   └── marketplace.json      # Plugin registry
├── plugins/
│   └── swift/
│       ├── .claude-plugin/
│       │   └── plugin.json   # Plugin metadata
│       ├── skills/
│       │   └── swift-6-migration/
│       │       ├── SKILL.md          # Skill definition
│       │       └── migration-guide.md # Reference docs
│       └── README.md
└── .github/
    └── workflows/
        └── validate-plugins.yml      # CI validation
```

## Validation

All plugins are validated on every push and pull request:

- JSON schema validation for plugin manifests
- Required field verification
- Duplicate name detection

## Roadmap

Planned additions to this collection:

- Additional Swift development skills
- iOS/macOS development workflows
- Code review assistance tools

## Related Resources

- [Claude Code Plugin Template](https://github.com/ivan-magda/claude-code-plugin-template) — Starter template for creating your own plugins
- [Apple Swift Migration Guide](https://www.swift.org/migration/documentation/migrationguide/) — Official Swift 6 migration documentation

## License

MIT License — see [LICENSE](LICENSE) for details.

## Acknowledgments

Built for [Claude Code](https://claude.com/claude-code) by [Anthropic](https://www.anthropic.com/).

## Author

Maintained by [Ivan Magda](https://github.com/ivan-magda). Contributions and feedback welcome via issues.
