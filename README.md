# software-engineering-thinking

*A modular book and a set of point-of-use tools for changing systems without losing control of meaning, evidence, architecture, or ownership.*

This repository can be read linearly, but it should not be operated linearly.

The essays explain forces. The guides intervene at the point of use. The lab preserves observed failures. The forces compress what survived. The epilogue ends the work.

```text
canonical source = the individual files
book = the reading path through them
```

Do not merge the practice guides into one comprehensive manual. Their usefulness depends on being small enough to open at the moment that triggers them.

---

## Read as a book

### Part I — The Theory

Why the work changes when implementation becomes cheap.

1. [`Change Under Constraints`](1.change-under-constraints.md) — the foundational frame.
2. [`The Bottleneck Moves`](2.the-bottleneck-moves.md) — tools reveal the next expensive layer.
3. [`The Cost of Meaning`](3.the-cost-of-meaning.md) — plausible behavior is cheaper than local meaning.
4. [`The Cost of Knowing`](4.the-cost-of-knowing.md) — evidence and grounds do not scale automatically with output.
5. [`Unmade Decisions`](5.unmade-decisions.md) — ambiguity becomes behavior when no one owns the choice.
6. [`Ownership`](6.ownership.md) — work can be delegated; accountability still has to land.

### Part II — The Architecture

How to shape the product and the process that changes it.

7. [`Thinking About Architecture`](7.thinking-about-architecture.md) — boundaries, reversibility, state, data, failure, ownership, and trade-offs.
8. [`The System That Builds the System`](8.the-system-that-builds-the-system.md) — what happens when autonomous builders share state and the workshop becomes another system.

### Part III — The Practice

Do not read this part as one long chapter under pressure. Route by trigger.

9. [`AI Risk Triage`](9.ai-risk-triage.md)
10. [`Moves For Communicating Intent`](10.moves-for-communicating-intent.md)
11. [`Architecture Questions`](11.architecture-questions.md)
12. [`AI Operator Field Guide`](12.ai-operator-field-guide.md)

### Part IV — The Lab

13. [`AI As A Judgment Lab`](13.ai-as-a-judgment-lab.md) — the incident record behind the rules, including uncertainty about causes and controls.

### Part V — The Compression

14. [`Forces of Software Engineering`](14.forces-of-software-engineering.md) — compressed notation as diagrams for thought, not a scoring system.

### Epilogue

15. [`The End`](15.the-end.md) — text, authorship, ownership, and finality.

---

## Route by point of use

- **Before work** — the task may expose sensitive input, use destructive tools, change durable state, or create expensive consequences → [`AI Risk Triage`](9.ai-risk-triage.md)
- **While forming intent** — the request contains missing decisions, tacit standards, unclear acceptance, or authority the model must not invent → [`Moves For Communicating Intent`](10.moves-for-communicating-intent.md)
- **While drawing a boundary** — a service, module, worker, source of truth, deployment split, or multi-agent workspace is being proposed → [`Architecture Questions`](11.architecture-questions.md)
- **While accepting output** — the result feels plausible, aligned, stale, partial, generic, forceful, self-verified, or complete → [`AI Operator Field Guide`](12.ai-operator-field-guide.md)
- **After a failure or near miss** — preserve what happened before polishing it into advice → [`AI As A Judgment Lab`](13.ai-as-a-judgment-lab.md)

---

## The four kinds of knowledge

```text
ESSAY   explains a durable force and its consequences
GUIDE   changes the next action at a specific point of use
LAB     preserves an observed incident and uncertainty around it
FORCE   compresses a surviving idea without calculating the answer
```

Keep those boundaries real.

An incident should not be rewritten as doctrine before the evidence survives. A guide should not become a philosophical essay. An essay should not absorb harness-specific instructions. A force should not become a score, linter, or gate.

---

## The core route for consequential work

```text
triage the task
→ expose missing decisions
→ identify product and workshop boundaries
→ state acceptance criteria and evidence
→ bound action authority
→ implement in small increments
→ verify the current artifacts
→ accept under a named owner
→ record failures that change the rule
```

Do not force low-risk work through the full sequence. The point of triage is to preserve speed where mistakes are cheap.

---

## Two pressures, one attention budget

The practice distinguishes two control problems.

```text
EPISTEMIC PRESSURE
A result may be wrong, ungrounded, unauthorized,
or difficult to verify. One actor is enough.

COORDINATION PRESSURE
Several autonomous actors may collide over shared mutable state.
Plurality and concurrency create it.
```

They are distinct, not uncorrelated. When verification depends on manual review, coordination consumes the same finite attention required for epistemic control. Mechanical evidence is what lets the pressures be managed separately.

---

## Maintenance rules for this repository

1. **Preserve the artifact boundary.** The book is a route through files, not a reason to collapse them into one document.
2. **Keep the trunk durable.** Put temporary model, product, or harness behavior in clearly marked automation codas or point-of-use guides.
3. **Record before generalizing.** New rules should link to incidents, external evidence, or explicit reasoning about the force.
4. **Log failed controls too.** A lab that records only confirming incidents becomes doctrine.
5. **Do not score the coordinates.** One severe property may dominate. The questions locate judgment; they do not replace it.
6. **Keep `The End` last.** Finality is part of the argument.

---

## The single thread

```text
software engineering manages change under constraints.

automation makes production cheaper
and exposes what production used to conceal:
meaning, evidence, decisions, architecture, and ownership.

when builders become plural,
the process that changes the product becomes another system.

make generation easy;
make accidental commitment hard;
make evidence automatic;
make ownership explicit;
make recovery boring.
```

If any of this is useful to you, take it.
