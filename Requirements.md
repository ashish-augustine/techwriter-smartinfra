# SMART INFRASTRUCTURE & CIVIL ENGINEERING DOCUMENTATION PROGRAM — Requirements Capture

Document version: 1.0
Author: Senior Technical Writer (project owner)
Date: 2026-06-07

## Purpose

This Requirements Capture records the finalized scope, constraints, success criteria, tooling decisions, and verification method for the enterprise-grade documentation portfolio titled "SMART INFRASTRUCTURE & CIVIL ENGINEERING DOCUMENTATION PROGRAM". This document will be the single source of truth for design and implementation during Phase 0 and subsequent milestones.

## Primary objectives

- Build a flagship portfolio that presents an enterprise documentation program (not a collection of writing samples) for infrastructure systems including Smart Cities, Transportation Networks, Rail Systems, Bridges, Tunnels, Highways, Utilities, Water and Energy Infrastructure, and Traffic Management Systems.
- Position the author for Senior Technical Writer and leadership roles in New Zealand.
- Demonstrate advanced capabilities in documentation strategy, governance, IA, KM, engineering and operations documentation, SOP development, metrics, change/risk/regulatory documentation, training, and stakeholder management.

## Key decisions & constraints (finalized)

- Primary audience / hiring target: Senior Technical Writer roles in New Zealand.
- Hiring constraints: any company (public or private) — no employer exclusions.
- Regulatory scope: NZ Building Code will be referenced where relevant.
- Existing assets: None to migrate; repository starts from clean slate.
- Authoring & publishing stack: MkDocs (primary) + Netlify for hosting (live website required).
- Diagram tooling: Lucidchart (preferred). No paid Lucidchart/Visio license is available; designs will include text descriptions and editable Drawio backups when necessary.
- Visual branding: neutral corporate palette; follow NZ government accessibility and tone where appropriate; UK English spelling.
- Content depth: Two sections will be fully detailed end-to-end; the remaining sections will be developed as structured outlines, templates, and authoritative templates for future completion.
- Deliverable formats: Live website (MkDocs site published to Netlify). Exportable PDFs will be generated for manuals where required.
- Timeline & availability: Author will allocate ~1 hour per day. High-level estimate: 10–12 weeks to produce a full enterprise-quality portfolio (iterative delivery by milestone); initial milestones will be small increments (1–5% per step).
- Sensitive data: None.

## Success criteria

- A live MkDocs site deployed to Netlify containing the full program structure and two fully-detailed sections with complete templates, governance artifacts, diagrams (text-described + Lucidchart links), and downloadable manuals.
- Hiring‑ready README and executive deliverables that hiring managers in NZ can review and validate as enterprise-grade.
- Acceptable authoring workflow demonstrated: local Git repository, content authored in Markdown, CI/deploy to Netlify, diagram assets linked from Lucidchart (or attached Drawio SVGS), and clear governance artifacts (RACI, KPIs, risk register).
- Verified by the author via screenshots and messages and by a short stakeholder review cycle.

## Assumptions

- The workspace has standard development tools (git) and the author can provide Netlify/GitHub credentials when required for remote repo creation and publishing.
- Visual diagrams will be created in Lucidchart; without a paid account, exports in PNG/SVG or Drawio alternatives will be used for repo assets.
- NZ regulatory references (NZ Building Code) will be cited at a high level — no legal advice provided.

## Detailed requirements (by category)

1. Objectives
   - Demonstrate leadership in enterprise documentation for infrastructure projects.
   - Provide a reusable documentation program blueprint suitable for large transport and utilities organisations.

2. Scope
   - In scope: Documentation program artifacts (strategy, governance, IA, KM, templates, SOPs), two fully‑detailed domain sections, diagrams, governance dashboards, and a live MkDocs site.
   - Out of scope: Migration of legacy documents, proprietary engineering CAD files, or operational system integrations beyond diagrammatic references to CMMS/GIS.

3. Stakeholders
   - Primary: Hiring managers (Senior Technical Writer/Documentation Lead roles), Author (project owner).
   - Secondary: Engineering Manager, Safety Lead, Asset Manager, Knowledge Manager (for review and sign-off during QA milestone).

4. Deliverables
   - `Requirements.md` (this document).
   - MkDocs site scaffold with navigation and landing pages.
   - Two fully-detailed sections (complete content, diagrams, SOPs, templates).
   - Template pack (Markdown templates, SOP templates, RACI).
   - Governance artifacts (RACI matrices, decision trees, risk register).
   - Deployment pipeline instructions for Netlify.
   - Exportable PDFs for the two detailed sections (manuals).

5. Processes
   - Authoring: Markdown → Git commits → Pull Request (peer review) → Merge to `main` → Netlify deploy.
   - Review: Editorial checklist + technical review (subject-matter reviewer) + final sign-off by named stakeholder.
   - Change control: Minor edits through standard PR; major structural changes require documented change request and approval by Content Owner.

6. Governance mechanisms
   - Content ownership model (see later milestones).
   - RACI matrices for major document types.
   - Versioning: semantic versioning of major manuals; Git for source control (branch-per-feature).

7. Templates
   - Master Markdown templates for: Executive Summary, SOP, Operations Manual, Maintenance Manual, Troubleshooting, Technical Reference, Policy, Risk Assessment.

8. Metrics
   - Documentation KPIs (page views, search success, time to find, review cycle time, content health).

9. Risks
   - Limited author availability (1 hour/day) may slow delivery.
   - No paid Lucidchart subscription may limit collaborative diagram editing.
   - Remote GitHub/Netlify configuration requires credentials or author assistance.

10. Mitigation strategies
    - Break the work into micro-milestones sized for 1 hour/day.
    - Use Drawio as a free backup; prepare textual diagram descriptions for accessibility.
    - Provide clear commands and short scripts; request author to supply GitHub/Netlify tokens or run the final push step.

11. Best practices
    - Single source of truth in Git for Markdown content.
    - CI-driven static site deployment to Netlify.
    - Template-first approach: author using templates to ensure consistency.
    - Accessibility and plain-English rules aligned to NZ guidelines.

## Verification and acceptance for Step 1

- Deliverable: This `Requirements.md` file.
- Verification method: Author will confirm by either (a) posting a screenshot that shows the file in the workspace, or (b) replying with a short confirmation message that the content is correct and accepted.
- Once accepted, Step 1 will be marked complete and we will proceed to Step 2 (Stakeholder questions & decisions).

## Next steps (after acceptance)

1. Mark Step 1 complete in the project todo list.
2. Present the Stakeholder Questions & Decisions (detailed list) for your answers — these will finalize repository names, remote publishing credentials, and diagram export strategy.
3. On your approval, I will create the full `MkDocs` scaffold, templates, and initial commits (I will provide the exact git commands and a human-style commit message for you to run or to authorize me to run).

## Git & GitHub note

I will initialize a local Git repository in the workspace and prepare a clear set of commands to create a remote repository and push content. Creating the remote repo and pushing requires GitHub authentication; please indicate whether you'd like me to create the remote (I will need `gh` / token), or whether you'd prefer to run the remote creation and push yourself. Suggested repo name: `smart-infra-docs-portfolio` (under a GitHub account or org you choose). If you give permission now I will prepare the local commit and the exact commands to create/push the remote.

## Estimated effort and schedule

- Step 1 (Requirements capture): complete (this file).
- Full program: estimated 10–12 weeks of part-time work (1 hour/day).
- Next 2 milestones (repo scaffold + IA draft): 2–3 weeks total at 1 hour/day.

## Sign-off

Please confirm acceptance of this document by replying with either:

- `ACCEPT` — if the requirements are correct and you agree to proceed to Step 2, or
- Edit requests — list corrections or missing items and I will update `Requirements.md`.

-- End of Requirements Capture --
