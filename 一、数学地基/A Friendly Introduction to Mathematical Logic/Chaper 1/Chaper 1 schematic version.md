# Chapter 1 Structures and Languages
1. Historical Background
    - Time: Mid-19th century
    - Drivers: Geometry & calculus developments, set theory paradoxes
    - Core Goal: Construct a consistent axiomatic system, especially for arithmetic

2. Hilbert’s Program
    - Trigger: Mathematical foundational crisis, challenge from Intuitionism
    - Core Method: Finitistic proof methods
    - Core Goal: Prove consistency of classical mathematics, secure its established achievements
    - Extended Aim: Achieve completeness, i.e., every semantically true statement is formally provable

3. Gödel’s Incompleteness Theorems (1931)
    1. First Incompleteness Theorem
        - Applicable System Conditions (all must be met):
            1. Consistent
            2. Recursively axiomatizable
            3. Sufficiently strong (can express basic Peano Arithmetic, PA, and can represent its own syntax (in particular, proofs) within arithmetic)
        - Conclusion: There exist sentences of arithmetic that are true in the standard model ℕ (assuming soundness), but unprovable within the system S.
        - Core Clarification: 
            1. Provability (⊢) is an internal, rule-governed process, without regard to meaning.
            2. Semantic truth (⊨) is defined externally via a model, and truth is determined by the satisfaction relation, not by derivation.
            3. The two are connected by soundness: every provable statement is semantically true.
    2. Second Incompleteness Theorem
        - Conclusion: If such a system S is consistent and sufficiently strong, it cannot prove Con(S) (the formal statement of its own consistency) within itself.
        - Core Meaning: No sufficiently strong formal system can internally certify its own consistency using its own proof rules.
    3. Impact
        - Hilbert’s Program is unachievable in its original form
        - Core Logical Takeaway: No sufficiently strong formal system can be complete, nor can it prove its own consistency
        - Core Philosophical Takeaway: The gap between truth (semantics) and provability (syntax) is irreducible.
        

4. Three Major Schools of Mathematical Philosophy
    - Platonism: Truth independent of provability (truth > provability)
    - Intuitionism (Brouwer): Truth ≡ Constructibility ⇒ Provable ⇒ True (truth is identified with constructive provability)
    - Formalism (Hilbert): Goals are Truth ⇒ Provable (completeness, ideal) + Consistency (core)

## Supplementary Note (Key Pitfall Avoidance)
1. Scope Limitations (Gödel’s Theorems do NOT apply to all systems)
    - Propositional logic: Complete
    - First-order predicate logic: Complete (Gödel’s Completeness Theorem, 1929)
    - Presburger arithmetic (addition-only): Complete & decidable

2. Gentzen’s 1936 Contribution
    - Proved consistency of PA using transfinite induction up to ε₀
    - Founded modern proof theory
    - Significance: Partial realization of Hilbert’s vision under well-defined, stricter assumptions