# Flowchart Diagrams

This page demonstrates how to include flowcharts in the documentation using Mermaid syntax and the `mkdocs-mermaid2-plugin` configured in `mkdocs.yml`.

## Basic Flowchart

```mermaid
flowchart TD
  A[Start] --> B{Decision}
  B -->|Yes| C[Proceed]
  B -->|No| D[Review]
  C --> E[Complete]
  D --> E
```

## Process with multiple steps

```mermaid
flowchart LR
  A[Define scope] --> B[Gather requirements]
  B --> C[Analyze risks]
  C --> D[Design documentation]
  D --> E[Review and approve]
  E --> F[Publish]
```

## Conditional workflow example

```mermaid
flowchart TD
  Start([Start]) --> Input[Get input]
  Input --> Check{Valid?}
  Check -->|Yes| Process[Process flowchart]
  Check -->|No| Error[Return error]
  Process --> End([Done])
  Error --> End
```

## Notes

- Mermaid diagrams are rendered automatically by the `mkdocs-mermaid2-plugin`.
- Any Mermaid `flowchart` block in Markdown can be added to docs pages.
- For additional diagram types, see the Mermaid documentation: https://mermaid.js.org/
