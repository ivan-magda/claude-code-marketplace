# Claude Code Plugin Marketplace

A curated collection of Claude Code plugins maintained by Ivan Magda.

## Overview

This marketplace provides high-quality plugins that extend Claude Code's capabilities with specialized tools and skills for software development. All plugins follow best practices and are validated through automated CI/CD workflows.

## Available Plugins

### Swift Plugin

Swift programming language utilities and migration tools for Claude Code.

**Features:**
- Swift 6 migration guidance with concurrency adoption
- Data race safety detection and fixes
- Sendable conformance support
- Complete checking mode implementation
- Incremental migration strategies

**Version:** 1.0.0

[View Swift Plugin Documentation](plugins/swift/README.md)

## Installation

### Prerequisites

- Claude Code installed and configured
- Git (for GitHub-based installation)

### Install from GitHub

1. Add this marketplace to Claude Code:
   ```
   /plugin marketplace add ivan-magda/claude-code-marketplace
   ```

2. Install the Swift plugin:
   ```
   /plugin install swift@claude-code-marketplace
   ```

3. Verify installation:
   ```
   /plugin list
   ```

### Local Development

For testing and development purposes:

1. Clone the repository:
   ```bash
   git clone https://github.com/ivan-magda/claude-code-marketplace.git
   cd claude-code-marketplace
   ```

2. Add the local marketplace:
   ```
   /plugin marketplace add ./
   ```

3. Install plugins:
   ```
   /plugin install swift@claude-code-marketplace
   ```

## Usage

After installing a plugin, its features automatically activate based on context. For example, the Swift 6 migration skill activates when working with Swift code migration tasks.

### Swift Plugin Example

```
Help me migrate this Swift code to Swift 6
```

or

```
Can you check this code for Swift 6 concurrency issues?
```

## License

MIT License - see [LICENSE](LICENSE) file for details.

## Acknowledgments

Built for the Claude Code ecosystem. Special thanks to the Anthropic team for creating an extensible and powerful AI coding assistant.
