---
course: PHIL 10
type: lecture
lecture_num: "6"
date: 1/29
---

# PHIL 10 Lecture 6
- ## 1/29
	- ## Truth Tables 2

## Using Truth Tables

### Review

#### Quiz

- What connective is represented by the truth table below?

| *A* | *B* | *A* \[?\] *B* |
| --- | --- | ------------- |
| T   | T   | T             |
| T   | F   | F             |
| F   | T   | T             |
| F   | F   | T             |
|     |     |               |
- D. →
	- conditional
		- false if antecedent is true and consequent is false

#### Refresher
- **truth tables for arbitrary sentences of TFL**:

> [!Definition] ‘Valuation’ definition
> - A valuation is any assignment of truth values to particular atomic sentences of TFL.
- **Process:**
	1. To the left: all possible valuations of the atomics.
	2. Under each atomic on the right, copy its truth value at each row
	3. Under an innermost connective, fill in the truth value of the subsentence, according to the characteristic truth table for the connective
	4. Work from innermost to outermost connectives. Main connective last!

| *P* | *Q* | *P* → (*P* ∨ *Q*)           |
| --- | --- | --------------------------- |
| T   | T   | **T**  ***T***  T  **T**  T |
| T   | F   | **T**  ***T***  T  **T**  F |
| F   | T   | **F**  ***T***  F  **T**  T |
| F   | F   | **F**  ***T***  F  **F**  F |

### Truth Tables

- The column under the main logical connective provides the truth value for the sentence as a whole for a given valuation.
	- In other words: 
		- given the truth values of the atomics, it tells you the truth value of the whole.
	- This is the column you look to to determine whether some sentence is a:
		- **tautology**, a **contradiction**, or **neither**.
	- Also: whether two sentences are **necessarily equivalent**
	- Also: whether some sentences are **jointly satisfiable** 
		- (= jointly logically consistent, compatible)
	- Also: whether some set of premises **entail** a conclusion.

### Valuations
- **Valuations and how to order them**:

> [!NOTE]
> - How many rows?
> 	- If a sentence contains *n* different atomic sentences, its truth table should have 2<sup><i>n</i></sup> rows under the headers.
- You're **required** to put valuations in the following order:
	- **Leftmost atomic**: 
		- mark the first half of rows ‘T’ and the second half of the rows ‘F’
	- **Second leftmost atomic**: 
		- first quarter of rows ‘T’, second quarter ‘F’, and repeat.
	- **Third leftmost atomic**: 
		- first eighth of rows ‘T’, second eighth ‘F’, and repeat.
	- If you do this correctly, the rightmost atomic will alternate between ‘T’ and ‘F’ at **every** row.
##### Examples

###### Example 1

| P   | Q   | ((P ∧ Q) → P)            |
| --- | --- | ------------------------ |
| T   | T   | \_T  **T**  T   **T**  T |
| T   | F   | \_T  **F**  F   **T**  T |
| F   | T   | \_F  **F**  T   **T**  F |
| F   | F   | \_F  **F**  F   **T**  F |

###### Example 2

| A   | B   | (¬ (¬ A → B) ∨ A) |
| --- | --- | ----------------- |
| T   | T   |                   |
| T   | F   |                   |
| F   | T   |                   |
| F   | F   |                   |
- innermost connective:
	- B. ¬
		- only thing negation is working on is atomic sentence *A*

| (¬  | (¬  | A   | →   | B)  | ∨   | A)  |
| --- | --- | --- | --- | --- | --- | --- |
| F   | F   | T   | T   | T   | T   | T   |
| F   | F   | T   | T   | F   | T   | T   |
| F   | T   | F   | T   | T   | F   | F   |
| T   | T   | F   | F   | F   | T   | F   |
- start with ¬A
- then →B
- then ¬ of conditional
- then disjunct of negation or A

#### Brackets
- **Notes about brackets**:
	- Conjunction and disjunction are associative:
		- (A ∧ B) ∧ C is logically equivalent to A ∧ (B ∧ C).
		- (A ∨ B) ∨ C is logically equivalent to A ∨ (B ∨ C).
	- But nota bene:
		- These are logically equivalent sentences, but they’re **not** the very same sentence. 
			- (You can’t swap one for the other in, e.g., proofs.)
		- Do not omit any brackets (except, per our convention, the outermost) on strings of conjunctions or disjunctions.
	- Note:
		- (A → B)→ C is **not logically equivalent** to A → (B → C).

### Truth Table Uses

- **Uses of truth tables**:
- Truth tables can be used to prove whether...
	1. a sentence is a **tautology**, a **contradiction**, or neither
	2. a pair of sentences are **logically equivalent**
	3. some sentences are **jointly logically consistent**
	4. some premises **logically entail** a conclusion
		- i.e. an argument is **logically valid**
- In all cases, we are concerned with whether the relevant notion holds **in virtue of truth-functional form**.

#### Semantic Concepts
- **Semantic concepts for truth tables**:
	- Definition of ‘tautology’:
		- *A* is a **tautology** iﬀ it is true on every valuation.
			- A tautology is guaranteed true by virtue of its truth-functional form.
	- Definition of ‘contradiction’:
		- *A* is a **contradiction** iﬀ it is false on every valuation.
- Not all necessary truths are tautologies! 
	- Tautologies are guaranteed to be true just by their truth-functional form.
		- If an object is green, it has a color.
			- necessary truth but not a tautology
		- $1/2=.5$
			- necessary truth but not a tautology
		- Every dog is a dog.
		- If it’s raining, then it’s either raining or snowing.
	- All tautologies are necessary truths, but not all necessary truths are tautologies.
		- tautologies a smaller circle insider the bigger NT circle

#### Examples

##### Instructions

- Let’s use truth tables to determine whether the following sentences are tautologies, contradictions, or neither.
- First, consult your intuitions: 
	- does this sound like a tautology? 
	- Like a contradiction?
- Q:
	1. (A) tautology
	2. (B) contradiction
	3. (C) neither
###### Questions
1. A → A
	- (A) tautology
2. (A ↔ B)→ (A ↔ ¬B)
	- 
3. (A ∧ B)↔ ¬(¬A ∨ ¬B)
	- 
### Logical Equivalence

> [!Definition] ‘Logical equivalence’ definition:
> - A and B are **logically equivalent** iﬀ, for every valuation, their truth values agree, 
> 	- i.e. if there is no valuation in which they have opposite truth values.
- One way for two sentences to be necessarily equivalent is if they are logically equivalent.
	- ‘¬P ∧ ¬Q’ is **logically equivalent** to ‘¬(P ∨ Q)’
	- ‘John is a bachelor’ is necessarily equivalent to ‘John is an unmarried adult man’, but **not logically equivalent**.
#### Logical Consistency

> [!Definition] ‘Joint logical consistency’ definition:
> - A<sub>1</sub>, A<sub>2</sub>, . . . , A<sub>n</sub> are **jointly logically consistent** iﬀ there is some valuation which makes them all true.
- Is ‘¬P’ logically consistent with ‘¬(P → ¬Q)’? 
	- First guess: 
		- A. yes; 
		- B. no.
#### Logical Entailment
- **Logical validity and entailment**:
> [!Definition] ‘Logical entailment’ definition:
> - The sentences A<sub>1</sub>, A<sub>2</sub>, . . . , A<sub>n</sub> **logically entail** the sentence *C* if there is *no* valuation of the atomic sentences which makes all of A<sub>1</sub>, A<sub>2</sub>, . . . , A<sub>n</sub> true and *C* false.
- In other words, the argument from A<sub>1</sub>, A<sub>2</sub>, . . . , A<sub>n</sub> to *C* is **logically valid** iﬀ there’s no row of their joint truth table where all of A<sub>1</sub>, A<sub>2</sub>, . . . , A<sub>n</sub> are true and *C* is false.
	- In other words, iﬀ it’s logically impossible for the premises to be true while the conclusion is false.

### Validity symbolism

- A new symbol (which is not part of our object language in this class, TFL): 
	- ### **`‘⊨’`**
- $$A_1, A_2, ... , A_n ⊨ C$$
- Translation: A<sub>1</sub>, A<sub>2</sub>, ... , A<sub>n</sub> **entail** the sentence *C*.
	- In other words, the argument from A<sub>1</sub>, A<sub>2</sub>, ... , A<sub>n</sub> to *C* is valid.
- Example:
	- P, (P → (Q ∨ R)), ¬R ⊨ Q

#### Valid Truth Tables
##### Using truth tables to prove validity
- **Validity testing procedure**: 
	- find lines where the conclusion is **false**, and check whether **all** of the premises are true.
- If there is at least one line where all of the premises are true, and the conclusion is false, then the argument is not valid. 
	- Otherwise, the argument is valid.
- First pass: 
	- is this simple argument valid? 
		- A. yes; 
		- B. no.
			- A ∨ B, ¬A ⊨ B

| A   | B   | A ∨ B | ¬A  | B   |
| --- | --- | ----- | --- | --- |
| T   | T   |       |     |     |
| T   | F   |       |     |     |
| F   | T   |       |     |     |
| F   | F   |       |     |     |
- Answer:
	- -
##### Truth tables and validity
- Let’s test whether the following argument is valid:
	- P ∨ (P → (¬P ↔ P)) ⊨¬P
		- How many rows under the headers?
		- Which connective in the premise must we begin with?
- Practice tables:

| P   | P ∨ (P → (¬ P ↔ P)) | ¬P  |
| --- | ------------------- | --- |
|     |                     |     |
|     |                     |     |
|     |                     |     |
#### Arguments
##### Arguments with an empty premise set
- Could an argument of the following form be valid?
	- ⊨ C
- We know that a set of premises entails a conclusion iﬀ it’s impossible for the premises to be true while the conclusion is false.
- But the argument above doesn’t have any premises! 
	- So all of its premises are **trivially true** at every valuation.
- Suppose *C* is false at some valuation. 
	- Since all of the (non-existent) premises are (trivially) true, and the conclusion false, then the argument is not valid.
		- So if the above argument is valid, then C must be true at every valuation: 
			- that is, C must be a **tautology**.
##### Arguments with an empty conclusion set
- Could an argument of this form be valid?
	- A ⊨
- Note: 
	- because this argument has no conclusion, its conclusion is **trivially false**.
- So in order for there to be no lines at which the premise is true and the conclusion is (trivially) false, it must be that there are no lines at which the premise is true.
	- In other words, the premise must be a **contradiction**.
##### Examples
Let’s assess the validity of these arguments using truth tables:
- A ↔ B, ¬(A ∧ B), A ∨ B ∴ C
- A ∨ B, B ∨ C, C → A ∴ C ∨ ¬C

---

Previous: [PHIL 10 Lecture 5](PHIL_10_LE_5.md).
Next: [PHIL 10 Lecture 7](PHIL_10_LE_7.md).