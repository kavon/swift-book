# Execution Semantics

Covers the runtime behaviors of a concurrent Swift program with respect to Tasks 
and how isolation is maintained and checked dynamically.

## Outline

This document is meant to cover topics such as:

- When and where hops will happen.
- When am I guaranteed to be on the MainActor?
  - how does `await` interact?
- What happens when I call `Task.init`?
- The reentrancy issue for actors.
- The FIFO situation for tasks.
- The runtime checks for isolation when bridging for ObjC.
- The general way we do bridging for ObjC.
- Task Groups (when things synchronize, when errors are thrown).
- Task cancellation.
- Priority escalation.