---
name: swift-6-migration
description: Guides Swift code migration to Swift 6, including concurrency adoption, data race safety, and strict checking. Fixes Sendable conformance issues, actor isolation problems, and enables complete checking mode. Use when migrating to Swift 6, enabling Swift 6 language mode, fixing concurrency warnings, resolving data race issues, or adopting async/await and actors.
allowed-tools: Read, Edit, Grep, Glob, Bash
---

# Swift 6 Migration

Expert guidance for migrating Swift codebases to Swift 6, including concurrency adoption and strict checking.

## Migration Approach

1. **Assess Current State**: Review Swift compiler version and current language mode
2. **Incremental Strategy**: Enable warnings first, then gradually fix issues
3. **Focus Areas**: Prioritize data race safety, actor isolation, and Sendable conformance
4. **Testing**: Verify runtime behavior after changes

## Key Migration Topics

Refer to [migration-guide.md](migration-guide.md) for detailed guidance on:
- Complete concurrency checking
- Data race safety patterns
- Incremental adoption strategies
- Common problems and solutions
- Library evolution considerations
- Swift 6 mode enablement

## Commands

Use these commands during migration:

```bash
# Check Swift compiler version
swift --version

# Build with Swift 6 warnings
swift build -Xswiftc -swift-version -Xswiftc 6

# Enable complete checking
# Add to Package.swift or build settings:
# .enableUpcomingFeature("StrictConcurrency")
```

## Instructions

When helping with Swift 6 migration:

1. **Read relevant Swift files** to understand the current implementation
2. **Identify concurrency and data race issues** in the code
3. **Reference migration-guide.md** - a single file containing 25 bundled sections:
   - Check the table of contents at the top to see all available sections
   - For common problems and solutions: Search for "FILE: Guide.docc/CommonProblems.md"
   - For Sendable conformance and data race patterns: Search for "FILE: Guide.docc/DataRaceSafety.md"
   - For incremental migration strategies: Search for "FILE: Guide.docc/IncrementalAdoption.md"
   - For Swift 6 mode enablement: Search for "FILE: Guide.docc/Swift6Mode.md"
   - For complete checking: Search for "FILE: Guide.docc/CompleteChecking.md"
   - Use grep to find specific topics: `grep -n "pattern" migration-guide.md`
4. **Propose incremental changes** following the patterns from the guide
5. **Test changes** with appropriate compiler flags (see Commands section)
6. **Explain the reasoning** behind each change to the user

