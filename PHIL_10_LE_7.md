---
course: PHIL 10
type: lecture
lecture_num: "7"
date: 1/31
---

# PHIL 10 Lecture 7
- ## 1/31
	- ## Truth Tables
		- ## Demonstrations
- Midterm:
	- Know the convention for the order of valuations
	- TA Name:
		- **Javier** Medina Barrientos

## Demonstrations with Truth Tables
### Uses of Truth Tables
- Truth tables can be used to prove whether...
	1. a sentence is a **tautology**, a **contradiction**, or neither
	2. a pair of sentences are **logically equivalent**
	3. some sentences are **jointly logically consistent**
	4. some premises **logically entail** a conclusion—i.e. an argument is **logically valid**
- In all cases, we are concerned with whether the relevant notion holds: 
	- **in virtue of truth-functional form**.
### Refresher

> [!Definition] Definition of ‘tautology’:
> - *A* is a **tautology** iﬀ it is true on every valuation.
- A tautology is guaranteed true by virtue of its truth-functional form.
> [!Definition] Definition of ‘contradiction’:
> - *A* is a **contradiction** iﬀ it is false on every valuation.
- Examples:
	- Let’s use truth tables to assess whether the following sentences are tautologies, contradictions, or neither.
		- A → A
		- ((A ∨ B) ∧ (¬A ∨ ¬B)) ∧ ((A → B) ∧ (B → A))
### Logical Equivalence

> [!Definition] ‘Logical equivalence’ definition:
> - A and B are **logically equivalent** iﬀ, for every valuation, their truth values agree, 
> 	- i.e. if there is no valuation in which they have opposite truth values.
- One way for two sentences to be necessarily equivalent is if they are logically equivalent.
	- ‘¬P ∧ ¬Q’ is **logically equivalent** to ‘¬(P ∨ Q)’
	- ‘John is a bachelor’ is necessarily equivalent to ‘John is an unmarried adult man’, but **not logically equivalent**.
#### Example
- Truth tables can be used to prove that two sentences are logically equivalent. 
	- We make use of **joint truth tables**.
- If two sentences have **the same column of truth values** under their main logical operators, then they are logically equivalent.

| P     Q | ¬ (P ∧ Q)       | ¬ P ∨ ¬ Q   |
| ------- | --------------- | ----------- |
| T     T | *F*  T  **T** T | F    *F*  F |
| T     F | *T*  T  **F** F | F    *T*  T |
| F     T | *T*  F  **F** T | T    *T*  F |
| F     F | *T*  F  **F** F | T    *T*  T |
- They are logically equivalent, because each row has the same truth value.
	- No counter-example.
#### Logical Consistency

> [!Definition] ‘Joint logical consistency’ definition:
> - A<sub>1</sub>, A<sub>2</sub>, . . . , A<sub>n</sub> are **jointly logically consistent** iﬀ there is some valuation which makes them all true.
- At least one row on their truth table where all the statements main logical operators are true.
- Is ‘¬P’ logically consistent with ‘¬(P → ¬Q)’? 
	- First guess: 
		- A. yes; 
		- B. **==no==**.

| P     Q | ¬ P | ¬(P → ¬Q)          |
| ------- | --- | ------------------ |
| T     T | *F* | *T*     **F**    F |
| T     F | *F* | *F*     **T**   T  |
| F     T | *T* | *F*     **T**   F  |
| F     F | *T* | *F*     **T**   T  |
- NOT jointly logically consistent
	- truth of one would rule out the other
- **Intuition:**
	- A → B
	- ==
	- ¬A ∨ B
		- and
	- ¬(A → B)
	- ==
	- A ∧ ¬B
		- if conditional is true, negated to false
		- then P must be true
		- and antecedent is false
		- so opposite
		- can't coexist
#### Logical Entailment
- **Logical validity and entailment**:
> [!Definition] ‘Logical entailment’ definition:
> - The sentences A<sub>1</sub>, A<sub>2</sub>, . . . , A<sub>n</sub> **logically entail** the sentence *C* if there is *no* valuation of the atomic sentences which makes all of A<sub>1</sub>, A<sub>2</sub>, . . . , A<sub>n</sub> true and *C* false.
- In other words, the argument from A<sub>1</sub>, A<sub>2</sub>, . . . , A<sub>n</sub> to *C* is **logically valid** iﬀ there’s no row of their joint truth table where all of A<sub>1</sub>, A<sub>2</sub>, . . . , A<sub>n</sub> are true and *C* is false.
	- In other words, iﬀ it’s logically impossible for the premises to be true while the conclusion is false.
#### Validity Symbolism

- A new symbol (which is not part of our object language in this class, TFL): 
	- ### **`‘⊨’`**
- $$A_1, A_2, ... , A_n ⊨ C$$
- Translation: A<sub>1</sub>, A<sub>2</sub>, ... , A<sub>n</sub> **entail** the sentence *C*.
	- In other words, the argument from A<sub>1</sub>, A<sub>2</sub>, ... , A<sub>n</sub> to *C* is **valid**.
- Example:
	- P, (P → (Q ∨ R)), ¬R ⊨ Q

### Valid Truth Tables
#### Using truth tables to prove validity
- **Validity testing procedure**: 
	- find lines where the conclusion is **false**, and check whether **all** of the premises are true.
- If there is at least one line where all of the premises are true, and the conclusion is false, then the argument is not valid. 
	- Otherwise, the argument is valid.
- First pass: 
	- is this simple argument valid? 
		- A. **==yes==**; 
		- B. no.
			- A → B, ¬B ∨ A ∴ B ↔ A

| A     B | A → B | ¬B ∨ A     | B ↔ A |
| ------- | ----- | ---------- | ----- |
| T     T | .   T | F.   **T** | .   T |
| T     F | .   F | T.   **T** | .   F |
| F     T | .   T | F.   **F** | .   F |
| F     F | .   T | T   **T**  | .   T |
- no lines of truth table where all premises true and conclusion false
	- is logically valid
- intuition:
	- for any conditional
		- equivalent to negation of disjunction of antecedent
			- A → B
			- ==
			- ¬A ∨ B
		- premises are equivalent
		- can't have different truth values
			- so they are equal/bidirectional
#### Exercise
- ##### **Truth tables and Validity**:
	- Let’s test whether the following argument is valid: 
		- P ∨ (P → (¬P ↔ P)) ∴ ¬P
	- How many rows under the headers?
		1. (A) 2 
		2. (B) 4 
		3. (C) 1 
		4. (D) 8
	- Which connective in the premise must we begin with?
		- (A) ∨ 
		- (B) → 
		- (C) ¬ 
		- (D) ↔

| P   | P ∨ (P → (¬ P ↔ P)) | ¬ P |
| --- | ------------------- | --- |
| T   |                     | F   |
| T   |                     | F   |
| F   |                     | T   |
| F   |                     | T   |

| P   | ∨   | (P    | →   | (¬  | P   | ↔     | P   |
| --- | --- | ----- | --- | --- | --- | ----- | --- |
| T   | ==T==   | **T** | F   | *F* | T   | **F** | *T* |
| T   | ==T==   | **T** | F   | *F* | T   | **F** | *T* |
| F   | ==T==   | **F** | T   | *T* | F   | **F** | *F* |
| F   | ==T==   | **F** | T   | *T* | F   | **F** | *F* |

### Conditionals

| *A* | *B* | *A* → *B* |
| --- | --- | --------- |
| T   | T   | .   T     |
| T   | F   | .   F     |
| F   | T   | .   T     |
| F   | F   | .   T     |
- Assuming that the following sentences express material conditionals 
	- (that is, that ‘if...then...’ means the same as ‘→’), 
- Assess the truth value of the following sentences:
	1. If apples are animals, then apples have mouths.
		- **True**
	2. If apples are mammals, then apples are fruit.
		- **True**
	3. If apples are fruit, then apples are mammals.
		- **False**
	4. If it’s sunny today, then apples are fruit.
		- **True**
	5. If today is Tuesday and today is Wednesday, then apples are mammals.
		- **True**

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

Previous: [PHIL 10 Lecture 6](PHIL_10_LE_6.md).
Next: [PHIL 10 Lecture 8](PHIL_10_LE_8.md).