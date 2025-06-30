# 3. Clean architecture implementation

Date: 2025-06-29

## Status

Accepted

## Context

The eShopping project will be redesigned as a distributed system based on polyglot microservices, with the goal of maximizing scalability, maintainability, and technological independence between services.

Architecture requirements:
- Allows complete isolation of business logic from the rest of the infrastructure.
- Is flexible enough to support different interfaces (REST, gRPC, messaging, CLI, etc.).
- Facilitates the independent evolution of each microservice, even across different technology stacks (NestJS, Golang).
- Provides a clear structure for unit and integration testing, reducing dependencies on external frameworks or details.

## Decision

It was decided to use hexagonal architecture (Ports & Adapters) in all microservices.

## Consequences

What becomes easier or more difficult to do and any risks introduced by the change that will need to be mitigated.
