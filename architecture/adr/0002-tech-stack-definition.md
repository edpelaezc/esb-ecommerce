# 2. Tech stack definition

Date: 2025-06-29

## Status

Accepted

## Context

The eShopping project will be redesigned using a polyglot microservices architecture approach. The goal is to build a distributed, scalable, and maintainable system where each service can be developed, deployed, and evolved independently.

## Decision

The decision was made to use:

- NestJS (TypeScript) to develop microservices for orchestration and exposing business APIs.
- Golang for microservices requiring high performance and concurrent processing.

## Consequences

The project will adopt a multi-lingual approach, which introduces additional operational challenges (observability, unified logging, multi-stack CI/CD).
