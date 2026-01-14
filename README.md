# Claude Superpowers

A personally curated collection of Claude Code plugins, skills, and development tools. This repository extends Claude Code with specialized capabilities for Swift development, code migration, and AI-assisted workflows.

[![GitHub stars](https://img.shields.io/github/stars/ivan-magda/claude-superpowers?style=social)](https://github.com/ivan-magda/claude-superpowers/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/ivan-magda/claude-superpowers?style=social)](https://github.com/ivan-magda/claude-superpowers/network/members)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Validate Plugins](https://github.com/ivan-magda/claude-superpowers/actions/workflows/validate-plugins.yml/badge.svg)](https://github.com/ivan-magda/claude-superpowers/actions/workflows/validate-plugins.yml)

## Available Plugins

| Plugin                           | Description                                           | Version |
| -------------------------------- | ----------------------------------------------------- | ------- |
| [swift](plugins/swift/README.md) | Swift 6 migration, DocC documentation, demo recording | 1.0.2   |

## Installation

### Quick Start

Add the marketplace:

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

## License

MIT License — see [LICENSE](LICENSE) for details.

## Acknowledgments

Built for [Claude Code](https://claude.com/claude-code) by [Anthropic](https://www.anthropic.com/).

## Author

Maintained by [Ivan Magda](https://github.com/ivan-magda). Contributions and feedback welcome via issues.
