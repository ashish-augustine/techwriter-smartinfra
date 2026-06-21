# Information Architecture Draft

## Purpose

This IA draft maps the site's 50 sections to logical landing pages, content types, URL patterns, and suggested metadata fields. It's a working blueprint for the documentation program designed to be reviewed and iterated by the IA working group.

## IA Summary

- Top-level navigation uses a subject-based approach (Governance, Engineering, Operations, Asset Programs, Support & Analytics).
- Each top-level section maps to a landing page with a short overview, key links, and a canonical content model.
- Asset-centric content (bridges, tunnels, rail, water) uses an `asset` content type that links to SOPs, maintenance histories, drawings, and compliance records.

## Landing pages & URL mapping (compact)

Page title → filename → suggested URL

- Executive Summary → `index.md` → `/`
- Documentation Vision and Strategy → `02-documentation-vision-and-strategy.md` → `/documentation-vision/`
- Enterprise Documentation Governance Framework → `03-enterprise-documentation-governance-framework.md` → `/governance/`
- Information Architecture Blueprint → `04-information-architecture-blueprint.md` → `/ia/`
- Knowledge Management Program → `05-knowledge-management-program.md` → `/knowledge-management/`
- Taxonomy Design → `06-taxonomy-design.md` → `/taxonomy/`
- Metadata Standards → `07-metadata-standards.md` → `/metadata/`
- Content Ownership Model → `08-content-ownership-model.md` → `/ownership/`
- Documentation Lifecycle Model → `09-documentation-lifecycle-model.md` → `/lifecycle/`
- Documentation Review Framework → `10-documentation-review-framework.md` → `/review/`
- Engineering Documentation Architecture → `11-engineering-documentation-architecture.md` → `/engineering-architecture/`
- Infrastructure Asset Documentation System → `12-infrastructure-asset-documentation-system.md` → `/asset-system/`
- Asset Lifecycle Documentation → `13-asset-lifecycle-documentation.md` → `/asset-lifecycle/`
- Bridge Maintenance Documentation → `14-bridge-maintenance-documentation.md` → `/assets/bridge/`
- Rail Operations Documentation → `15-rail-operations-documentation.md` → `/assets/rail/`
- Traffic Management Documentation → `16-traffic-management-documentation.md` → `/traffic/`
- Utilities Documentation Framework → `17-utilities-documentation-framework.md` → `/utilities/`
- Water Infrastructure Documentation → `18-water-infrastructure-documentation.md` → `/assets/water/`
- Emergency Response Documentation → `19-emergency-response-documentation.md` → `/emergency/`
- Incident Management Documentation → `20-incident-management-documentation.md` → `/incident-management/`
- Preventive Maintenance Documentation → `21-preventive-maintenance-documentation.md` → `/preventive-maintenance/`
- Risk Assessment Documentation → `22-risk-assessment-documentation.md` → `/risk-assessment/`
- Safety Documentation Framework → `23-safety-documentation-framework.md` → `/safety/`
- Regulatory Compliance Documentation → `24-regulatory-compliance-documentation.md` → `/compliance/`
- Standard Operating Procedures Library → `25-standard-operating-procedures-library.md` → `/sops/`
- Operations Manual → `26-operations-manual.md` → `/operations-manual/`
- Maintenance Manual → `27-maintenance-manual.md` → `/maintenance-manual/`
- Troubleshooting Manual → `28-troubleshooting-manual.md` → `/troubleshooting/`
- Technical Reference Manual → `29-technical-reference-manual.md` → `/technical-reference/`
- Knowledge Base Architecture → `30-knowledge-base-architecture.md` → `/kb-architecture/`
- Search Strategy Design → `31-search-strategy-design.md` → `/search/`
- Documentation Templates → `32-documentation-templates.md` → `/templates/`
- Documentation Standards → `33-documentation-standards.md` → `/standards/`
- Documentation Style Guide → `34-documentation-style-guide.md` → `/style-guide/`
- Engineering Change Documentation Process → `35-engineering-change-documentation-process.md` → `/ecp/`
- Training and Learning Framework → `36-training-and-learning-framework.md` → `/training/`
- Certification Program Documentation → `37-certification-program-documentation.md` → `/certification/`
- Documentation Quality Assurance Framework → `38-documentation-quality-assurance-framework.md` → `/qa/`
- Content Audit Methodology → `39-content-audit-methodology.md` → `/audit/`
- Documentation Analytics Program → `40-documentation-analytics-program.md` → `/analytics/`
- Documentation KPIs → `41-documentation-kpis.md` → `/kpis/`
- Documentation ROI Framework → `42-documentation-roi-framework.md` → `/roi/`
- Content Health Metrics → `43-content-health-metrics.md` → `/content-health/`
- Governance Dashboard → `44-governance-dashboard.md` → `/dashboard/`
- Stakeholder Communication Framework → `45-stakeholder-communication-framework.md` → `/communication/`
- Cross-Functional Collaboration Model → `46-cross-functional-collaboration-model.md` → `/collaboration/`
- Documentation Risk Register → `47-documentation-risk-register.md` → `/risk-register/`
- Enterprise Documentation Roadmap → `48-enterprise-documentation-roadmap.md` → `/roadmap/`
- Future-State Documentation Architecture → `49-future-state-documentation-architecture.md` → `/future-architecture/`
- Senior Technical Writer Leadership Contributions → `50-senior-technical-writer-leadership-contributions.md` → `/leadership/`

## Content types & front-matter schema (suggested)

1. `landing_page` — Overview pages that introduce a program area
  - fields: `title`, `summary`, `owner`, `related_pages: []`, `last_reviewed`, `tags: []`

2. `asset` — Asset-centric records (bridge, tunnel, site)
  - fields: `title`, `asset_id`, `asset_type`, `location`, `owner`, `status`, `drawings: []`, `sops: []`, `maintenance_history: []`, `compliance_records: []`, `tags: []`

3. `sop` — Standard Operating Procedure
  - fields: `title`, `sop_id`, `scope`, `prerequisites`, `steps`, `safety_notes`, `owner`, `revision`, `effective_date`, `tags: []`

4. `procedure` — Short procedural guidance (task-level)
  - fields: `title`, `duration`, `difficulty`, `steps`, `owner`, `tags: []`

5. `reference` — Technical references, specs, drawings
  - fields: `title`, `doc_id`, `format`, `linked_assets: []`, `version`, `owner`, `tags: []`

6. `policy` — Governance & policy documents
  - fields: `title`, `policy_id`, `owner`, `approval_date`, `next_review`, `scope`, `tags: []`

## Navigation & discoverability

- Keep primary nav shallow (up to 3–4 top items) and use right-hand secondary nav for deep sections.
- Implement a tags-based faceted search and surface `asset` pages in search results with high priority.
- Add `related_pages` on landing pages to encourage cross-navigation.

## Cross-linking rules

- Every `asset` page must link to its canonical `sops`, `maintenance_history`, and `drawings`.
- Policies and standards should link to `sop` examples and `procedure` pages.

## Quick wins & next steps

1. Populate the `asset` content model with 3 sample bridge pages.
2. Create YAML front-matter templates for `asset`, `sop`, and `landing_page` and add to `docs/templates/`.
3. Configure search weighting so `asset` and `sop` types rank higher for operational queries.

---

If this looks good I will (a) generate YAML front-matter templates, (b) create three sample `asset` pages for bridges, and (c) add a simple search weighting example in `mkdocs.yml`.
