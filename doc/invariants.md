# System Invariants

## Core Invariants

### Invariant 1: Origin Immutability
**Rule:** origin.md must never be modified after creation.

**Relies on:**
- File system preserving write timestamps
- Human discipline to not edit the file

**Must not alter:**
- The ability to trace all system decisions back to original intent

**Detection of violation:**
- File modification timestamp differs from creation timestamp
- Git history shows edits to origin.md after initial commit

---

### Invariant 2: State Append-Only
**Rule:** State records must never be deleted or modified. Only new records may be added.

**Relies on:**
- Sequential naming (state-001.md, state-002.md, ...)
- Each record documenting what existed before it

**Must not alter:**
- The ability to reconstruct system evolution from any point

**Detection of violation:**
- Missing sequence numbers in state/ directory
- File modification timestamps on existing state records
- State record content contradicting earlier records without acknowledgment

---

### Invariant 3: No Execution Authority
**Rule:** This system must not execute code, enforce rules, or make decisions.

**Relies on:**
- Absence of executable code
- Absence of automation scripts
- Absence of CI/CD integration

**Must not alter:**
- The declarative, inspection-only nature of the system

**Detection of violation:**
- Presence of .sh, .py, .js, or other executable files
- Presence of Makefile, package.json, or build configuration
- README instructions that say "run" or "execute"

---

### Invariant 4: Zero Assumed Context
**Rule:** Every artifact must be readable in isolation by someone with no prior knowledge.

**Relies on:**
- Explicit documentation of dependencies between artifacts
- No use of pronouns without antecedents
- No references to "we", "our team", or "the project"

**Must not alter:**
- The ability for a stranger to understand the system

**Detection of violation:**
- Use of undefined terms or acronyms
- References to external context not documented
- Assumptions about reader's knowledge or intent

---

## Valid Extension Example

**Proposed addition:** Create a `corrections/` directory for documenting errors in immutable records.

**Declares reliance on:**
- Invariant 1 (origin immutability)
- Invariant 2 (state append-only)

**Declares what it must not alter:**
- The immutability of origin.md
- The append-only nature of state records
- The ability to read original records unchanged

**Why this is valid:**
- Does not modify existing artifacts
- Adds new information without erasing old information
- Maintains ability to trace truth over time
- Does not introduce execution or automation

---

## Invalid Extension Example

**Proposed addition:** Add a script that validates state records are in correct format.

**Why this fails:**
- Violates Invariant 3 (no execution authority)
- Introduces dependency on runtime environment
- Shifts enforcement from structural inspection to automated checking
- Creates obligation to maintain script as system evolves
- Assumes future contributors have compatible execution environment

**What it would alter:**
- The declarative nature of the system
- The ability to inspect without executing
- The independence from tooling and platforms

**Correct alternative:**
- Document the expected format in README.md
- Provide examples of correct and incorrect formats
- Rely on human inspection during handover

---

## How to Extend This System

Before adding anything:

1. Identify which invariants your addition relies on
2. Identify which invariants your addition must not alter
3. Document both explicitly in your addition
4. Verify your addition does not introduce execution, automation, or external dependencies
5. Verify your addition can be understood in isolation

If you cannot complete steps 1-5, the addition violates system invariants.

---

## Detecting Invariant Violations

Violations are detected by inspection, not automation:

- Read origin.md and check file timestamp
- List state/ directory and verify sequential naming with no gaps
- Search codebase for executable files or build configurations
- Read any artifact and verify it defines all terms it uses

No tool will prevent violations.  
Violations are discovered by the next person who reads the system.  
This is intentional.
