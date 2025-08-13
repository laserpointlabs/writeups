## Subsystems in BFO-Inspired SE Ontology

Subsystems fit naturally within our foundational ontology as hierarchical aggregates, building on the system definition (non-summative whole with MSD). A system is an aggregate of components via MSD, but subsystems introduce nesting: A subsystem is itself a system (i.e., subsystem ≡ system in core properties—MSD, non-summative unity) embedded within a larger structure, often an artifact. This aligns with BFO's mereotopology, where parts (subsystems) maintain identity while contributing to wholes. For example, hydraulics (system) within an aircraft (artifact) is a subsystem, not diminishing its systemic nature.

Key: No need for special "subsystem" class at foundational level—it's a system delimited by boundaries (fiat or bona fide) for scoping. This supports modular growth: Extend via OWL imports without altering base chain.

## Relation to Artifacts and Boundaries

Yes, a subsystem is a system within an artifact, where (subsystem == system) holds—same MSD criteria apply, but contextually nested. Delineation uses BFO boundaries:
- **Fiat Boundary**: Human-imposed (e.g., engineering-defined scope in ICDs, like "avionics subsystem" bounded by design docs). When this exists, the system is treated as a subsystem for hierarchical modeling, enabling traceability (e.g., query paths from artifact-level Requirement to subsystem Function).
- **Bona Fide Boundary**: Physical (e.g., enclosure of hydraulics pipes/valves). If absent, fallback to fiat for abstract subsystems (e.g., software modules).

This avoids over-theorizing: Boundaries are practical for SE workflows (e.g., LLM extraction of bounded entities from CDDs), reducing churn in variant convergence.

Critique: Treating subsystem == system risks recursive dilution if not constrained—e.g., infinite nesting without testability. Balance: Tie to applied tests (e.g., removal breaks parent but not subsystem identity), echoing experience where unconstrained hierarchies stalled projects.

## Evidence from BFO Literature (via Tool Search)

Web searches confirm BFO's emphasis on fiat boundaries for delineating aggregates in domains like geospatial and engineering (e.g., ISO/IEC 21838-2 standardizes BFO for interoperability). Key snippets: Fiat boundaries address vagueness in sharp demarcations (Wikipedia); applied to engineering for part-whole relations without physical basis (ScienceDirect on SE ontologies); fiat surfaces lack full axiomatization but imply human-imposed hugging of material entities (ResearchGate paper on fiat surfaces, e.g., "every fiat surface has its location determined in relation to some material entity"). No direct BFO subsystem class, but extensions use boundaries for nested wholes (e.g., in DOLCE comparisons, subsystems via homeomericity/cumulativity). This supports our view without over-theorizing—use for practical SE like subsystem scoping in air vehicle models.

## Mathematical Sketch for Subsystems

Extend system definition hierarchically: Let S be a system (S = ∑{c_i} with MSD ∀ c_j, c_k ∈ S). A subsystem S' ⊆ S where S' satisfies MSD independently, delimited by boundary B (fiat or bona fide). Formally:  
\[ S' \subseteq S \land \forall c \in S', \, \exists B \, (B \text{ bounds } S' \land \text{MSD holds in } S') \]  
Here, "bounds" as BFO relation (e.g., fiat B hugs material aggregate). Ties to mereology: Part(S', S) iff P(S', S) ∧ S' ≠ S. Non-breaking: Add as OWL axiom in extensions, validate with SHACL (e.g., minCount 1 boundary per subsystem).

## Additional Tests for Subsystem Delineation

Build on prior checklist; prioritize testability in workflows (e.g., NetworkX simulation of nested graphs for breakage checks).

| Test | Description | Example (Hydraulics as Subsystem in Aircraft) | BFO Tie | Applied Benefit |
|------|-------------|----------------------------------------------|---------|-----------------|
| Nested MSD | Subsystem maintains MSD within boundary, independent of parent | Yes (fluid-pipe dependence holds locally) | Dependence relations | Enables modular ICD extraction (LLM parses subsystem variants without artifact churn) |
| Boundary Coherence | Fiat/bona fide boundary encloses without overlap conflicts | Yes (fiat scope in design docs) | Fiat boundaries for vagueness | Reduces modeling time (minutes vs. weeks) via SHACL validation of bounds |
| Hierarchical Traceability | Paths from parent Requirement to subsystem Function intact | Yes (query chains preserve nesting) | Continuants in unity | Supports Git merges for non-breaking evolution |
| Identity Preservation | Subsystem retains system properties post-parent change | Yes (hydraulics functional if aircraft modified) | Non-summative wholes | Critiques overfocus: Test with "show me" prototypes (e.g., SymPy for dependence calcs) |
| Scalability | Can nest further subsystems without dilution | Yes (valves as sub-subsystem) | Mereological sums | Constraints innovation: Limited nesting via catalogs avoids complexity |

## Critique and Non-Breaking Integration

Critique: Equating subsystem == system with fiat boundaries risks bias toward human-centric views (e.g., ignoring emergent bona fide subsystems in biology-inspired SE), potentially diluting applied focus if not tested (echoing 95% application rule). Evidence: BFO applications in engineering (e.g., ScienceDirect) show boundaries streamline interoperability but warn against unvalidated axioms. Balance: Introduce in first-order paper as FOL extension (static axioms for nesting), simulate with code (e.g., NetworkX nested graphs) to check traceability breakage. Keeps foundational paper intact—add teaser in "Extension" section.