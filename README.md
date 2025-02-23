

> Some notes inspired by the book ["Discrete Mathematics: An Open Introduction, Oscar Levin"](https://discrete.openmathbooks.org/dmoi3/ch_intro.html).

# Discrete Mathematics

Individually separate and distinct.

## Discrete vs. Continuous Values (with Function Examples)

### Discrete Function

A discrete function takes only distinct, separate values, usually integers or countable items.

**Example:**

Consider the function representing the number of students in each classroom:

| Classroom `x` | Students `f(x)` |
|---------------|-----------------|
| 1             | 25              |
| 2             | 30              |
| 3             | 18              |

You can't have fractional or intermediate values (like 25.5 students). The values are separate, distinct, and countable.


### Continuous Function

A continuous function can take any intermediate value within an interval.

**Example:**

Consider the function:

```
f(x) = 2.5x + 3
```

| Input `x` | Output `f(x)` |
|-----------|---------------|
| 1.0       | 5.5           |
| 1.5       | 6.75          |
| 2.0       | 8.0           |
| 2.7       | 9.75          |

The function varies gradually from point to point. You can always find intermediate values (such as 1.01, 1.02, etc.). There is no gap between values.

# Mathematical Statements

In order to do mathematics, we must clearly and precisely communicate mathematical ideas. Unlike many other subjects, mathematics requires exact definitions and statements.

## 1. Atomic and Molecular Statements

**Definitions:**

- **Statement:** A declarative sentence that is either true or false.
- **Atomic Statement:** A statement that cannot be broken down into simpler statements.
- **Molecular Statement:** A statement composed of simpler statements combined using logical connectives.

**Non-Statements:**

- Some expressions resemble statements but aren't, because they contain free variables. For example, the expression  
  `3 + x = 12`  
  is not inherently true or false—it depends on the value assigned to `x`.

---

## 2. Logical Connectives

We use logical connectives to form complex statements from simpler ones.

### Binary Connectives:

- **Conjunction (`P ∧ Q`):**  
  - Read as `"P and Q"`.  
  - True only if both `P` and `Q` are true.

- **Disjunction (`P ∨ Q`):**  
  - Read as `"P or Q"`.  
  - True if at least one of `P` or `Q` is true.

- **Implication (`P → Q`):**  
  - Read as `"if P then Q"`.  
  - True whenever `P` is false, or when both `P` and `Q` are true.

- **Biconditional (`P ↔ Q`):**  
  - Read as `"P if and only if Q"`.  
  - True if `P` and `Q` have the same truth value (both true or both false).

### Unary Connective:

- **Negation (`¬P`):**  
  - Read as `"not P"`.  
  - True when `P` is false.
 
**Example:**
 Let `P`: "It is raining." and `Q`: "I carry an umbrella."

- `P ∧ Q`: "It is raining, and I carry an umbrella."
- `P ∨ Q`: "It is raining, or I carry an umbrella, or both."
- `P → Q`: "If it rains, then I carry an umbrella."
- `¬P`: "It is not raining."

---

## 3. Implications

An implication (conditional) is expressed as `P → Q`, where:

- `P` is the **hypothesis (antecedent)**.
- `Q` is the **conclusion (consequent)**.

**Key Idea:**  
The implication `P → Q` is false **only** when `P` is true and `Q` is false. If `P` is false, the implication is always considered true (this concept is called **vacuous truth**).

**Direct Proofs:**  
To prove `P → Q`, assume `P` is true and show that this assumption leads logically to `Q`.

**Example:**
**If** a number is divisible by 10, **then** it is divisible by 5.

---

## 4. Converse and Contrapositive

- **Converse:** The converse of `P → Q` is `Q → P`.  
  **Important:** The converse is **not** logically equivalent to the original implication.

- **Contrapositive:** The contrapositive of `P → Q` is `¬Q → ¬P`.  
  **Important:** An implication is always logically equivalent to its contrapositive.

**Example:**
- Original: "If it's a cat, then it's an animal."
- Converse: "If it's an animal, then it's a cat." (**not always true**)
- Contrapositive: "If it's not an animal, then it's not a cat." (**always true**)

---

## 5. "If and Only If" Statements (Biconditionals)

A statement of the form `P ↔ Q` means both implications `P → Q` and `Q → P` hold simultaneously. Thus, it splits into two parts:

- If `P` is true, then `Q` is true.
- If `Q` is true, then `P` is true.

**Example:**
A rectangle is a square if and only if all its sides are equal.

means precisely:

- If rectangle is a square, then all its sides are equal.
- If all sides of a rectangle are equal, then it is a square.

---

## 6. Necessary and Sufficient Conditions

- **Necessary Condition:**  
  `"P is necessary for Q"` means `Q → P`.

- **Sufficient Condition:**  
  `"P is sufficient for Q"` means `P → Q`.

- **Necessary and Sufficient:**  
  If `P` is both necessary and sufficient for `Q`, then we have a biconditional `P ↔ Q`.

**Example:**  
Consider the statement:  
If you live in Paris, then you live in France.

- Living in France is **necessary** to live in Paris.
- Living in Paris is **sufficient** to live in France.

---

## 7. Quantifiers

Quantifiers enable the use of variables in mathematical statements. The two primary quantifiers are:

- **Universal Quantifier (`∀`):**  
  - Read as `"for all"` or `"for every"`.  
  - Example: `∀x (x ≥ 0)` means "for every `x`, it is true that `x` is greater than or equal to 0."

- **Existential Quantifier (`∃`):**  
  - Read as `"there exists"` or `"there is at least one"`.  
  - Example: `∃x (x < 0)` means "there exists some `x` such that `x` is less than 0."

**Domain of Discourse:**  
Quantifiers always require clarity about the set of possible values (domain). In discrete mathematics, the domain is commonly the set of natural numbers (`0, 1, 2, …`).

**Quantifiers and Negation:**  
Negations of quantified statements follow these equivalences:

- `¬∀x P(x)` is equivalent to `∃x ¬P(x)`.
- `¬∃x P(x)` is equivalent to `∀x ¬P(x)`.

---

## 8. Exercises

Solutions provided for the following exercices in the book:

- 0.2.1  
- 0.2.3  
- 0.2.4, 0.2.5, 0.2.6, 0.2.7  
- 0.2.9, 0.2.10  
- 0.2.12  
- 0.2.14, 0.2.15, 0.2.16, 0.2.17  
