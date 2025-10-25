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

Current version: 1.0.0

## Keywords

swift, migration, swift6, concurrency

