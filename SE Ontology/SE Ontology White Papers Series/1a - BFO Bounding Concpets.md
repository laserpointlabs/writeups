## BFO Boundary Concepts

Based on Barry Smith and Achille Varzi's work in Basic Formal Ontology (BFO), boundaries are divided into two types: bona fide and fiat. Bona fide boundaries are physical, grounded in spatial discontinuities or qualitative differences (e.g., the surface of a tennis ball or a person's skin). Fiat boundaries are human-imposed, lacking physical basis (e.g., national borders or the equator). This distinction supports ontological modeling of spatial entities, resolving issues like contact and separation. In SE contexts, bona fide boundaries suit physical systems (e.g., component interfaces), while fiat boundaries apply to conceptual divisions (e.g., subsystem demarcations in designs).

## Relevance to Foundational SE Ontology

Our current definition emphasizes mutual specific dependence (MSD) for systems as non-summative wholes, distinguishing them from artifacts (e.g., hydraulics qualify due to fluid-pipe interdependence; aircraft do not). Boundaries align with BFO's spatial topology, potentially enhancing delineation—e.g., a system's boundary could define its unity, preventing arbitrary aggregates. This ties to traceability in the chain (e.g., Interfaces as boundary entities). However, at the foundational level, boundaries might be implicit in MSD, as dependence often implies spatial or functional enclosure.

## Potential Addition at Foundational Level

Adding "a system must have a boundary" could strengthen the definition by requiring explicit demarcation, using BFO's bona fide/fiat split. For instance: Systems require a bona fide boundary for physical integrity (e.g., enclosed hydraulics) or fiat for conceptual ones (e.g., defined subsystem scopes). This avoids vagueness in SE practices, like ambiguous subsystem partitioning in ICDs. Pros: Improves modularity (e.g., SHACL validation for boundary properties); supports practical workflows (e.g., LLM extraction of bounded entities from docs). Cons: Risks over-theorizing if not tied to application—keep it ≤5% theory by linking to tests like graph boundary detection in NetworkX simulations.

## Critique and Balance

Critique: Adding boundaries might bias toward spatial/physical systems, underrepresenting abstract ones (e.g., software systems without clear fiat boundaries), diluting the applied focus. Evidence from BFO applications (e.g., in biology via web searches) shows boundaries reduce churn in entity classification, but SE critiques highlight over-reliance on such theory as "shields" against testing. Balance: Introduce optionally in extensions (e.g., first-order paper with FOL axioms for boundaries), ensuring non-breaking growth via Git/SHACL. Test via code simulation: Model system graph with/without boundary nodes; check for breakage in traceability queries.

## Additional Tests for System Delineation

Beyond MSD and potential boundaries, use these tests to delineate systems, prioritizing practical SE validation (e.g., via checklists in workflows). Draw from BFO and experience to avoid overfocus on theory.

| Test | Description | Example (Hydraulics) | Example (Aircraft) | BFO Tie |
|------|-------------|----------------------|--------------------|---------|
| Emergent Properties | Whole exhibits properties not reducible to parts | Yes (pressure regulation from interactions) | No (flight from assembly, not emergence) | Continuants/Occurrents unity |
| Purpose/Teleology | Oriented toward a function or goal | Yes (fluid transfer for actuation) | No (artifact hosts multiple purposes) | Realizable dispositions |
| Homeostasis/Stability | Maintains internal state against perturbations | Yes (valves regulate flow) | Partial (but not defining) | Process dependencies |
| Scalability/Composition | Can aggregate into larger systems without loss of identity | Yes (subsystem in vehicle) | No (disassembly breaks identity) | Mereological sums |
| Testability Metric | Empirical validation (e.g., removal test: does removal break whole?) | Yes (remove pipe, system fails) | No (remove wing, still identifiable artifact) | Dependence relations