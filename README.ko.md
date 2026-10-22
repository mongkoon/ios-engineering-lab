# iOS Engineering Lab

**한국어** | [English](README.md)

iOS 개발 기술과 엔지니어링 지식을 체계적으로 재정립하기 위한 실험 중심 기술 학습 저장소입니다. 기존 개발 경험을 바탕으로 기초 개념을 다시 확인하고, 작은 코드 실험으로 실제 동작을 검증하며, 설계 의사결정의 근거를 기록합니다.

## 저장소의 목적

장기간 iOS 앱을 개발하면서 축적한 실무 경험과 최신 기술에 대한 정확한 개념적 이해를 연결합니다. Thread와 RunLoop부터 Reactive Programming, Swift Concurrency, SwiftUI, 아키텍처, 테스트까지 폭넓게 다룹니다.

핵심은 API 사용법을 외우는 것이 아니라 **왜 그렇게 동작하는지 설명할 수 있는 수준**에 도달하는 것입니다.

## 학습 원칙

- **개념 우선:** API에 앞서 정확한 용어와 개념의 경계를 이해합니다.
- **기술 비교:** GCD, RxSwift, Combine, Swift Concurrency의 목적과 차이를 비교합니다.
- **코드 검증:** 최소 재현 코드, 컴파일러 진단, 자동화 테스트로 가설을 확인합니다.
- **환경 기록:** Swift/Xcode 버전, 언어 모드, 주요 빌드 설정과 플랫폼 버전을 남깁니다.
- **설계 근거:** 정확성, 취소, 소유권, UI 반응성, 유지보수성을 기준으로 판단합니다.
- **면접 준비:** 기술적 의사결정을 영어로 간결하게 설명하는 연습을 병행합니다.

## 학습 지도

| 영역 | 주제 | 상태 |
| --- | --- | --- |
| 01 · Foundations | Thread, RunLoop, GCD, OperationQueue, 동기화 | 예정 |
| 02 · RxSwift | Observable, 구독, Trait, Scheduler, Dispose, 테스트 | 예정 |
| 03 · Combine | Publisher, Subscriber, Demand, Scheduling, Cancellation | 예정 |
| 04 · Swift Concurrency | async/await, Task, Actor, Isolation, Sendable, 구조화된 동시성 | 예정 |
| 05 · SwiftUI | 상태, Observation, View Identity, 생명주기 | 예정 |
| 06 · Architecture | MVVM, 의존성 주입, 모듈화, 설계의 장단점 | 예정 |
| 07 · Testing | 단위·통합·UI·동시성 테스트 | 예정 |

> 위 순서는 **학습 경로**이며, RxSwift → Combine → Swift Concurrency가 서로를 완전히 대체한다는 의미는 아닙니다.

## 저장소 구조

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

각 빈 폴더에는 Git에서 디렉터리 구조가 유지되도록 `.gitkeep` 파일을 넣었습니다. 코드와 학습 문서는 검증한 뒤 단계적으로 추가합니다.

## 실험 기록 양식

1. **Question — 질문:** 무엇을 확인하려는가?
2. **Hypothesis — 가설:** 어떤 결과를 예상하며 그 이유는 무엇인가?
3. **Environment — 환경:** Xcode/Swift 버전, 언어 모드, 플랫폼과 빌드 설정
4. **Code — 코드:** 최소 재현 예제
5. **Observation — 관찰:** 실제 출력, 컴파일러 진단, 테스트 결과
6. **Explanation — 해석:** 언어가 보장하는 동작과 단순 관찰 결과를 구분
7. **Trade-offs — 장단점:** 어떤 상황에서 유용하고 위험한가?
8. **Interview notes — 면접 정리:** 영어로 설명하는 핵심 문장

**중요:** 한 번 관찰된 Task 실행 순서만으로 다른 실행 순서가 불가능하다고 단정하지 않습니다. 언어 차원의 보장과 실행 환경에 따른 결과를 구분합니다.

## 첫 번째 목표

**Thread, Queue, Concurrency, Parallelism, Asynchronous Execution, Scheduling**을 정확히 이해하고, 이를 RxSwift 및 최신 Swift 동시성 모델과 연결합니다.

## 공식 참고 문서

- [The Swift Programming Language — Concurrency](https://docs.swift.org/swift-book/documentation/the-swift-programming-language/concurrency/)
- [Swift.org — Migrating to Swift 6](https://www.swift.org/migration/)
- [RxSwift](https://github.com/ReactiveX/RxSwift)
- [Apple — Combine](https://developer.apple.com/documentation/combine)

## 저장소 상태

계속 확장하는 개인 기술 학습 저장소입니다. 예제와 설명은 학습용이며, 실제 서비스에 적용하기 전 관련 환경과 제약을 다시 확인합니다.
