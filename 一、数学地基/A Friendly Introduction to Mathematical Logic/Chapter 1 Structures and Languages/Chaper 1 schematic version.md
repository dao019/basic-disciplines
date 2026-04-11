# §1.0 Leading in

> Core Theme: From the attempt to unify truth and provability to the discovery of their fundamental separation

========
## 1. Historical Background
1. Time: Mid-19th century
2. Drivers: Geometry & calculus developments, set theory paradoxes
3. Core Goal: Construct a consistent axiomatic system, especially for arithmetic

## 2. Hilbert’s Program
1. Trigger: Mathematical foundational crisis, challenge from Intuitionism
2. Core Method: Finitistic proof methods
3. Core Goal: Prove consistency of classical mathematics, secure its established achievements
4. Extended Aim: Achieve completeness, i.e., every semantically true statement is formally provable

## 3. Gödel’s Incompleteness Theorems (1931)
1. First Incompleteness Theorem
    1. Applicable System Conditions (all must be met):
        1. Consistent
        2. Recursively axiomatizable
        3. Sufficiently strong (can express basic Peano Arithmetic, PA, and can represent its own syntax (in particular, proofs) within arithmetic)
    2. Conclusion: There exist sentences of arithmetic that are true in the standard model ℕ (assuming soundness), but unprovable within the system S.
    3. Core Clarification: 
        1. Provability (⊢) is an internal, rule-governed process, without regard to meaning.
        2. Semantic truth (⊨) is defined externally via a model, and truth is determined by the satisfaction relation, not by derivation.
        3. The two are connected by soundness: every provable statement is semantically true.
2. Second Incompleteness Theorem
    1. Conclusion: If such a system S is consistent and sufficiently strong, it cannot prove Con(S) (the formal statement of its own consistency) within itself.
    2. Core Meaning: No sufficiently strong formal system can internally certify its own consistency using its own proof rules.
3. Impact
    1. Hilbert’s Program is unachievable in its original form
    2. Core Logical Takeaway: No sufficiently strong formal system can be complete, nor can it prove its own consistency
    3. Core Philosophical Takeaway: The gap between truth (semantics) and provability (syntax) is irreducible.
        
## 4. Three Major Schools of Mathematical Philosophy
1. Platonism: Truth independent of provability (truth > provability)
2. Intuitionism (Brouwer): Truth ≡ Constructibility ⇒ Provable ⇒ True (truth is identified with constructive provability. Intuitionism rejects non-constructive proofs & unrestricted use of LEM.)
3. Formalism (Hilbert): Goals are Truth ⇒ Provable (completeness, ideal) + Consistency (core)

## Supplementary Note (Key Pitfall Avoidance)
1. Scope Limitations (Gödel’s Theorems do NOT apply to all systems)
    1. Propositional logic: Complete
    2. First-order predicate logic: Complete (Gödel’s Completeness Theorem, 1929)
    3. Presburger arithmetic (addition-only): Complete & decidable
2. Gentzen’s 1936 Contribution
    1. Proved consistency of PA using transfinite induction up to ε₀
    2. Founded modern proof theory
    3. Significance: Partial realization of Hilbert’s vision under well-defined, stricter assumptions


# §1.1 Naïvely

> Core Theme: From form (syntax) to meaning (semantics), and how truth is determined via structures.

========
## 1. Skeleton
1. Syntax ($\vdash$)
    1. Formal language
    2. Formulas
    3. Sentences
    4. Proof system
    5. Provability
    6. Axiom
2. Theory (set of sentences)
3. $\operatorname{Axioms} \subseteq \mathcal{T} \subseteq \operatorname{Sentences} \subset \operatorname{Formulas}$
4. Semantics ($\models$)
    1. Structure
    2. Assignment
    3. Satisfaction ($\models$)
5. Conclusion
    1. Syntax determines what can be proved (e.g., $T \vdash \varphi$).
    2. A theory is a set of sentences (axioms) in a formal language, i.e., a theory $T$.
    3. Semantics determines in which structures those sentences are true.
6. Three Uses of $\models$ (Same Symbol, Different Levels)
    1. Structure Satisfaction: $\mathcal{M} \models \varphi$
    2. Model of a Theory: $\mathcal{M} \models T$
    3. Semantic Consequence (Logical Consequence): $T \models \varphi$ and $\models \varphi$

## 2. Syntax vs. Semantics (Foundational Distinction)
1. Syntax (Pure Form)
    1. Definition: Determines well-formed expressions and derivability.
    2. Core Trait: Meaning-free
    3. Essence: A rule-governed system of symbol manipulation
2. Semantics (Meaning & Reference)
    1. Definition: Assigns meaning via interpretations in structures, thereby determining truth.
    2. Core Trait: Relates formulas to structures via interpretation, thereby enabling truth evaluation.
    3. Essence: Meaning assignment + truth determination mechanism.
3. Core Principle (Naïve Version)
    1. Symbols have no inherent meaning.
    2. Meaning arises through interpretation in a structure.
    3. Truth is evaluated relative to a structure.

## 3. Theory (Between Syntax and Semantics)
1. Definition
    1. A set of sentences: $T = \{\varphi_1, \varphi_2, \varphi_3, \dots\}$
    2. Provides axioms for syntactic derivation ($\vdash$).
    3. Not necessarily closed under logical consequence.
    4. Closure hierarchy
        1. Deductive closure (purely syntactic closure): $\mathcal{T}^\vdash = \{\varphi \mid \mathcal{T} \vdash \varphi\}$
        2. Semantic closure: $\operatorname{Th}(\mathcal{T}) = \{\varphi \mid \mathcal{T} \models \varphi\}$
    5. Properties
        1. $\mathcal{T}$ is deductively closed iff $\mathcal{T} = \mathcal{T}^\vdash$
        2. $\mathcal{T}$ is semantically closed iff $\mathcal{T} = \operatorname{Th}(\mathcal{T})$
2. Nature of Axioms
    1. Syntactic Role: Sentences of a formal language describing abstract properties.
    2. Semantic Status: Truth is model-dependent (no absolute truth value).
    3. Epistemic Nature: Assumptions, not absolute truths.
3. Critical Insight
    1. A theory determines a model class (semantic structure + theory satisfaction): $\mathrm{Mod}(T) = \{ \mathcal{M} \mid \mathcal{M} \models T \}$
    2. A theory characterizes a class of structures (its models,a $T$-world), not a single structure.
4. Bridge Clarification: The satisfaction relation $\models$ is the only formal connection between syntax and semantics.

## 4. Mathematical Structures (and Models)
1. Standard Model-Theoretic Definition: $\mathcal{M} = (D, I)$
    1. Domain $D \neq \emptyset$ (universe of discourse), a nonempty set.
    2. Interpretation function $I$ (non-logical symbols)
    2. Role:
        1. Provides a domain for interpretation of a formal language
        2. Acts as a universe of discourse
    3. A structure $\mathcal{M}$ becomes a model of a theory $T$ iff: $\mathcal{M} \models T \quad\Longleftrightarrow\quad \forall\,\varphi\in T,\ \mathcal{M}\models\varphi$
2. Core Feature
    1. A theory defines a class of models among all possible structures.
    2. Model = Structure + Theory satisfaction

## 5. Interpretation
1. Definition
    1. An interpretation is a function that assigns meanings to non-logical symbols
        1. Constant symbol: $c \mapsto I(c) \in D$
        2. Function symbol: $f \mapsto I(f) : D^n \to D$
        3. Relation symbol: $R \mapsto I(R) \subseteq D^n$
    2. It is an integral part of a structure.
    3. It determines the truth values of formulas (or sentences) in the structure.
2. Core Observation
    1. The same symbol can have distinct interpretations in different structures.
    2. Therefore: Syntax is fixed; semantics varies via interpretation.

## 6. Truth and Models
1. Three Notions: Validity, Satisfaction, and Provability (Critical Distinction)
    1. $\vDash \varphi$: true in all structures
    2. $\mathcal{M} \vDash \varphi$: true in structure $\mathcal{M}$
    3. $T \vdash \varphi$: provable from theory $T$
2. Model Definition: $\mathcal{M}$ is a model of theory $\Sigma$
    1. Naïve: all sentences in $\Sigma$ are true in $\mathcal{M}$
    2. Formal: $\mathcal{M} \models \Sigma \ \iff\ \forall\varphi\in\Sigma,\ \mathcal{M}\models\varphi$
3. Formal Set-Theoretic Definition
    1. $\models$ is a ternary relation (three-place relation): $\models \ \subseteq \ \operatorname{Str} \times \operatorname{Assign} \times \operatorname{Form}$
    2. General Case: $\mathcal{M}, s \models \varphi$ (formula with free variables, depends on a structure and an assignment)
    3. Special Case: $\mathcal{M} \models \varphi$ (sentence, no assignment)
4. Notation
    1. $\mathcal{M} \models \Sigma$ (read: "$\mathcal{M}$ satisfies $\Sigma$" or "$\mathcal{M}$ is a model of $\Sigma$")
    2. Here $\models$ denotes the satisfaction relation between a structure and a sentence (or a set of sentences).
    3. Key Deep Insight: The definition of satisfaction is given relative to a structure and a variable assignment. It is defined recursively on the structure of formulas (by breaking formulas into simpler subformulas until atomic cases are reached).
    4. Critical Distinction: Satisfaction of formulas depends on variable assignments; satisfaction of sentences (closed formulas) does not.
5. Core Philosophical Distinction
    1. Platonism
        1. Fix a structure $\mathbb{M}_0$.
        2. $\varphi$ is true iff $\mathbb{M}_0 \models \varphi$.
    2. Formalism / Model-Theoretic View: No privileged structure exists.
        1. Two semantic notions are recognized:
            1. $\mathcal{M} \models \varphi$: model-relative truth
            2. $\models \varphi$: validity (true in all structures)
        2. It rejects truth defined via a distinguished structure.
6. Truth Clarification (Semantic Summary)
    1. Model-relative truth
        1. The truth of a sentence is always defined relative to a structure: $\mathcal{M} \models \varphi$
        2. The truth of a formula is always defined relative both to a structure and an assignment: $\mathcal{M}, s \models \varphi$
    2. Logical validity (structure-invariant truth)
        1. A sentence is logically valid iff it is true in every structure: $\models \varphi$
        2. This notion does not depend on any distinguished or intended model.

## 7. Interpretation and Truth
1. Changing interpretation of symbols changes truth values.
2. Example in $\mathbb{R}^3$:
    1. If $+$ is interpreted as vector addition: $u + v = v + u$
    2. If $+$ is interpreted as cross product: $u + v \neq v + u$
3. Key Point: Truth depends on a structure together with an interpretation of the language.