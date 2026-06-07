# Metadata Standards

Objectives

- Define required metadata fields and controlled formats for all documents to improve search, governance and lifecycle automation.

Scope

- Front-matter fields, asset IDs, revision, author, owner, review date, regulatory tags.

Stakeholders

- IA, Content Owners, DevOps.

Deliverables

- Metadata schema (YAML), examples, validation scripts.

Processes

- Authors include front-matter; CI runs validation on PRs.

Governance Mechanisms

- Metadata schema stored in repo and version-controlled.

Templates

- Example front-matter for SOPs, manuals, and technical references.

Metrics

- Percentage of pages with valid metadata, validation failures per PR.

Risks

- Missing or inconsistent metadata.

Mitigation Strategies

- Enforce metadata in CI; provide editors with templates.

Best Practices

- Keep metadata minimal but sufficient for search and lifecycle management.
