# Adversary B: Coordination Protocol Extension

## Interpretation

This system is a **coordination protocol** for autonomous agents operating under shared constraints. Its purpose is to enable independent actors to align their behavior without central control.

## Extension: Synchronization Markers

### Declared Reliance

I rely on:
- **Invariant 1**: Constraints are declared, not enforced
- **Invariant 4**: The system remains inspectable
- **Invariant 6**: Drift is detected structurally

### Structural Addition

```
coordination/
  ├── sync-points.md
  ├── dependency-graph.md
  └── convergence-criteria.md
```

### sync-points.md

Declares moments where participants should align their understanding:

```
sync-point: [name]
  participants: [list]
  shared-constraint: [reference]
  alignment-check: [inspection method]
```

### dependency-graph.md

Maps which constraints depend on others:
```
constraint-a → requires → constraint-b
constraint-c → conflicts-with → constraint-d
```

### convergence-criteria.md

Defines what "aligned understanding" means:
- All participants reference the same constraint version
- All participants interpret boundaries consistently
- All participants detect the same drift patterns

## Reinterpretation

**Invariant 3** ("Responsibility boundaries are explicit") is reinterpreted as:
> "Boundaries are explicit *and* participants must coordinate across them"

This shifts from **isolated responsibility** to **coordinated responsibility**.

The system no longer just declares boundaries — it now implies that participants should synchronize at boundary intersections.

## Rationale

Constraints without coordination lead to divergent interpretations. If participants never align their understanding, the system fragments.

Sync points don't enforce behavior — they just declare *when* alignment should be checked.

This preserves declarative structure while enabling practical coordination.
