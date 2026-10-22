# iOS Engineering Lab

[한국어](README.ko.md) | **English**

A hands-on knowledge base for iOS engineering: revisiting foundational concepts, verifying behavior with small experiments, and documenting the engineering trade-offs behind real-world decisions.

## Why this repository exists

Years of shipping iOS applications build valuable practical intuition. This lab connects that experience with a precise understanding of the technologies underlying today's iOS systems—from threads and event loops to reactive programming, Swift Concurrency, SwiftUI, architecture, and testing.

The emphasis is on **understanding why a mechanism works**, not only remembering how to use an API.

## Learning principles

- **Concept first:** define terms and understand their boundaries before adopting an API.
- **Compare approaches:** relate GCD, RxSwift, Combine, and Swift Concurrency without assuming one universally replaces another.
- **Prove with code:** use small reproducible experiments, compiler diagnostics, and automated tests.
- **Record the context:** document Swift version, language mode, compiler settings, and relevant platform versions.
- **Explain trade-offs:** focus on correctness, cancellation, ownership, responsiveness, and maintainability.
- **Interview-ready:** practice explaining technical decisions clearly in English.

## Learning map

| Area | Topics | Status |
| --- | --- | --- |
| 01 · Foundations | Threads, RunLoop, GCD, OperationQueue, synchronization | Planned |
| 02 · RxSwift | Observable, subscriptions, traits, schedulers, disposal, testing | Planned |
| 03 · Combine | Publishers, subscribers, demand, scheduling, cancellation | Planned |
| 04 · Swift Concurrency | async/await, Task, actors, isolation, Sendable, structured concurrency | Planned |
| 05 · SwiftUI | State, observation, view identity, lifecycle | Planned |
| 06 · Architecture | MVVM, dependency injection, modularization, design trade-offs | Planned |
| 07 · Testing | Unit, integration, UI, and concurrency tests | Planned |

> The sequence is a **learning path**, not a claim that RxSwift, Combine, and Swift Concurrency are successive replacements for one another.

## Repository structure

```text
ios-engineering-lab/
├── README.md
├── README.ko.md
├── 01-foundations/
│   ├── threads/
│   ├── runloop/
│   ├── gcd/
│   └── operation-queue/
├── 02-rxswift/
│   ├── observable/
│   ├── subjects-relays/
│   ├── operators/
│   ├── schedulers/
│   ├── memory-management/
│   └── testing/
├── 03-combine/
│   ├── publishers/
│   ├── subscribers/
│   ├── operators/
│   └── schedulers/
├── 04-swift-concurrency/
│   ├── async-await/
│   ├── tasks/
│   ├── actors/
│   ├── isolation/
│   └── sendable/
├── 05-swiftui/
│   ├── state-management/
│   ├── observation/
│   └── lifecycle/
├── 06-architecture/
│   ├── mvvm/
│   ├── dependency-injection/
│   └── modularization/
└── 07-testing/
    ├── unit-tests/
    ├── concurrency-tests/
    └── ui-tests/
```

Each empty topic directory contains a `.gitkeep` placeholder until its first notes or runnable examples are added.

## Experiment template

Each experiment should include:

1. **Question** — What behavior are we investigating?
2. **Hypothesis** — What do we expect, and why?
3. **Environment** — Xcode/Swift versions, language mode, platform, and relevant build settings.
4. **Code** — A minimal reproducible example.
5. **Observation** — Actual output, diagnostics, and test results.
6. **Explanation** — Which guarantees are specified, and which outcomes are merely observed?
7. **Trade-offs** — When would this approach be appropriate or risky?
8. **Interview notes** — A concise explanation in English.

**Important:** a single observed scheduling order does not prove that other orders are impossible. Experiments should distinguish language guarantees from implementation-dependent behavior.

## First milestone

Build a precise mental model of **threads, queues, concurrency, parallelism, asynchronous execution, and scheduling**, then connect those ideas to RxSwift and contemporary Swift features.

## References

- [The Swift Programming Language — Concurrency](https://docs.swift.org/swift-book/documentation/the-swift-programming-language/concurrency/)
- [Swift.org — Migrating to Swift 6](https://www.swift.org/migration/)
- [RxSwift](https://github.com/ReactiveX/RxSwift)
- [Apple — Combine](https://developer.apple.com/documentation/combine)

## Project status

This is an evolving learning lab. Examples and notes are educational and should be checked against the documented environment before production use.
