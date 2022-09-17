# Type System

Covers the static type checking that Swift performs to verify
that a program is safe and well-formed from the point-of-view of Concurrency.

## Terminology

TODO: define isolation and explain the concept behind Sendable.

TODO: cover the kinds of isolation.

## Isolation

Nearly all declarations in Swift are considered to have isolation, except:

- Local `let` or `var` within a function.
- Parameters

## Sendable