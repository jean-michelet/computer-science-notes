# Summary

> Some notes inspired by the book ["Discrete Mathematics: An Open Introduction, Oscar Levin"](https://discrete.openmathbooks.org/dmoi3/ch_intro.html).

- [Introduction](#introduction)
- [Logic](#logic)
- [Sets](#sets)
- [Functions](#functions)

# Introduction

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

[⬆️ Return to top](#summary)

# Logic 

Logic is the study of the conclusions that can be drawn from given mathematical statements or facts.
A **statement** becomes a **fact** once it's proven to be true.

## Basic Example

If I say a number is greater than 5 and less than 10, we can conclude:

-  It is between 5 and 10.
- But we can't conclude it's exactly 7.

This shows that conclusions in math must be supported by valid reasoning.

#### **Structure of a Mathematical Argument**

A mathematical argument has:

- **Premises** – the starting assumptions or conditions.
- **Conclusion** – what follows logically from the premises.

**Example:**

- Premises: "All even numbers are divisible by 2" and "8 is even".
- Conclusion: "8 is divisible by 2".

The conclusion is a logical consequence of the premises.

#### Not all arguments are valid.

**Example:**

- Premise: "If it rains, the ground gets wet."
- Conclusion: "It rained because the ground is wet."

This is a **logical fallacy** (affirming the consequent). The wet ground might have another cause, like a sprinkler.

Logic helps us:

- Determine when a conclusion **does** follow from given premises.
- Recognize when it **doesn't**.

In mathematics, every result we claim must come from a valid argument even when the logic is simple or seems obvious.

## Mathematical Statements

In order to do mathematics, we must clearly and precisely communicate mathematical ideas. Unlike many other subjects, mathematics requires exact definitions and statements.

### 1. Atomic and Molecular Statements

**Definitions:**

- **Statement:** A declarative sentence that is either true or false.
- **Atomic Statement:** A statement that cannot be broken down into simpler statements.
- **Molecular Statement:** A statement composed of simpler statements combined using logical connectives.

**Non-Statements:**

- Some expressions resemble statements but aren't, because they contain free variables. For example, the expression  `3 + x = 12`
is not inherently true or false—it depends on the value assigned to `x`.

---

### 2. Logical Connectives

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

#### Unary Connective:

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

### 3. Implications

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

### 4. Converse and Contrapositive

- **Converse:** The converse of `P → Q` is `Q → P`.  
  **Important:** The converse is **not** logically equivalent to the original implication.

- **Contrapositive:** The contrapositive of `P → Q` is `¬Q → ¬P`.  
  **Important:** An implication is always logically equivalent to its contrapositive.

**Example:**
- Original: "If it's a cat, then it's an animal."
- Converse: "If it's an animal, then it's a cat." (**not always true**)
- Contrapositive: "If it's not an animal, then it's not a cat." (**always true**)

---

### 5. "If and Only If" Statements (Biconditionals)

A statement of the form `P ↔ Q` means both implications `P → Q` and `Q → P` hold simultaneously. Thus, it splits into two parts:

- If `P` is true, then `Q` is true.
- If `Q` is true, then `P` is true.

**Example:**
A rectangle is a square if and only if all its sides are equal.

means precisely:

- If rectangle is a square, then all its sides are equal.
- If all sides of a rectangle are equal, then it is a square.

---

### 6. Necessary and Sufficient Conditions

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

### 7. Quantifiers

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

### 8. Exercises

Solutions provided for the following exercices in the book:

- 0.2.1  
- 0.2.3  
- 0.2.4, 0.2.5, 0.2.6, 0.2.7  
- 0.2.9, 0.2.10  
- 0.2.12  
- 0.2.14, 0.2.15, 0.2.16, 0.2.17  

[⬆️ Return to top](#summary)

## Rules of Logic

Logic explains how statements combine, letting us analyze mathematical arguments with precision.

### Truth Tables

A **truth table** lists every possible assignment of truth values to atomic statements and shows the result of a molecular statement.

**Example:**

Let

- `P`: *You do your homework.*
- `Q`: *You get a good grade.*

Consider the molecular statement:  
`¬P ∨ Q`  
(read as "Either you don’t do your homework, or you get a good grade.")

| P    | Q    | ¬P   | **¬P ∨ Q** |
| ---- | ---- | ---- | ---------- |
| T    | T    | F    | **T**      |
| T    | F    | F    | **F**      |
| F    | T    | T    | **T**      |
| F    | F    | T    | **T**      |

---

### Logical Equivalence

Two molecular statements `A` and `B` are **logically equivalent** (written `A ≡ B`) if they have the same truth value for all possible combinations of truth values of their components.

**Implication form:**
If it is raining, then I will take an umbrella.
(This is of the form `P → Q`).
**Logically equivalent disjunction form:**
Either it is not raining, or I will take an umbrella.
(This is of the form `¬P ∨ Q`).

**Key Result:**

`P → Q ≡ ¬P ∨ Q`

| P    | Q    | **P → Q** | **¬P ∨ Q** |
| ---- | ---- | --------- | ---------- |
| T    | T    | **T**     | **T**      |
| T    | F    | **F**     | **F**      |
| F    | T    | **T**     | **T**      |
| F    | F    | **T**     | **T**      |

This means **implications are disjunctions**.

---

#### Implication and Contrapositive

**Theorem:**  
`P → Q ≡ ¬Q → ¬P`

*If it is a cat, then it is an animal.* 
**Contrapositive:** *If it is not an animal, then it is not a cat.*

| P (Cat) | Q (Animal) | **P → Q** | ¬Q   | ¬P   | **¬Q → ¬P** |
| ------- | ---------- | --------- | ---- | ---- | ----------- |
| T       | T          | **T**     | F    | F    | **T**       |
| T       | F          | **F**     | T    | F    | **F**       |
| F       | T          | **T**     | F    | T    | **T**       |
| F       | F          | **T**     | T    | T    | **T**       |

An implication is logically equivalent to its contrapositive.

---

#### De Morgan’s Laws

These laws describe how negation interacts with conjunction (`and`) and disjunction (`or`):

- `¬(P ∧ Q) ≡ ¬P ∨ ¬Q`
- `¬(P ∨ Q) ≡ ¬P ∧ ¬Q`

**Example:**

Let

- `P`: You study
- `Q`: You sleep early

- `¬(P ∧ Q)`: "It is not true that you study and sleep early."  
  Equivalent to `¬P ∨ ¬Q`: "You don’t study or you don’t sleep early."

- `¬(P ∨ Q)`: "It is not true that you study or sleep early."  
  Equivalent to `¬P ∧ ¬Q`: "You don’t study and you don’t sleep early."

**Truth Table for `¬(P ∧ Q) ≡ ¬P ∨ ¬Q`:**

| P    | Q    | P ∧ Q | ¬(P ∧ Q) | ¬P   | ¬Q   | **¬P ∨ ¬Q** |
| ---- | ---- | ----- | -------- | ---- | ---- | ----------- |
| T    | T    | T     | F        | F    | F    | F           |
| T    | F    | F     | T        | F    | T    | T           |
| F    | T    | F     | T        | T    | F    | T           |
| F    | F    | F     | T        | T    | T    | T           |

**Truth Table for `¬(P ∨ Q) ≡ ¬P ∧ ¬Q`:**

| P    | Q    | P ∨ Q | ¬(P ∨ Q) | ¬P   | ¬Q   | **¬P ∧ ¬Q** |
| ---- | ---- | ----- | -------- | ---- | ---- | ----------- |
| T    | T    | T     | F        | F    | F    | F           |
| T    | F    | T     | F        | F    | T    | F           |
| F    | T    | T     | F        | T    | F    | F           |
| F    | F    | F     | T        | T    | T    | T           |

---

#### Negation of an Implication

**Theorem:**  
`¬(P → Q) ≡ P ∧ ¬Q`

Let `P`: You study  
Let `Q`: You pass the exam

Then  
`¬(P → Q)` means: "It’s not true that if you study, then you pass."  
This is equivalent to: "You study and you don’t pass."

| P (Study) | Q (Pass) | P → Q | **¬(P → Q)** | **P ∧ ¬Q** |
| --------- | -------- | ----- | ------------ | ---------- |
| T         | T        | T     | **F**        | **F**      |
| T         | F        | F     | **T**        | **T**      |
| F         | T        | T     | **F**        | **F**      |
| F         | F        | T     | **F**        | **F**      |

#### Boolean Algebra Perspective

Since logical statements can be rewritten using these identities (e.g. implication as disjunction, De Morgan’s laws, etc.), they follow a system known as **Boolean algebra**.

###   Equivalence for Quantified Statements

studying...

###   Deduction

In logic, deduction rules are valid forms of argument that guarantee the truth of the conclusion, provided the premises are true.

#### Structure of a Deduction Formula

A deduction rule is written in a vertical structure, like a small argument. 
It contains:
- One or more premises (assumed to be true),
- A horizontal line (couldn't display on GitHub Markdown),
- And a conclusion, marked by the symbol `∴` (read as "therefore").

#### Study case 1: **Modus Ponens**

Let:

* `P`: Your phone is connected to Wi-Fi
* `Q`: Your phone receives notifications

We are using the deduction rule:

```math
\begin{array}{c}
P \rightarrow Q \\
P \\
\therefore\ Q
\end{array}
```

**Explanation**:

- If your phone is connected to Wi-Fi, then it receives notifications. (`P → Q`)
- Your phone **is** connected to Wi-Fi. (`P`)
- **Therefore**, your phone receives notifications. (`Q`)

Reminder: In logic, the implication `P → Q` can still be **true even when `P` is false**. 
For example, if the phone is *not* connected to Wi-Fi (`P` is false), the implication doesn't tell us whether it receives notifications (`Q`) or not — it still counts as logically "true" either way (Vacuous truth).

But here, we **know** that:

* The implication `P → Q` is true, and
* `P` is true (your phone is connected),

So in order for the implication to hold, `Q` **must** be true as well.

#### Study case 2

```math
\begin{aligned}
P \rightarrow Q \\
\neg P \rightarrow Q \\
\therefore\ Q
\end{aligned}
```

**Example**
Let:

* `P`: You flipped the switch
* `Q`: The lights are on

- If you flipped the switch, the lights are on.
- If you didn’t flip the switch, the lights are still on (maybe motion sensor).
- **Therefore**, the lights are on.

#### Study case 3:

```math
\begin{aligned}
P \rightarrow R \\
Q \rightarrow R \\
P \vee Q \\
\therefore\ R
\end{aligned}
```

**Example**
Let:

* `P`: The bakery is open
* `Q`: The café is open
* `R`: You can buy fresh bread

- If the bakery is open, you can buy fresh bread.
- If the café is open, you can buy fresh bread.
- Either the bakery or the café is open.
- **Therefore**, you can buy fresh bread.

[⬆️ Return to top](#summary)

# Sets

A **set** is an unordered collection of distinct mathematical objects. Each object in a set is called an **element** or **member**. 

- **Uniqueness**: Repeated elements do not affect the set.
- **Order irrelevance**: The order of elements in a set does not matter.

## Set Notation

We represent sets using curly braces `{}` to enclose their elements.

- Example: `A = {1, 2, 3}`

The symbol `∈` denotes membership and is read as "is an element of" or "belongs to".

- Example:
  - `a ∈ {a, b, c}` means `a` is an element of the set `{a, b, c}`.
  - `d ∉ {a, b, c}` means `d` is not an element of `{a, b, c}`.

An **empty set** is a set with no elements and is denoted by:

- `∅ = {}`

### Describing Sets

When sets contain many elements (possibly infinitely many), listing elements explicitly becomes impractical. 
For example, the set of all even natural numbers can be represented as:

- `E = {0, 2, 4, 6, ...}`

A more precise way is using **set-builder notation**, which specifies the conditions elements must satisfy:

- Example: `E = {x ∈ ℕ : ∃n ∈ ℕ (x = 2n)}`

Here, the colon `:` (or sometimes a vertical bar `|`) means "such that".

In simpler terms, we can write:

- `E = {x ∈ ℕ : x is even}`

## Relationships Between Sets

### Equality

Two sets are **equal** if and only if they contain exactly the same elements.

- Example:
  - `{1, 2, 3} = {3, 1, 2}` (order doesn't matter)
  - `{1, 2, 3} = {1, 1 + 1, 1 + 1 + 1}` (representation doesn't matter)

If `A = {1, 2, 3}` and `B = {1, 2, 3, 4}`, then:

- `A ≠ B` because `B` contains the element `4` which is not in `A`.

### Subsets

A set `A` is a **subset** of another set `B` if every element of `A` is also an element of `B`. 
We write:
`A ⊆ B`

Symbol **⊆** means that equality is allowed.

Symbol **⊂** means every element in `A` is also in `B`, but `A ≠ B`. 
Equality is not allowed, this a **proper subset**.

Symbol **⊈** means **not a subset**.

Examples:

- `{1, 3, 2} ⊆ {1, 2, 3}` (**subset**)
- `{1, 2} ⊂ {1, 2, 3, 4}` (**proper subset**)
- `{3, 7} ⊈ {1, 2, 3, 4}` (**not a subset** since `7` is missing)

### Power Sets

The **power set** of a set `A`, denoted `P(A)`, is the set of all subsets of `A`.

- Example: If `A = {1, 2, 3}`, then:

```
P(A) = {∅, {1}, {2}, {3}, {1, 2}, {1, 3}, {2, 3}, {1, 2, 3}}
```

### Cardinality

The **cardinality** of a set `A`, denoted `|A|`, is the number of elements in the set.

Examples:

- If `A = {1, 2, 3}`, then `|A| = 3`
- If `B = {1, 2, 3, 4}`, then `|B| = 4`

Thus, `|A| ≠ |B|`.

## Operations on Sets

### Union

The **union** of sets `A` and `B`, denoted `A ∪ B`, is the set of all elements that are in either `A`, `B`, or both.

Example:

- If `A = {1, 2, 3}` and `B = {2, 3, 4}`, then `A ∪ B = {1, 2, 3, 4}`

### Intersection

The **intersection** of sets `A` and `B`, denoted `A ∩ B`, is the set of all elements common to both `A` and `B`.

Example:

- If `A = {1, 2, 3}` and `B = {2, 3, 4}`, then `A ∩ B = {2, 3}`

### Set Difference

The **difference** of sets `A` and `B` (`A \ B`) is the set of elements that are in `A` but not in `B`.

Example:

If `A = {1, 2, 3}` and `B = {2, 4}`, then `A \ B = {1, 3}`

### Complement

Given a universal set `U`, the **complement** of set `A`, denoted `A̅`, contains all elements of `U` not in `A`.

Example:

- If `U = {1, 2, ..., 10}` and `A = {2, 3, 5, 7}`, then `A̅ = {1, 4, 6, 8, 9, 10}`

### Cartesian Product

The **Cartesian product** of sets `A` and `B`, denoted `A × B`, is the set of all ordered pairs `(a, b)` where `a ∈ A` and `b ∈ B`.

Example:

- If `A = {1, 2}` and `B = {3, 4}`, then:

```
A × B = {(1, 3), (1, 4), (2, 3), (2, 4)}
```

## Logical Equivalences

Set operations can be related to logical connectives:

- `x ∈ A ∪ B ⇔ (x ∈ A) ∨ (x ∈ B)`
- `x ∈ A ∩ B ⇔ (x ∈ A) ∧ (x ∈ B)`
- `x ∈ A̅ ⇔ ¬(x ∈ A)`

## Exercises

Solutions provided for the following exercises in the book:

- 0.3.1, 0.3.2, 0.3.3, 0.3.4, 0.3.5, 0.3.6, 0.3.7, 0.3.8, 0.3.9
- 0.3.11, 0.3.12, 0.3.13
- 0.3.15
- 0.3.17
- 0.3.20
- 0.3.28

[⬆️ Return to top](#summary)

# Functions

A **function** is a rule that assigns each input **exactly one** output.  
The set of all inputs is the **domain**, and the set of allowed outputs is the **codomain**.

```math
f : X \to Y
```

Here,  

- **f** is the name of the function,  
- **X** is the **domain**,  
- **Y** is the **codomain**,  
- A specific **rule** tells us how each input in X maps to an output in **Y**.



## Basic Examples

**Example**  
```math
f : \mathbb{N} \to \mathbb{N} \quad\text{defined by}\quad f(x) = x + 1
```
  - **Domain** and **Codomain**: the set of natural numbers $(\mathbb{N})$.  
  - **Rule**: “Add 1 to the input.”

Not every element of the codomain must be used. For instance:

```math
f : \{1, 2, 3\} \to \{0, 1, 2, 3\}, \quad f(x) = x - 1
```

- $(f(1) = 0,\ f(2) = 1,\ f(3) = 2)$
- The **range** (actual outputs) here is {0,1,2}, which is a subset of the codomain {0,1,2,3\}



## Validity Conditions

1. **Every input has some output** (no input is left undefined).  
2. **Each input has exactly one output** (no input is mapped to multiple outputs).

### Invalid Examples

- **Missing Output**  
```math
f : \{1\} \to \{1,2,3\}, \quad f(x) = x - 1
```
  Since $(f(1)=0) and (0 \notin \{1,2,3\})$, this “function” is invalid. The output must lie in the codomain.

- **Multiple Outputs**  
  Suppose Jack has two dogs, a labrador and a doberman:
```math
f : \{\text{Jack}, \text{Paul}\} \to \{\text{Labrador}, \text{Rottweiler}, \text{Doberman}\}
```
  If we try:

  - f(Jack) = Labrador
  - f(Jack) = Doberman
  - f(Paul) = Rottweiler

  Jack is assigned **two** different outputs (Labrador and Doberman). This violates the rule that each input can map to **only one** output.



## Describing a Function

According to the **Rule of Four**, a function can be described:

1. **Algebraically** (a formula)  
2. **Numerically** (a table)  
3. **Graphically** (a coordinate plot, for example)  
4. **In words** (a verbal description)

When the domain is **finite**, an algebraic formula might be too complicated or impossible to find. Therefore, we often use **two-line notation** or **mapping diagrams**.

Two-line notations is better to prevent mistakes like missing outputs or duplicating outputs.

### Two-Line Notation

**Correct Definition Example**:
```math
f : \{1, 2, 3\} \to \{a, b, c, d\}
```

```math
f = 
\begin{pmatrix}
1 & 2 & 3 \\
d & a & c
\end{pmatrix}
```

This means:  

- f(1) = d
- f(2) = a
- f(3) = c  
  No input is left without an output, and no input has more than one output.

**Invalid Definition Example**:
```math
g : \{1, 2, 3\} \to \{a, b, c, d\}
```

```math
g =
\begin{pmatrix}
1 & 2 & 3 \\
\; & a, c? & d
\end{pmatrix}
```

- “1” has **no** assigned output.  

- “2” has **two** outputs ((a\) and (c\)).  
  Hence, (g\) is not a valid function.

  > Note that errors are really easy to spot using a matrice

#### Tables

We can also define functions in a table, but we must ensure every input has exactly one output:

| Input (x) | Output g(x)   |
| --------- | ------------- |
| 1         | *(undefined)* |
| 2         | a, c?         |
| 3         | d             |

This is an invalid function for the same reasons stated above.

---

### Recursively Defined Functions

For $f : \mathbb{N} \to \mathbb{N}$, a **recursive definition** has:

- An **initial condition**, specifying (f\) at some starting point.
- A **recurrence relation**, indicating how to get f(n+1) from f(n)\.

A **recurrence relation** is a mathematical expression that defines a sequence by relating each term to one or more previous terms.

#### Example of a Recursive Definition

- **Initial condition**: $f(0) = 1$  
- **Recurrence relation**: $f(n + 1) = f(n) + 1$

**Find** $f(3)$:

| Step | Calculation       | Result |
| ---: | :---------------- | -----: |
|    1 | $f(0)$            |      1 |
|    2 | $f(1) = f(0) + 1$ |      2 |
|    3 | $f(2) = f(1) + 1$ |      3 |
|    4 | $f(3) = f(2) + 1$ |      4 |

**Answer**: $f(3) = 4$.



## Surjections, Injections, and Bijections

**Injective (One-to-One)**  

- **Definition**: A function is injective if **different** inputs never map to the **same** output. Equivalently, every element of the codomain is mapped by **at most one** domain element.  
- **Example**: $\{1,2,3\}\to\{2,4,6\}$ with $1\mapsto2,\ 2\mapsto4,\ 3\mapsto6$ is injective.

**Surjective (Onto)**  

- **Definition**: A function is surjective if **every** element of the codomain is the image of **at least one** domain element.  
- **Example**: $\{1,2,3,4\}\to\{0,1\}$ where $1\mapsto1,\ 2\mapsto0,\ 3\mapsto1,\ 4\mapsto0$. Both $0$ and $1$ appear as outputs.

**Bijective**  

- **Definition**: A bijective function is both **injective** and **surjective**. Each codomain element is the image of **exactly one** domain element.  
- **Example**: $\{1,2,3\}\to\{2,3,4\}$ with $1\mapsto2,\ 2\mapsto3,\ 3\mapsto4$ is bijective.



## Image and Inverse Image

**Image of an Element**  
For $x$ in the domain, the **image** is $f(x)$ in the codomain.

For a subset $B$ of the codomain, $f^{-1}(B) = \lbrace x \mid f(x) \in B \rbrace$.

**Inverse Image of an Element**  
For $y$ in the codomain, the **inverse image** $f^{-1}(y)$ is the set of all $x$ in the domain for which $f(x) = y$.

**Image of a Subset**  
For a subset $A$ of the domain, $f(A) = \lbrace f(x) \mid x \in A \rbrace$.

**Inverse Image of a Subset**  
For a subset $B$ of the codomain, $f^{-1}(B) = \lbrace x \mid f(x) \in B \rbrace$.


## Exercises (0.4.x)

Solutions provided for the following exercises in the book:

- 0.4.1, 0.4.2
- 0.4.5
- 0.4.7
- 0.4.9, 0.4.10
- 0.4.12, 0.4.13
- 0.4.17
- 0.4.21, 0.4.22
- 0.4.24, 0.4.25, 0.4.26, 0.4.27


[⬆️ Return to top](#summary)



