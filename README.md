# PRAXO-CORE Swift Core

Swift implementation of the PRAXO-CORE contract. This repository is the
Swift Package Manager distribution of the Swift Core from
[axisvela/praxo-core](https://github.com/axisvela/praxo-core).

- `SPEC_VERSION`: `0.2.0`
- Core version: `0.2.0`
- License: MIT
- No external package dependencies

## Install

```swift
.package(url: "https://github.com/axisrobo/praxo-core-swift.git", from: "0.2.0")
```

## Build and test

```bash
swift test
swift run praxo-conformance
python3 api-snapshot.py --check
```

## Layout

- `Sources/PraxoCore/` library.
- `Sources/PraxoConformance/` wire and core vector runner.
- `Tests/PraxoCoreTests/` XCTest coverage.
- `api/` public API snapshot.

## Scope

`0.2.0` implements all eleven conformance vector groups: tool-call parsing, JSON
Schema, plugin manifests, memory, events, stream kinds, checkpoint envelopes,
path policy, context budgets, middleware, and the agent loop. Provider adapters
remain follow-up work.

The normative contract is `spec/` in the main repository. Go remains the
reference implementation.

## Release tags

This repository uses plain semantic-version tags such as `0.2.0`; the main
monorepo uses `swift/v0.2.0`.
