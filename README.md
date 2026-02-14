# Deterministic System Continuity Substrate

This repository contains a system for preserving truth across time when contributors change.

Files:
- `origin.md` - Immutable record of system purpose
- `state/` - Directory of daily state records
- `invariants.md` - Rules preventing semantic drift
- `HANDOVER.md` - Instructions for zero-context resumption
- `drift-detection-framework.md` - Semantic anchors and detection mechanism
- `extension-template.md` - Mandatory disclosure form for extensions
- `adversary-a.md`, `adversary-b.md`, `adversary-c.md` - Adversarial extension simulations
- `continuity-conflict-analysis.md` - Drift analysis across adversaries
- `SIMPLE-EXPLANATION.md` - Plain-language task explanation
- `README.md` - This file

## How to Use These Artifacts

### Reading the System

1. Start with `origin.md` to understand what this system is and is not
2. Read state records in `state/` directory in sequential order (state-001.md, state-002.md, ...)
3. Read `invariants.md` to understand what must not change
4. Read `HANDOVER.md` if you are resuming work without prior context

### Understanding State Records

Each state record documents:
- What existed at start of day
- What was added
- What was explicitly not changed
- What remains unresolved

State records are append-only. They are never modified or deleted.

To understand current state: read the most recent state record.  
To understand history: read all state records in sequence.

### Understanding Origin

`origin.md` is immutable. It is never modified after creation.

If you need to clarify or correct the origin, create a new document that references it.  
Do not edit the original.

### Understanding Invariants

Invariants are rules that prevent the system from drifting.

They are not enforced by code.  
They are enforced by inspection.

Before adding anything to this system, read `invariants.md` and verify your addition does not violate any invariant.

### How Origin Is Used

Origin is used as:
- The reference point for all future decisions
- The boundary of system responsibility
- The record of rejected assumptions

Origin is not used as:
- A vision statement
- A roadmap
- A motivational document

When making changes, reference origin to verify the change aligns with original purpose.  
Do not modify origin to align with your change.

### How State Records Are Used

State records are used to:
- Reconstruct system evolution from any point
- Understand what was intentionally not done
- Identify unresolved questions

State records are not used to:
- Plan future work
- Justify past decisions
- Tell a story

When adding to the system, create a new state record documenting what changed.  
Do not modify previous state records.

## How to Add to This System

If you are continuing this work:

1. Read all existing state records
2. Create a new state record (next sequential number)
3. Document what existed at start of your work
4. Document what you added
5. Document what you explicitly did not change
6. Document what remains unresolved
7. Verify your additions respect invariants in `invariants.md`

Do not:
- Modify `origin.md`
- Modify existing state records
- Add executable code
- Add automation
- Add external dependencies

## How to Stop Work

To stop work:

1. Ensure the most recent state record documents current state
2. Commit all files
3. Stop

No other action is required.

## How Continuity Is Preserved

Continuity is preserved through:

1. **Immutability of origin** - The purpose never changes
2. **Append-only state** - History is never rewritten
3. **Explicit invariants** - Drift is detectable by inspection
4. **Zero-context handover** - Anyone can resume from any point

Continuity is not preserved through:
- Shared memory between contributors
- Continuous presence of original author
- Enforcement via automation
- Assumed trust or alignment

## What This System Does Not Provide

This system does not:
- Execute code
- Enforce rules automatically
- Make decisions
- Prescribe future direction
- Guarantee usefulness
- Require continuation

## Verification

To verify system integrity:

1. Check that `origin.md` has not been modified (compare file timestamp to creation date)
2. Check that state records are sequential with no gaps (state-001.md, state-002.md, ...)
3. Check that no executable code exists in the repository
4. Check that all artifacts can be read in isolation

If any check fails, the system has been corrupted.

## How Drift Detection Works

Semantic drift is detected structurally through:

1. **Semantic Anchors** (drift-detection-framework.md) - Define immutable meanings and reference interpretations
2. **Extension Template** (extension-template.md) - Forces explicit declaration of meaning changes
3. **Detection Method** - Compare declarations to references, check for contradictions

Drift becomes visible through:
- **Absence** - Missing required sections in extensions
- **Contradiction** - Claims vs actual changes
- **Comparison** - Conflicting interpretations across extensions

No automation. No enforcement. Only inspection.

## Questions This README Does Not Answer

- Why does this system exist? (See `origin.md`)
- What should I do next? (Your decision)
- Is this approach correct? (Verify independently)
- Should I continue this work? (Your decision)

This README explains how to use the artifacts.  
It does not explain what they mean or why they should be followed.
