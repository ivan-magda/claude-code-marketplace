# Swift Plugin for Claude Code

Swift programming language utilities and migration tools for Claude Code.

## Features

### Skills

#### Swift 6 Migration

Expert guidance for migrating Swift codebases to Swift 6, including concurrency adoption and strict checking.

**Automatically activates when:**

- Migrating Swift code to Swift 6
- Enabling Swift 6 language mode
- Fixing data race safety issues
- Adopting Swift concurrency (async/await, actors)
- Resolving Sendable conformance issues
- Implementing complete checking mode

**Capabilities:**

- Read and edit Swift files
- Search for concurrency patterns
- Run Swift compiler and build tools
- Provide incremental migration strategies
- Reference comprehensive Swift 6 migration documentation

#### Swift DocC Comments

Guidance for writing proper Swift DocC inline documentation comments.

**Automatically activates when:**

- Writing or enhancing Swift documentation comments
- Adding inline doc comments to Swift source files
- User asks for API documentation help

**Capabilities:**

- Read and edit Swift files
- Ensure correct DocC comment structure
- Distinguish inline comments from .docc catalog files

#### Swift DocC GitHub Pages

Automate Swift package documentation publishing to GitHub Pages via GitHub Actions.

**Automatically activates when:**

- Setting up DocC documentation for a Swift package
- Deploying documentation to GitHub Pages
- Encountering "no such module 'UIKit'" during doc generation

**Capabilities:**

- Create GitHub Actions workflows
- Configure iOS-only vs cross-platform builds
- Set up proper DocC hosting with redirects

#### Swift Package Demo

Record and optimize demo GIFs for Swift package READMEs.

**Automatically activates when:**

- Creating demo GIFs for Swift package READMEs
- Recording iOS Simulator videos
- Setting up demo apps for SwiftUI libraries

**Capabilities:**

- Guide demo app setup
- Run simulator recording commands
- Convert videos to optimized GIFs
- Ask user preferences for GIF sizing

## Installation

### Local Testing

1. Add the local marketplace:

   ```
   /plugin marketplace add ./plugins
   ```

2. Install the Swift plugin:

   ```
   /plugin install swift@local-plugins
   ```

3. Restart Claude Code

### Using the Plugin

Once installed, the Swift 6 migration skill will automatically activate when you're working with Swift code migration tasks. You can also explicitly ask Claude to use it:

```
Help me migrate this Swift code to Swift 6
```

or

```
Can you check this code for Swift 6 concurrency issues?
```

## Documentation

The plugin includes comprehensive Swift 6 migration documentation covering:

- Complete concurrency checking
- Data race safety patterns
- Incremental adoption strategies
- Common problems and solutions
- Library evolution considerations
- Swift 6 mode enablement

## Version

Current version: 1.0.2

## Keywords

swift, migration, swift6, concurrency, docc, documentation, demo
