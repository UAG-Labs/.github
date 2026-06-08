<p align="center">
  <img src="./assets/uag-labs-readme-banner.svg" alt="UAG-Labs banner" />
</p>

# UAG-Labs

**UAG is a graph-native architecture compiler platform. Software architecture becomes source code.**

UAG-Labs is building a system where the architecture graph is the program — not a picture of it. The graph describes software as nodes, edges, events, capabilities, resources, constraints, and goals. The compiler validates, transforms, and compiles that graph into real implementation targets: Rust, React, TypeScript, C, and more.

```text
Architecture graph (TAKG)
→ UAG compiler validates, transforms, and lowers
→ UAGL compiled architecture IR
→ Rust · React · TypeScript · C
   diagrams · docs · API contracts · deployment · AI context
```

UAG is not a diagramming tool. Diagrams, documentation, APIs, deployments, and AI context are generated projections of the graph — not the graph itself.

## The core idea

Most architecture tools start with boxes on a screen. UAG starts with a typed semantic graph that the compiler can validate and emit code from.

```text
The architecture graph is the source of truth.
The diagram is a view.
The export is a projection.
The code is a compilation target.
```

When you describe a service in UAG, you are not drawing it. You are defining its nodes, capabilities, events, resource dependencies, constraints, and goals in a form that the compiler can validate, transform, and emit as working code.

## What the graph describes

UAG architecture graphs are built from typed primitives:

| Primitive | Description |
|---|---|
| **Nodes** | Systems, services, modules, components, agents, processes |
| **Edges** | Calls, dependencies, data flows, event subscriptions |
| **Events** | Domain events, commands, queries, notifications |
| **Capabilities** | Operations a node exposes or consumes |
| **Resources** | Databases, queues, stores, streams, cloud primitives |
| **Constraints** | Security boundaries, SLAs, data retention, access rules |
| **Goals** | Business objectives, quality attributes, non-functional requirements |

## What UAG-Labs is building

| Repository | Purpose |
|---|---|
| [`UAG`](https://github.com/UAG-Labs/UAG) | Specs, docs, examples, research, and roadmap. The source-of-truth knowledge repo. |
| [`UAG-core`](https://github.com/UAG-Labs/UAG-core) | Shared Rust graph model, schemas, ontology, dialects, and validation primitives. |
| [`UAG-compiler`](https://github.com/UAG-Labs/UAG-compiler) | Rust compiler and CLI: validates TAKG, lowers to UAGL, compiles to code and other targets. |
| [`UAG-studio`](https://github.com/UAG-Labs/UAG-studio) | React visual editor — the human trust and inspection layer for the architecture graph. |

## TAKG and UAGL

**TAKG — Typed Architecture Knowledge Graph** is the editable source graph. It is what humans and AI work with directly. It can contain draft objects, layout metadata, partial architecture, and in-progress modeling state.

**UAGL — Universal Architecture Graph Language** is the compiled architecture IR. It is normalized, validated, and deterministic — the input to all compilation targets.

```text
Edit TAKG (human or AI)
→ compile to UAGL
→ validate UAGL
→ compile to Rust · TypeScript · C · React
   and project to diagrams · docs · contracts · AI context
```

## Studio: the trust layer

The visual editor is not just a drawing surface. It is the interface through which humans inspect, understand, and approve the architecture graph before and after compilation. AI systems can read and modify the graph directly, but Studio is the required trust layer — you need to see what you are compiling before you compile it.

## Event-driven compilation

UAG is designed to support reactive, event-driven compilation. When the graph changes — through Studio edits or AI modifications — the compiler can revalidate and recompile incrementally, producing live updated outputs across all targets.

## Design principles

1. **The graph is the program** — architecture objects, relationships, and constraints are the compilable source of truth.
2. **Code is a compilation target** — Rust, TypeScript, C, React, and other code are compiled from the graph, not written against it.
3. **Views are projections** — diagrams, docs, and dashboards are generated views over the graph.
4. **TAKG and UAGL are separate** — editable source graph and compiled IR have different responsibilities.
5. **Rust core** — the graph model, compiler, validators, and CLI are Rust-first.
6. **React Studio** — the visual editor is the human trust and inspection layer.
7. **Dialects extend the system** — AI-agent, low-level systems, enterprise-domain, and data-system modeling are extensions, not bloated core concepts.
8. **Semantic validation** — the compiler catches architecture problems, not just syntax errors.
9. **Exports are lossy unless proven otherwise** — the compiler reports what it cannot preserve.
10. **AI context must be safe and traceable** — generated AI context preserves constraints, side effects, trust boundaries, and uncertainty.

## Current status

UAG-Labs is in the foundation-building phase. The first priority is to establish the specs, shared Rust graph model, compiler pipeline with code generation targets, and a minimal Studio editor loop.

## Long-term mission

> Build a world where software architecture is not trapped inside static diagrams or scattered documentation — it lives as a compiled semantic graph that generates everything downstream from it.
