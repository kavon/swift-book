# Execution Semantics

Covers the runtime behaviors of a concurrent Swift program with respect to Tasks 
and how isolation is maintained and checked dynamically.

## Outline

This document is meant to cover topics such as:

probably worth skimming this for more ideas: https://forums.swift.org/tag/concurrency

- When and where hops will happen.
- When am I guaranteed to be on the MainActor?
  - how does `await` interact?
- What happens when I call `Task.init`?
- The reentrancy issue for actors.
- The not-FIFO situation for tasks & actors.
  - https://forums.swift.org/t/is-the-order-of-task-execution-in-this-code-deterministic/60342
- The runtime checks for isolation when bridging for ObjC.
- The general way we do bridging for ObjC.
- Task Groups (when things synchronize, when errors are thrown).
- Task cancellation.
- Priority escalation.
- DispatchQueue.main =?= MainActor (https://forums.swift.org/t/current-actor-semantics-question/60120)