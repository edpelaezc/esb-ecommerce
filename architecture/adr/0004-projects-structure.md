# 4. Projects structure

Date: 2025-06-29

## Status

Accepted

## Context

In the eShopping project redesign, a hexagonal architecture (Ports & Adapters) was adopted to isolate the core business and facilitate technological evolution.

To support this architecture, a standardized folder structure was defined for each microservice (regardless of whether built in NestJS or Golang) to:

- Maintain consistency and clarity.
- Improve maintainability and ease of navigation.
- Enable specific separation between domains, use cases, and adapters.

## Decision

It was decided to use the following base folder structure:

core
├── application
│   ├── ProductCreator.ts
│   └── ProductSearcher.ts
├── domain
│   ├── entities
│   │   └── Product.ts
│   ├── ports
│   │   └── repositories
│   │       └── ProductRepository.ts
│   └── services
│       └── ProductService.ts
infraestructure
├── adapters
│   └── PostgresProductRepository.ts
├── database
│   └── postgres
│       └── orm
└── http-server
└── api
├── jwt
├── model
└── restcontrollers

## Consequences

- It requires greater initial discipline to maintain the boundaries between core and infrastructure.
- New team members will need training to understand the structure.
- It improves testability and portability of business logic.
