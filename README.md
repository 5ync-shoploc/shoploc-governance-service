# Shoploc Governance Service

## Overview

`shoploc-governance-service` is a backend microservice responsible for
governing and managing merchant accounts within the Shoploc platform.

It handles business-level governance operations such as merchant account
validation, activation, suspension, and deactivation.

This service is part of the Shoploc microservices architecture.

## Responsibilities

The Governance Service is responsible for:

- Validating merchant accounts
- Activating merchant accounts
- Suspending or deactivating merchant accounts
- Managing merchant governance status
- Applying governance rules to merchant accounts
- Providing governance-related APIs to other Shoploc services

Authentication and identity management are handled by the
`shoploc-identity-service`.

## Architecture

```text
                    ┌──────────────────────┐
                    │   API Gateway        │
                    │ shoploc-api-gateway  │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │ Governance Service   │
                    │                      │
                    │ Merchant governance  │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │ Merchant data / DB   │
                    └──────────────────────┘