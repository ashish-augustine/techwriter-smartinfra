# Documentation Risk Register

Objectives

- Maintain a register of documentation-specific risks with owners and mitigations.

Scope

- Risks to documentation quality, continuity, compliance and availability.

Stakeholders

- Governance Board, Risk Owner, Content Owners.

Deliverables

- Risk register table (example rows below) and mitigation plans.

Processes

- Quarterly review and update; escalate high risks.

Governance Mechanisms

- Risk owner assignment and review cadence.

Templates

- Risk register CSV/YAML template.

Example entries
| ID | Risk | Likelihood | Impact | Owner | Mitigation |
|----|------|------------|--------|-------|------------|
| R1 | Single-author dependency | Medium | High | Content Owner | Cross-train and capture knowledge |
| R2 | No paid Lucidchart account | Medium | Medium | Senior Technical Writer | Use Drawio backups and textual diagrams |
| R3 | Limited author availability (1 hr/day) | High | Medium | Project Owner | Micro-milestones and backlog prioritisation |

Metrics

- Number of open high risks, mitigation progress.

Risks

- Untracked risks; stale mitigations.

Mitigation Strategies

- Automate reminders and keep register close to governance dashboard.

Best Practices

- Keep register actionable and assign owners for each mitigation.

Sample risk-to-mitigation diagram (Mermaid)

The following Mermaid flowchart visualises a subset of register entries, their likelihood/impact notes, and mapped mitigations. Copy this into any Mermaid-capable renderer (MkDocs with a Mermaid plugin, or mermaid.live) to view the diagram.

```mermaid
flowchart TD
  subgraph Risks[Documentation Risks]
    R1["R1: Single-author dependency\n(Likelihood: Medium, Impact: High)"]
    R2["R2: No paid Lucidchart account\n(Likelihood: Medium, Impact: Medium)"]
    R3["R3: Limited author availability\n(Likelihood: High, Impact: Medium)"]
  end

  subgraph Mitigations[Mitigations]
    M1["M1: Cross-train & create knowledge backups"]
    M2["M2: Maintain Drawio exports + textual diagram descriptions"]
    M3["M3: Break work into micro-milestones (1-hr tasks)"]
  end

  R1 --> M1
  R2 --> M2
  R3 --> M3
  R1 --> R3
  M1 --> Done["Status: Assigned / In-progress"]
  M2 --> Done
  M3 --> Done

  classDef risk fill:#ffe6e6,stroke:#cc0000;
  classDef mitig fill:#e6fff2,stroke:#009900;
  class R1,R2,R3 risk;
  class M1,M2,M3 mitig;
```

Use this diagram as an example — expand the register table above and map additional rows to diagram nodes for board-level visualisations.

# Documentation Risk Register

Objectives

- Maintain a register of documentation-specific risks with owners and mitigations.

Scope

- Risks to documentation quality, continuity, compliance and availability.

Stakeholders

- Governance Board, Risk Owner, Content Owners.

Deliverables

- Risk register table (example rows below) and mitigation plans.

Processes

- Quarterly review and update; escalate high risks.

Governance Mechanisms

- Risk owner assignment and review cadence.

Templates

- Risk register CSV/YAML template.

Example entries
| ID | Risk | Likelihood | Impact | Owner | Mitigation |
|----|------|------------|--------|-------|------------|
| R1 | Single-author dependency | Medium | High | Content Owner | Cross-train and capture knowledge |

Metrics

- Number of open high risks, mitigation progress.

Risks

- Untracked risks; stale mitigations.

Mitigation Strategies

- Automate reminders and keep register close to governance dashboard.

Best Practices

- Keep register actionable and assign owners for each mitigation.
