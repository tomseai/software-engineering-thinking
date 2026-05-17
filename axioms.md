# Axioms of Software Engineering

> Software engineering is the management of change under constraints.

These are compressed notes, not laws.

They are useful because they name forces, not because they calculate outcomes.
Notation compresses intuition. It does not replace it.

Read them as reminders, not instructions.

---

## On notation

Notation is compressed judgment.

A formula can name the forces in a system, but it cannot tell you which force matters most here, now, under these constraints. That part is judgment.

This is why best practices fail when copied without context. The notation survives. The intuition does not.

It is also why AI output can feel more mature than it is. A model can reproduce the language of engineering judgment without carrying the consequences that produced that judgment.

---

## 1. The Foundational Axiom

$$
\text{Software Engineering} \approx \operatorname{Manage}(\Delta \text{System} \mid \text{Constraints})
$$

Software engineering is not primarily the act of writing code.
It is the discipline of changing a system without losing control of it.

The constraints may be technical, human, economic, temporal, organizational, regulatory, or political.

---

## 2. The Complexity Axiom

$$
\text{Complexity} \approx \text{State Space} + \sum_{e \in \text{Coupling Graph}} \text{Weight}(e) \cdot \text{Change Rate}(e)
$$

Isolated things are cheap.
Coupled things that change are expensive.

Complexity does not come from the number of parts alone.
It comes from the relationships between parts, especially when those relationships must survive change.

---

## 3. The Architecture Axiom

$$
d \in \text{Architecture} \iff \text{Cost}_{reverse}(d) \gg 0
$$

Architecture is the set of decisions that are expensive to reverse.

This is why architecture is not “the folder structure” or “the framework.”
Architecture is where reversibility is low: data ownership, service boundaries, deployment topology, consistency model, security model, and long-lived contracts.

---

## 4. The Boundary Axiom

$$
\text{Quality}_{boundary} \approx \frac{\text{Independent Change}}{\text{Required Shared Context}}
$$

A good boundary allows one side to change without forcing the other side to understand its internals.

A weak boundary is not weak because it has the wrong name.
It is weak because change crosses it too easily.

---

## 5. The Correctness Axiom

$$
\forall f \in \text{Flows}:\quad \text{Invariants}_{before} \Rightarrow \text{Invariants}_{after}
$$

Correctness means invariants survive every valid flow.

The happy path is not correctness.
Correctness is what remains true after retries, failures, edge cases, reordering, concurrency, bad input, partial updates, and human mistakes.

---

## 6. The State Axiom

$$
\text{State Complexity} \approx \text{Possible States} \times \text{Transitions} \times \text{Lifetime}
$$

Long-lived mutable state is where systems become difficult.

The most dangerous states are not the valid ones.
The dangerous states are the invalid ones the system accidentally allows itself to represent.

---

## 7. The Maintainability Axiom

$$
\text{Maintainability} \approx \text{Local Reasoning} + \text{Fast Feedback} + \text{Change Locality}
$$

A system is maintainable when a developer can understand the relevant part, change it locally, and verify the result quickly.

Maintainability is not aesthetic cleanliness.
It is the ability to make safe changes at acceptable cost.

---

## 8. The Abstraction Axiom

$$
\text{Value}_{abstraction} \approx \text{Coupling Reduced} - \text{Indirection Added} - \text{Generality Debt}
$$

An abstraction is only good if it removes more complexity than it introduces.

Bad abstractions are worse than duplication:

$$
\text{Cost}_{wrong\ abstraction} \gg \text{Cost}_{duplication}
$$

Duplication is visible.
A wrong abstraction becomes infrastructure for misunderstanding.

---

## 9. The Technical Debt Axiom

$$
\text{Interest}_{debt} \approx \text{Change Frequency} \times \text{Friction per Change} \times \text{Coupling Radius}
$$

Technical debt is not equally important everywhere.

Debt in code that never changes may be harmless.
Debt in code that changes every week compounds aggressively.

The priority is not “clean the code.”
The priority is “reduce friction where change repeatedly hurts.”

---

## 10. The Test Value Axiom

$$
\text{Value}_{test} \approx \text{Confidence Gained} - \text{Maintenance Cost}
$$

A test is valuable when it increases confidence more than it slows change.

Coverage is not confidence.
A good test suite protects behavior.
A bad test suite protects implementation details.

---

## 11. The Delivery Axiom

$$
\text{Delivery Speed} \approx \frac{\text{Feedback Speed}}{\text{Coordination Cost}}
$$

Teams rarely move slowly because people type slowly.

They move slowly because feedback is delayed, ownership is unclear, dependencies are deep, decisions are blocked, or every change requires coordination across too many boundaries.

---

## 12. The Distributed Systems Axiom

$$
\text{Pain}_{distributed} \approx \text{Network Reality} \times \text{Coupled Invariants}
$$

Where:

$$
\text{Network Reality} = \text{Latency} + \text{Partial Failure} + \text{Retries} + \text{Duplication} + \text{Version Skew} + \text{Observability Gaps}
$$

Distributed systems are painful when local assumptions become false.

A distributed system is not just a bigger local system.
It is a system where time, failure, identity, ordering, and visibility become first-class design problems.

---

## 13. The Production Axiom

$$
\text{Operability} \approx \text{Observability} + \text{Recoverability} + \text{Understandability}_{under\ stress}
$$

A system is not production-ready merely because it works.

It is production-ready when humans can understand it during failure, observe what matters, and recover without heroics.

Pretty architecture diagrams do not matter during an incident unless they help someone restore service.

---

## 14. The Ambiguity Axiom

$$
\text{Structural Debt} \approx \text{Requirements Ambiguity} \times \text{Implementation Irreversibility}
$$

Ambiguity does not disappear.

If unresolved, it becomes edge cases, rework, inconsistent behavior, product exceptions, support burden, and eventually architecture.

Bad requirements are one of the most expensive forms of technical debt.

---

## 15. The Sociotechnical Axiom

$$
\text{Architecture}_{system} \approx \text{Communication Topology}_{organization}
$$

Systems tend to inherit the communication structure of the people who build them.

And ownership only works when three things exist together:

$$
\text{Ownership Quality} \approx \text{Responsibility} \times \text{Authority} \times \text{Context}
$$

Responsibility without authority creates frustration.
Authority without context creates bad decisions.
Context without ownership creates commentary.

Software architecture is never purely technical.
It is technical structure embedded in human structure.

---

## 16. The Generated Work Axiom

$$
\text{Risk}_{generated} \approx \text{Fluency} \times \text{Distance}(\text{Author}, \text{Meaning}) \times \text{Irreversibility}
$$

Generated output becomes dangerous when it sounds coherent but the author is far from the meaning.

Fluency lowers suspicion.
Distance lowers judgment.
Irreversibility raises cost.

This applies to AI-generated code, documentation, requirements, architecture proposals, summaries, and decisions.

---

## Final Compression

$$
\text{Software Engineering} \approx \operatorname{Manage}(\Delta \text{System} \mid \text{Constraints})
$$

$$
\text{Complexity} \approx \text{Coupled Relationships Under Change}
$$

$$
\text{Architecture} \approx \text{Expensive-to-Reverse Decisions}
$$

$$
\text{Correctness} \approx \text{Invariants Preserved Across Flows}
$$

$$
\text{Maintainability} \approx \text{Local Reasoning} + \text{Fast Feedback} + \text{Change Locality}
$$

$$
\text{Delivery Speed} \approx \frac{\text{Feedback Speed}}{\text{Coordination Cost}}
$$

$$
\text{Operability} \approx \text{Understandability Under Stress}
$$

$$
\text{Software Quality} \approx \text{Usefulness} + \text{Correctness} + \text{Changeability} + \text{Operability}
$$

---

The deepest practical rule:

> Optimize for the next change without destroying the present system.
