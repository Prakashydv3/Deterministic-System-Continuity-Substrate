# Extension Template

## Instructions

Copy this template for any new extension to the system.

Fill every section. Empty sections make drift obvious by inspection.

## Extension Metadata

**Extension name**: [short name]

**Author**: [identifier]

**Date**: [YYYY-MM-DD]

**Purpose**: [one sentence describing what this extension does]

## Interpretation Statement

**I interpret this system as**: [one sentence describing the system's purpose]

**This extension serves that purpose by**: [one sentence explaining the connection]

## Invariant Reliance Declaration

List every invariant this extension depends on.

### Invariant [number]

**Exact text**: [copy from origin]

**Reference meaning**: [copy from drift-detection-framework.md]

**My interpretation**: [how you understand this invariant]

**Why I rely on it**: [what breaks if this invariant changes]

---

*Repeat for each relied-upon invariant*

## Invariant Preservation Declaration

List every invariant this extension does NOT alter.

### Invariant [number]

**Exact text**: [copy from origin]

**Preserved aspect**: [what remains unchanged]

**Evidence**: [how to verify by reading the extension]

---

*Repeat for each preserved invariant*

## Semantic Delta Declaration

### What Meaning Changed

**Concept**: [name of concept]

**Original meaning**: [what it meant before]

**Extended meaning**: [what it means after this extension]

**Reason for change**: [why this change is necessary]

---

*Repeat for each changed concept*

### What Meaning Did NOT Change

**Concept**: [name of concept]

**Stable meaning**: [what it still means]

**Evidence**: [how to verify it didn't change]

---

*Repeat for each stable concept*

## Boundary Impact Declaration

### Boundaries Affected

**Boundary**: [name of responsibility boundary]

**Original scope**: [what was included before]

**Extended scope**: [what is included after]

**Expansion justification**: [why this expansion is necessary]

---

*Repeat for each affected boundary*

### Boundaries Preserved

**Boundary**: [name of responsibility boundary]

**Unchanged scope**: [what remains the same]

**Evidence**: [how to verify by inspection]

---

*Repeat for each preserved boundary*

## Reinterpretation Declaration

If you reinterpret any invariant (change its meaning without breaking its text), declare it here.

### Invariant [number]

**Original reference meaning**: [from drift-detection-framework.md]

**Reinterpreted as**: [your new interpretation]

**Justification**: [why this reinterpretation is necessary]

**Drift risk**: [what could go wrong with this reinterpretation]

**Mitigation**: [how to detect if drift becomes harmful]

---

*Repeat for each reinterpreted invariant*

## Semantic Checksum

**Original system meaning**: [one sentence]

**System meaning after this extension**: [one sentence]

**Delta**: [what changed]

**Preserved**: [what stayed the same]

## Structural Addition

Describe what files/directories this extension adds.

```
[directory structure]
```

### [filename]

**Purpose**: [what this file does]

**Content summary**: [brief description]

**Inspection method**: [how to verify it follows the rules]

---

*Repeat for each added file*

## Conflict Declaration

### Potential conflicts with other extensions

**Extension**: [name of potentially conflicting extension]

**Conflict type**: [semantic / boundary / interpretation]

**Description**: [how they might conflict]

**Detection method**: [how to spot the conflict by inspection]

---

*Repeat for each potential conflict*

### Compatibility claims

**Extension**: [name of compatible extension]

**Why compatible**: [explanation]

**Verification**: [how to verify compatibility by inspection]

---

*Repeat for each compatibility claim*

## Rationale

[Explain why this extension is necessary and how it strengthens the system without violating its principles]

## Inspection Checklist

For reviewers to verify this extension:

- [ ] All invariant reliances are declared
- [ ] All invariant preservations are declared
- [ ] Semantic delta is explicit
- [ ] Boundary impacts are documented
- [ ] Reinterpretations are acknowledged
- [ ] Semantic checksum is filled
- [ ] No automation introduced
- [ ] No enforcement code added
- [ ] Structure remains inspectable
- [ ] Drift is detectable by reading

---

## Template Compliance

**This template was filled**: [completely / partially / minimally]

**Omitted sections**: [list any sections left empty]

**Reason for omissions**: [justify any empty sections]
