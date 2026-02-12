# Handover Document

Someone who does not know me, does not trust me, and does not share my context

## What This Is

This is a system for preserving truth across time when contributors change.

It is not:
- A product
- A framework
- A tool you must use
- A set of instructions you must follow

You have no obligation to continue this work.

## How to Understand This System From Scratch

### Step 1: Read origin.md

This file explains:
- Why this system exists
- What it intentionally does not do
- What assumptions are rejected

Read it first. It is immutable and will never change.

If origin.md has been modified (check file timestamp), the system has been corrupted.

### Step 2: Read state records in sequence

State records are in the `state/` directory, named `state-001.md`, `state-002.md`, etc.

Each record contains:
- What existed at start of that day
- What was added
- What was explicitly not changed
- What remains unresolved

Read them in order. Each record assumes you have read all previous records.

If any state record is missing or modified, the continuity is broken.

### Step 3: Read invariants.md

This file declares rules that prevent the system from drifting.

It contains:
- Core invariants that must not be violated
- Examples of valid extensions
- Examples of invalid extensions

Invariants are not enforced by code. They are enforced by inspection.

### Step 4: Read README.md

This file explains how to use the system artifacts.

It does not explain why they exist (that is in origin.md).  
It does not tell you what to do next (that is your decision).

## How to Decide What to Do Next

This system does not prescribe your next action.

You may:
- Continue adding to the system
- Stop work entirely
- Use this pattern elsewhere
- Reject this approach

If you continue:
- Create state-003.md documenting what exists now
- Add new artifacts that respect invariants
- Do not modify origin.md or existing state records
- Do not add execution, automation, or external dependencies

If you stop:
- No action required
- The system remains readable by the next person
- Nothing will break

## How to Safely Stop Work

To stop work safely:

1. Ensure the most recent state record documents current state
2. Commit all files
3. Stop

You do not need to:
- Announce your departure
- Document why you stopped
- Prepare the system for future work
- Ensure someone else continues

The system is designed to be resumed from any state record by anyone.

## What If You Disagree With This System

If you find this system incorrect, unnecessary, or harmful:

1. Do not modify origin.md or state records
2. Create a new document explaining your disagreement
3. Reference the specific artifacts you disagree with
4. Explain what assumption or invariant you reject

Your disagreement becomes part of the record.  
It does not erase what came before.

## What If You Find an Error

If you find an error in an immutable record:

1. Do not correct the original
2. Create a new artifact documenting the error
3. Reference the incorrect artifact by name
4. Explain what is incorrect and why

The error remains visible.  
The correction is added.  
Both are preserved.

## What This System Cannot Do For You

This system cannot:
- Tell you if your work is correct
- Prevent you from making mistakes
- Ensure future contributors understand your intent
- Guarantee this work will be useful
- Make decisions on your behalf

It can only:
- Preserve what was done
- Preserve what was not done
- Preserve what was intentionally left unresolved

## Trust and Authority

You should not trust this document.

You should verify:
- That origin.md is immutable (check timestamp)
- That state records are sequential and unmodified
- That no executable code exists
- That all claims can be independently verified

This document grants you no authority.  
It imposes no obligation.  
It makes no promises about the future.

## If You Are Reading This Years Later

If significant time has passed:

1. Verify origin.md still exists and is unmodified
2. Read all state records in sequence
3. Check for gaps or modifications
4. Decide if the system still serves its purpose

If the system has drifted from its origin, that drift is visible in the state records.

If the system has been abandoned, the last state record shows when and in what state.

If the system has been corrupted, the violations are detectable by inspection.

## Final Note

This system exists because context is lost and contributors change.

If you have full context and stable contributors, you do not need this system.

If you have neither, this system allows you to start from zero.

That is all it does.
