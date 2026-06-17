# Claude Superpowers

A personally curated marketplace of Claude Code plugins.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Validate Plugins](https://github.com/ivan-magda/claude-superpowers/actions/workflows/validate-plugins.yml/badge.svg)](https://github.com/ivan-magda/claude-superpowers/actions/workflows/validate-plugins.yml)

## Table of Contents

- [Background](#background)
- [Philosophy](#philosophy)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## Background

This repository is a [Claude Code](https://claude.com/claude-code) plugin marketplace. It packages plugins that extend Claude Code with specialized skills, and you add it through Claude Code's plugin system rather than cloning it into a project.

The marketplace currently ships one plugin, `swift`, which bundles four skills for Swift and iOS work: Swift 6 migration, DocC inline comments, publishing DocC documentation to GitHub Pages, and recording demo GIFs for package READMEs.

## Philosophy

The collection stays narrow on purpose. Each skill encodes a workflow that has been used on real projects, so the marketplace grows only when a plugin earns its place. A CI workflow validates the marketplace manifest and every plugin entry on each push and pull request, which keeps the catalog installable.

## Features

### swift

Swift programming language utilities and migration tools. The plugin contributes four skills that Claude Code activates from conversation context.

**Swift 6 Migration** — Migrates codebases to Swift 6 language mode and resolves data-race-safety diagnostics. The skill bundles Apple's full migration guide and searches it for each compiler error before applying a fix, covering Sendable conformance, actor isolation, unsafe globals, and async/await adoption. Activates on Swift 6 concurrency errors, Sendable warnings, actor isolation issues, or a request to enable Swift 6 mode.

**Swift DocC Comments** — Writes inline DocC documentation comments with the correct structure, keeping section headers like `## Overview` and `## Topics` out of source comments where they don't belong. Activates when you write or enhance documentation comments in Swift source files.

**Swift DocC GitHub Pages** — Publishes Swift package documentation to GitHub Pages through GitHub Actions. The skill picks the right build method for iOS-only versus cross-platform packages, which avoids the "no such module 'UIKit'" failure, and wires up static hosting with a root redirect. Activates when you set up DocC documentation or deploy it to GitHub Pages.

**Swift Package Demo** — Records and optimizes demo GIFs for Swift package READMEs. It guides demo-app setup, runs iOS Simulator recording, and converts the video to an optimized GIF, asking whether you want full-size or cropped output before encoding. Activates when you create demo GIFs or record simulator videos for a SwiftUI library.

## Installation

Run these commands inside Claude Code.

Add the marketplace:

```
/plugin marketplace add ivan-magda/claude-superpowers
```

Install the Swift plugin:

```
/plugin install swift@claude-superpowers
```

Confirm what is installed:

```
/plugin list
```

### Local development

To work on the plugins from a clone, add the checkout as a local marketplace:

```bash
git clone https://github.com/ivan-magda/claude-superpowers.git
cd claude-superpowers
```

```
/plugin marketplace add ./
/plugin install swift@claude-superpowers
```

## Usage

The skills run automatically once the plugin is installed. Claude Code reads your prompt, matches it against each skill's activation criteria, and applies the relevant one. You can prompt directly:

```
Help me migrate this Swift code to Swift 6
```

```
Add documentation comments to this Swift file
```

```
Set up DocC documentation for this Swift package with GitHub Pages
```

```
Create a demo GIF for this Swift package README
```

See [plugins/swift/README.md](plugins/swift/README.md) for the full activation triggers and the capabilities of each skill.

## Project Structure

```
.claude-plugin/
  marketplace.json              # Marketplace manifest; lists every plugin
plugins/
  swift/
    .claude-plugin/plugin.json  # Plugin manifest
    README.md                   # Plugin documentation
    skills/                     # Skill definitions (SKILL.md per skill)
      swift-6-migration/
      swift-docc-comments/
      swift-docc-github-pages/
      swift-package-demo/
.claude/skills/                 # Maintainer-only skills (not shipped in a plugin)
.github/workflows/              # CI that validates the marketplace and plugins
LICENSE
README.md
```

The `.claude/skills/` directory holds tooling for maintaining this repository, such as the release workflow for bumping plugin versions. Those skills are not part of the installable `swift` plugin.

## Contributing

Issues and pull requests are welcome. The CI workflow checks that `marketplace.json` is valid, that each plugin has a well-formed `plugin.json`, and that no plugin names collide, so run your changes against those expectations before opening a pull request.

## License

Released under the MIT License. Copyright (c) 2025 Ivan Magda. See [LICENSE](LICENSE) for the full text.
