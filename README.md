# Fry Express Systems Backstage Demo

This repository contains a complete fictional Backstage catalog for Fry Express Systems, a logistics and e-commerce company operating a delivery platform for hot food, convenience items, and last-mile order fulfillment.

The repository is designed for local Backstage demos and includes:

- organization data for teams and users
- a business domain and supporting systems
- service, frontend, and worker components
- API and infrastructure resource entities
- TechDocs content for each component
- a software template for a Python FastAPI service starter

## Repository Layout

- `catalog-info.yaml`: root registration entrypoint
- `org/`: groups and users
- `domains/`: business domain entities
- `systems/`: platform systems
- `apis/`: published APIs
- `resources/`: infrastructure resources
- `components/`: individual software components with TechDocs
- `templates/`: software template definitions and starter assets

## Registering In Backstage

For local Backstage setups, register the root [`catalog-info.yaml`](./catalog-info.yaml) file. It uses `spec.type: file` and is intended for local filesystem registration.

For GitHub-based registration through the Backstage UI, register [`catalog-info-remote.yaml`](./catalog-info-remote.yaml) instead. It uses `spec.type: url`, which allows relative targets to resolve correctly when the catalog file is loaded from a repository URL.

If your Backstage instance uses the default restrictive catalog rules for UI-registered locations, use [`catalog-info-bootstrap.yaml`](./catalog-info-bootstrap.yaml) first. That bootstrap file contains only components and APIs, which are the most commonly allowed kinds in the "Register existing component" flow.

To ingest the full demo model including groups, users, domains, systems, resources, and the software template, add the repository through `app-config.yaml` with explicit `rules.allow` entries, or expand your catalog backend rules for that location.

## TechDocs

Each component and the software template includes a `mkdocs.yml` file and a `docs/index.md` entrypoint. When TechDocs is enabled in Backstage, each entity page should show a **Docs** tab with the corresponding Markdown rendered through the TechDocs plugin.
