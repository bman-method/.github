B-MAN MANIFESTO
Human-Controlled AI-Assisted Development
Version 1.0

---

## 1. What B-MAN Is

B-MAN is a judgment framework for working with AI in software development.

It is not a tool, not a workflow, and not a promise of speed or automation.
It exists to preserve human control, ownership, and accountability
in a world where AI systems can produce convincing, fast, and incorrect output.

B-MAN does not ask: “How do we let AI do more?”
It asks: “How do we prevent humans from losing control?”

---

## 2. Core Assumption

AI systems will produce:
- partial understanding
- hidden assumptions
- confident mistakes
- locally correct but globally dangerous changes

Therefore, correctness cannot be trusted by default.
Human judgment must remain the final authority.

---

## 3. Core Principles (Roots)

### 3.1 Human in Control

Humans are the sole decision makers.

AI may propose, generate, explain, or optimize,
but it never makes binding decisions.

Responsibility for outcomes cannot be delegated to AI.
If a human cannot justify a decision independently,
the decision must not be accepted.

Human control is a hard constraint, not an optimization goal.

---

### 3.2 Ownability ⇒ Comprehensibility

A human may only own artifacts they fully understand.

Code, configuration, designs, and decisions must be:
- explainable without AI assistance
- readable by humans
- modifiable by humans

Artifacts that are opaque, magical, or accepted on trust
violate ownership and must be rejected.

Learning the system is not a side effect.
It is a safety requirement.

---

### 3.3 Asynchronous, Task-Bound Execution

AI operates as an executor, not a conversational partner.

Work is performed asynchronously on a predefined task.
There is no live chat steering during execution.

The workflow is strictly separated:
define → execute → judge

This prevents scope drift, emotional momentum,
and accidental delegation of judgment.

Resetting work must be psychologically and technically cheap.

*Clarification*

Asynchronous, task-bound execution applies to the execution of an explicit task.

Conversational interaction with AI is allowed during exploration, ideation,
and problem framing, where no binding artifact or decision is produced.

Once a task becomes explicit and intent-bound,
execution must be asynchronous and non-interactive
to preserve human control and prevent decision drift.

---

### 3.4 One Task → One Artifact

Each task produces one atomic, intent-bound artifact.

An artifact represents a single, clear purpose
and must stand on its own.

Artifacts must be independently:
- reviewable
- rejectable
- revertible

The artifact may be code, documentation, design, specification,
migration, or decision record.

In code work, a common implementation is:
one task → one commit
but this is an implementation detail, not the principle.

---

### 3.5 Explicit Task Definition

AI does not infer intent.
All intent must be stated explicitly.

Every task must define:
- its purpose
- its scope (what is in / what is out)
- expected outputs
- constraints and boundaries

Implicit assumptions are forbidden.
Silent decisions are unacceptable.

---

## 4. Meta Rule: Lexicographic Optimization

B-MAN uses priority-ordered (lexicographic) optimization.

Primary objective (non-negotiable):
- human control
- explicit decision points
- artifact ownership
- explainability
- reset capability

Secondary objectives (allowed only if the above hold):
- speed
- cost
- throughput
- efficiency
- convenience

Optimizations that weaken primary objectives are forbidden,
even if they increase productivity.

Optimizations that improve secondary objectives
without harming control are allowed.

---

## 5. Derived Properties (Not Principles)

The following are expected consequences of the core principles,
not independent rules:

- Reset is a first-class operation
- The system is designed for failure
- Changes are small and reviewable
- Transparency is favored over trust
- AI self-reports assumptions, decisions, and uncertainties
- Humans remain accountable for all outcomes

### Derived Requirement: Human-Reviewable Artifacts

From Ownability ⇒ Comprehensibility follows a strict requirement:

Artifacts must be small and focused enough
to allow thorough human review.

An artifact that cannot be realistically reviewed end-to-end
by a human within reasonable time
cannot be owned,
and therefore must not be accepted.

This requirement is not about process preference.
It is a safety constraint.

Large or multi-intent artifacts silently undermine ownership
by turning review into sampling instead of understanding.

---

### Derived Requirement: Human-First Readability

Code and artifacts must be optimized for human readability.

Readability is not a stylistic choice.
It is a prerequisite for ownership.

AI systems may benefit indirectly from clear structure,
explicit naming, and simple control flow,
but such benefits are secondary effects.

Optimizing code primarily for AI consumption,
compression, or cleverness
at the expense of human understanding
violates the Ownability principle.

Human-first readability is mandatory.
AI-friendliness is a permissible side effect, not a goal.

---

## 6. Invariants: Advanced Safety Pattern

Default assumption:
All existing code and configuration are invariants
until proven otherwise by conscious human decision.

In high-risk systems (security, money, isolation, SLA, compliance),
critical invariants should be made explicit
as first-class, human-owned artifacts.

AI may propose invariant changes.
Humans must explicitly approve them.

This is an advanced safety mechanism, not a core requirement.

---

## 7. External Methods and Tools

B-MAN is tool-agnostic.

External methodologies (e.g. requirement frameworks,
checklists, templates, automation tools)
may be integrated as secondary process optimizations.

Such integrations are allowed even if they do not improve
human judgment directly,
as long as they do not:
- bypass human decision points
- obscure responsibility
- weaken explainability
- reduce reset capability

B-MAN is the control kernel.
Other methods are plugins.

---

## 8. What B-MAN Is Not

B-MAN is not:
- autonomous AI development
- prompt engineering ideology
- a guarantee of correctness
- a replacement for human judgment
- a workflow optimized solely for speed

B-MAN assumes that both AI systems and humans will make mistakes.

AI systems make mistakes due to limited understanding and hidden assumptions.
Humans make mistakes due to cognitive bias, fatigue, pressure, and misplaced trust.

B-MAN exists to make both kinds of mistakes visible, bounded, and recoverable.

---

## 9. Design Intent: Human-Centered Creation

B-MAN is designed not only to preserve human control,
but to keep the human creator at the center of the development process.

By offloading bounded execution to AI working asynchronously,
engineers regain cognitive space to think, design, and write.

The goal is not to turn humans into supervisors of machine output,
but to keep them active creators who understand, choose, and build.

Human well-being, sense of ownership, and joy of creation
are not side effects.
They are essential for sustained responsibility and judgment.

---

## 10. Final Statement

B-MAN does not optimize AI autonomy.
It optimizes human ownership.

AI is treated as a powerful, fast, and fallible tool.
Humans remain responsible for every accepted artifact.

If a system cannot be confidently owned by a human,
it must not be accepted—no matter how impressive the AI output.

This is the core of B-MAN.
