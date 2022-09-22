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

### Domains

TODO: Define the boundaries of an isolation domain. That will help people understand
what crossing one means and when they can happen. I believe the language constructs
that have these boundaries are isolated accessors, methods, functions, and closures.

I think in general we need to explain that isolation is something checked only upon uses of a value that has isolation in its type. The requirements for that access varies depending on the isolation of the context in which that use appears. That includes whether an `await` is needed, and whether values passed or returned must be `Sendable`.

## Sendable

Only a value whose type conforms to the `Sendable` protocol is safe to share
across isolation domains.
