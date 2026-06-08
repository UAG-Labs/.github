<!--
Place this file at:
UAG-Labs/.github/profile/README.md

This is the public organization profile README shown on the UAG-Labs GitHub organization overview page.
-->

# UAG-Labs

**Universal Architecture Graphs for software, systems, runtime, data, AI agents, and infrastructure.**

The only systems architecture suite you will ever need.

UAG-Labs is building a graph-native architecture modeling ecosystem where the architecture graph is the source of truth. Diagrams, documentation, API specs, deployment files, validation reports, and AI-readable context are generated projections from that graph.

```text
TAKG source graph
→ UAG compiler
→ UAGL compiled architecture IR
→ diagrams · docs · contracts · deployment stubs · AI context
```

## Core idea

Most architecture tools start with drawings.

UAG starts with a typed semantic graph.

A normal diagram might show:

```text
Web App → API Server → Database
```

UAG is designed to preserve the deeper architecture meaning:

```text
FrontendApp calls BackendService over HTTPS.
BackendService exposes operations with contracts.
BackendService writes to a Database under a security boundary.
Database has ownership, retention, classification, and runtime constraints.
```

The central rule:

```text
The graph is the truth.
The diagram is a view.
The export is a projection.
```

## What UAG-Labs is building

UAG-Labs is organized around four initial repositories:

| Repository | Purpose |
|---|---|
| [`UAG`](https://github.com/UAG-Labs/UAG) | The main project repository for specs, docs, examples, research, roadmap, and system-level context. |
| [`UAG-core`](https://github.com/UAG-Labs/UAG-core) | Shared Rust graph model, schemas, ontology, dialects, and validation primitives for TAKG and UAGL. |
| [`UAG-compiler`](https://github.com/UAG-Labs/UAG-compiler) | Rust compiler and CLI for transforming TAKG source graphs into UAGL compiled architecture IR and generated outputs. |
| [`UAG-studio`](https://github.com/UAG-Labs/UAG-studio) | React and Rust visual architecture graph editor for creating, validating, compiling, and exporting UAG projects. |

## TAKG and UAGL

UAG uses two related formats:

### TAKG — Typed Architecture Knowledge Graph

TAKG is the editable source graph.

It is what the visual editor works with. It can contain draft objects, layout data, partial architecture, editor metadata, and in-progress modeling state.

```text
.takg.yaml = editable architecture source graph
```

### UAGL — Universal Architecture Graph Language

UAGL is the compiled architecture IR.

It is normalized, resolved, deterministic, validated, and suitable for export, analysis, and AI context generation.

```text
.uagl.yaml = compiled architecture intermediate representation
```

The intended workflow:

```text
Edit TAKG
→ compile to UAGL
→ validate UAGL
→ export from UAGL
```

## What the graph can model

UAG is designed to model architecture across a wide range of abstraction levels:

```text
business capabilities
bounded contexts
software systems
applications
services
modules
APIs
events
data contracts
databases
queues
streams
AI agents
MCP servers
model providers
runtime processes
threads
deployment environments
cloud infrastructure
operating system concepts
low-level hardware/software interfaces
validation rules
generated artifacts
```

The goal is not to flatten all of these into the same kind of box. The goal is to preserve their layer, plane, scope, fidelity, provenance, and relationships.

## Design principles

UAG-Labs is built around these principles:

1. **Graph first** — architecture objects and relationships are the source of truth.
2. **Views are projections** — diagrams are generated views over the graph.
3. **Exports are lossy unless proven otherwise** — every serious export should be able to report what it cannot preserve.
4. **TAKG and UAGL are separate** — editable source graph and compiled IR have different responsibilities.
5. **Rust for system-level implementation** — the core model, compiler, validators, and CLI are Rust-first.
6. **React for the visual editor** — Studio uses React, TypeScript, and a graph canvas UI.
7. **Dialects extend the system** — AI-agent, low-level systems, enterprise-domain, and data-system modeling should be extensions, not bloated core concepts.
8. **Validation must be semantic** — the system should catch architecture problems, not just syntax errors.
9. **High-level and low-level architecture need guardrails** — abstraction boundaries, time domains, safety constraints, and runtime/physical distinctions must be explicit.
10. **AI context must be safe and traceable** — generated AI context should preserve constraints, side effects, trust boundaries, and uncertainty.

## Initial implementation direction

The first complete implementation should support:

```text
1. Write or edit a TAKG file.
2. Parse and validate the TAKG source graph.
3. Compile TAKG into UAGL.
4. Validate the compiled UAGL graph.
5. Export useful artifacts from UAGL.
6. Open and edit the architecture visually in UAG Studio.
```

Initial export targets should include:

```text
Mermaid
D2
Markdown architecture summaries
OpenAPI
AsyncAPI
AI context YAML/JSON
```

Future export targets may include:

```text
Docker Compose
Kubernetes YAML
Terraform stubs
Structurizr
LikeC4
package/database formats
```

## Current status

UAG-Labs is currently in the foundation-building phase.

The organization is starting with empty repositories and system-level documentation. The first priority is to establish the specs, shared Rust model, compiler pipeline, and minimal Studio editor loop.

The first milestone is:

```text
UAG specs and examples
→ UAG-core Rust object model
→ UAG-compiler TAKG-to-UAGL compile path
→ UAG-studio minimal visual editing prototype
```

## Long-term vision

UAG-Labs aims to become a complete architecture compiler ecosystem.

The future direction includes:

```text
visual architecture editing
architecture-as-code
semantic validation
compiler diagnostics
architecture diffing
loss reports
generated docs
generated diagrams
generated API specs
generated event contracts
AI-readable architecture context
package formats
queryable architecture databases
dialect and plugin systems
MCP tools for architecture graph inspection
runtime drift detection
simulation and verification support
```

The long-term mission:

> Make architecture graph-native, typed, validatable, compilable, searchable, diffable, and understandable by both humans and AI systems.

UAG-Labs is building toward a world where architecture is not trapped inside static diagrams or scattered documentation, but lives as a compiled semantic graph.
