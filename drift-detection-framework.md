# Drift Detection Framework

## Purpose

Make semantic drift visible by inspection alone. No automation. No enforcement. Only structure.

## Semantic Anchors

Semantic anchors are immutable meaning points. They define what cannot change without breaking the system's identity.

### Anchor 1: Declaration vs Enforcement

**Immutable meaning**:
- "Declared" means written down, visible, inspectable
- "Not enforced" means no code runs to check compliance
- These are opposites that define the system boundary

**Drift indicators**:
- If "declared" starts meaning "declared + logged"
- If "not enforced" starts meaning "not *automatically* enforced"
- If declaration implies obligation beyond visibility

### Anchor 2: Inspection vs Execution

**Immutable meaning**:
- "Inspection" means human reading
- "Execution" means machine running
- Detection happens through the first, not the second

**Drift indicators**:
- If inspection requires tooling
- If detection requires computation
- If reading requires interpretation guides

### Anchor 3: Boundary vs Coordination

**Immutable meaning**:
- "Boundary" means separation point
- "Explicit" means clearly stated
- Boundaries divide, they don't connect

**Drift indicators**:
- If boundaries imply synchronization
- If explicit means "explicit + aligned"
- If separation becomes coordination requirement

## Invariant Reference Points

Each invariant has a reference interpretation. Extensions must declare deviation from these references.

### Reference: Invariant 1

**Text**: "Constraints are declared, not enforced"

**Reference meaning**:
- System writes constraints in documents
- System does not check if constraints are followed
- Participants may read, may ignore, may comply
- No obligation exists beyond declaration

**Boundary**: Declaration stops at visibility

### Reference: Invariant 2

**Text**: "No execution authority"

**Reference meaning**:
- System cannot run code to verify behavior
- System cannot trigger actions based on state
- System is passive structure only

**Boundary**: No computational power

### Reference: Invariant 3

**Text**: "Responsibility boundaries are explicit"

**Reference meaning**:
- Each participant's duties are written down
- Boundaries separate participants
- No implicit coordination required

**Boundary**: Independence is preserved

### Reference: Invariant 4

**Text**: "The system remains inspectable"

**Reference meaning**:
- All structure is readable by humans
- No hidden state
- No computation required to understand

**Boundary**: Human-readable only

### Reference: Invariant 5

**Text**: "Detection occurs through inspection"

**Reference meaning**:
- Humans read to detect problems
- No tools required
- No processing required

**Boundary**: Detection is passive observation

### Reference: Invariant 6

**Text**: "Drift is detected structurally"

**Reference meaning**:
- Structure itself reveals drift
- Comparison of documents shows change
- No interpretation history required

**Boundary**: Detection is synchronic, not diachronic

## Semantic Checksum Concept

A semantic checksum is a human-readable summary that makes meaning changes visible.

### Structure

Every extension must include:

```
SEMANTIC CHECKSUM
─────────────────
Original meaning: [one sentence]
Extended meaning: [one sentence]
Delta: [what changed]
Preserved: [what stayed the same]
```

### Example: Compliant Extension

```
SEMANTIC CHECKSUM
─────────────────
Original meaning: System declares constraints for inspection
Extended meaning: System declares constraints for inspection
Delta: Added new constraint type
Preserved: Declaration remains passive, no enforcement added
```

### Example: Drifting Extension

```
SEMANTIC CHECKSUM
─────────────────
Original meaning: Constraints are declared, not enforced
Extended meaning: Constraints are declared with compliance tracking
Delta: Declaration now implies logging obligation
Preserved: No automated enforcement
```

The second example makes drift visible: "implies logging obligation" contradicts "not enforced."

## Extension Declaration Requirements

Every new artifact must include these sections:

### 1. Invariant Reliance Declaration

```
RELIES ON:
- Invariant [number]: [exact text]
  Reference meaning: [from reference points above]
  My interpretation: [how I understand it]
```

### 2. Invariant Preservation Declaration

```
DOES NOT ALTER:
- Invariant [number]: [exact text]
  Preserved aspect: [what remains unchanged]
  Evidence: [how to verify by inspection]
```

### 3. Semantic Delta Declaration

```
SEMANTIC DELTA:
What meaning changed:
- [specific concept]: [old meaning] → [new meaning]

What meaning did not change:
- [specific concept]: [still means the same thing]

Boundary impact:
- [which boundaries expanded/contracted/shifted]
```

### 4. Reinterpretation Declaration

```
REINTERPRETATIONS:
- Invariant [number]:
  Original: [reference meaning]
  Reinterpreted as: [new meaning]
  Justification: [why this is necessary]
  Drift risk: [what could go wrong]
```

## Detection Method

### Step 1: Read Extension

Locate the four required sections above.

### Step 2: Compare to References

For each claimed invariant reliance:
- Read the reference meaning
- Read the extension's interpretation
- Check if they match

### Step 3: Check Semantic Checksum

- Does "extended meaning" match "original meaning"?
- Does "delta" contradict "preserved"?
- Does "preserved" claim match actual changes?

### Step 4: Inspect Reinterpretations

- Is the reinterpretation acknowledged?
- Does it expand obligations?
- Does it shift boundaries?

### Step 5: Cross-Reference

Compare multiple extensions:
- Do they interpret the same invariant differently?
- Do their semantic checksums conflict?
- Do their boundary impacts overlap?

## Drift Visibility Principle

**If an extension omits required sections**: Drift is obvious by absence

**If an extension fills sections incorrectly**: Drift is obvious by contradiction

**If an extension fills sections honestly**: Drift is obvious by comparison

The framework makes drift visible regardless of intent.

## Non-Enforcement Guarantee

This framework:
- Does not run code
- Does not validate automatically
- Does not prevent bad extensions
- Does not reject anything

It only makes drift inspectable.

Enforcement remains human responsibility.
