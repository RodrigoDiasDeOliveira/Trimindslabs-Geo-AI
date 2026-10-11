# ADR-001: Separate Predecessor Repository from Geo-AI V4 Deployment Identity

- **Status:** PROPOSED
- **Date:** 2026-10-11

## Context

This repository contains a Python/FastAPI and ML-oriented Geo-AI implementation with Terraform resources. The separate `Trimindslabs-Geo-AI-V4` repository contains the current Node.js/Express and TypeScript application and a Cloud Run deployment workflow. The older README associated the V4 service URL with this repository without proving that the deployed image was built from this source.

## Decision proposed

Treat this repository as the predecessor/related Python implementation unless current Cloud Run image provenance demonstrates otherwise. Record deployment identity using the service, project, region, revision, image digest and source commit. Keep local synthetic-model validation separate from real satellite-data claims.

## Consequences

- Historical URL references are not proof that this repository is currently deployed.
- Terraform configuration and model components describe capability/configuration, not live operational state.
- This record remains proposed pending owner confirmation.
