---
course: PHIL 10
type: lecture
lecture_num: "5"
date: 1/24
---

# PHIL 10 Lecture 5
- ## 1/24
	- ## Truth Tables

## Introduction to Truth Tables

### Truth-Functionality Intro

#### Truth Values

- Every sentence of TFL has a truth value: 
	- either true (T) or false (F).
		- (‘T’ and ‘F’ without italics are not atomic sentences: 
			- they are abbreviations for truth values.)
- The truth values of complex sentences are determined by the truth values of their atomic sentences and how they are composed.
	- If you know the truth value of ‘P’, you know the truth value of ‘¬P’.
	- If you know the truth value of ‘P’ and the truth value of ‘Q’, you know the truth value of ‘(P ∧ Q)’.
	- Etc.

#### Truth-Functionality

- To know the truth value of a complex sentence of TFL, you only need to know:
	1. the truth values of the atomic sentences in it, and
	2. the complex sentence’s structure.
		- You don’t need other background information.
		- You don’t need to know what the atomic sentences mean.

#### Truth Tables

- **Truth tables show how the truth value of a whole sentence is a function of the truth values of its subsentences + logical form**
- If ‘P’ is true, then ‘¬P’ is 
	- False
- If ‘P’ is false, then ‘¬P’ is
	- True

##### Negation

- A way of displaying this information:
	- **Characteristic truth table of ‘¬’**

| *A* | ¬*A* |
| --- | ---- |
| T   | F    |
| F   | T    |
- Left column: 
	- all possible truth values for the input sentence.
- Right column: 
	- the resulting truth value for the complex sentence.

### Truth-Functionality Explained

#### Definition

> [!Definition]
> - Definition of ‘truth-functional’:
> 	- A connective is **truth-functional** iﬀ the truth value of a sentence with that connective as its main logical operator is uniquely determined by the truth value(s) of the constituent sentence(s).

- Let ‘△’ be an arbitrary truth-functional operator.
	- Suppose ‘△’ needs only one input sentence (like negation).
		- Then the truth value of A determines the truth value of △A.
	- Suppose ‘△’ needs two input sentences (like all other connectives in TFL).
		- Then the truth values of A and of B determine the truth value of (A △ B).

#### Explanation

- In TFL, all connectives are truth-functional.
- In natural language, not all connectives are truth-functional: 
	- e.g. ‘because’. 
		- (TFL has no ‘because’ connective.)
- **Examples**:
	- I’m hungry **because** I haven’t eaten lunch.
		- (Subsentences are both **true**, full sentence is **true**)
	- It’s Wednesday **because** it’s sunny.
		- (Subsentences are both **true**, full sentence is **false**)
- With ‘and’, two true input sentences always yield a true conjunction.
- With ‘because’, the two input sentences also need to be true. 
	- But it’s not always the case that two true input sentences yield a true ‘because’-statement.

### Truth Tables

- #### **Characteristic Truth Tables of TFL Connectives**

#### And

- Characteristic truth table for conjunction (‘∧’):

| *A* | *B* | *A* ∧ *B* |
| --- | --- | --------- |
| T   | T   | T         |
| T   | F   | F         |
| F   | T   | F         |
| F   | F   | F         |

- Left of the bar: every possible combination of truth values for the conjuncts.
	- Note: this truth table has four rows, while the truth table for ‘¬’ had only two. Why?
	- What this tells us: 
		- for any conjunction ‘A ∧ B, the only rows on which the conjunction as a whole is true is are rows where both of its two conjuncts A and B are true.

#### Or

- Let’s fill in the characteristic truth table for disjunction (‘∨’).

| *A* | *B* | *A* ∨ *B* |
| --- | --- | --------- |
| T   | T   | T         |
| T   | F   | T         |
| F   | T   | T         |
| F   | F   | F         |

#### If Table

- ##### **Conditionals in TFL**

| *A* | *B* | *A* → *B* |
| --- | --- | --------- |
| T   | T   | T         |
| T   | F   | F         |
| F   | T   | T         |
| F   | F   | T         |

- *Memorize this:* 
	- the ***ONLY*** case where *A* → *B* is ***false*** is:
		- **when the antecedent is true and the consequent is false.**
- A → B is true whenever the antecedent is false or the consequent is true.

#### Conditionals

- **A → B is true whenever the antecedent is false or the consequent is true.**
	- In other words:
	- **Material Conditionals**:
		- **A → B is logically equivalent to ¬A ∨ B.**
- Remember: 
	- there’s no requirement that the antecedent and the consequent are causally connected, or relevant to each other *in any way*.

#### Biconditional

- Characteristic truth table of the biconditional ‘↔’:

| *A* | *B* | *A* ↔ *B* |
| --- | --- | --------- |
| T   | T   | T         |
| T   | F   | F         |
| F   | T   | F         |
| F   | F   | T         |
- As with the conditional, there’s no requirement that the lefthand and righthand sides are related to each other.
	- They just have to have the **same truth value**—*coincidentally or not*.

### Arbitrary Sentences

- **Truth tables for arbitrary sentences of TFL**

#### Valuations

##### Definition

> [!Definition] 'Valuation' Definition
> A **valuation** is any assignment of truth values to particular atomic sentences of TFL.

- Left of the vertical line, we have **valuations**.
- You can think of these as sets of possible worlds 
	- (e.g. all the worlds where all atomics are true; etc).
- Every subsentence has a column representing its truth value at each valuation. 
	- For atomics, that just repeats what’s on the left.
	- For each complex subsentence, its column appears under its main logical connective.
- The column under the **main connective** tells you the truth value, at each valuation, of the sentence as a whole.

| *P* | *Q* | *P* → (*P* ∨ *Q*)   |
| --- | --- | ------------------- |
| T   | T   | T  **T**  T  *T*  T |
| T   | F   | T  **T**  T  *T*  F |
| F   | T   | F  **T**  F  *T*  T |
| F   | F   | F  **T**  F  *F*  F |

##### Explained

1. To the left: all possible valuations of the atomics.
2. Under each atomic on the right, copy its truth value at each row
3. Under an innermost connective, fill in the truth value of the subsentence, according to the characteristic truth table for the connective
4. Work from innermost to outermost connectives. 
	- Main connective last
- For each connective, before you can fill out its column (which tells you when its scope is true or false), its **input** sentences must be filled in first. 
- Before a conjunction’s column, fill in each conjunct’s column. 
	- So **start with atomics** and **work your way out**.

##### Order

- ###### **How to Order Valuations**
- **How Many Rows?**
	- If a sentence contains *n* different atomic sentences, its truth table should have: 
		- 2<sup>n</sup> rows under the headers.
- The convention we use to fill in the possible valuations:
	- **Leftmost atomic**: 
		- mark the first half of rows ‘T’ and the second half of the rows ‘F’
	- **Second leftmost atomic**: 
		- first quarter of rows ‘T’, second quarter ‘F’, and repeat.
	- **Third leftmost atomic**: 
		- first eighth of rows ‘T’, second eighth ‘F’, and repeat.
	- If you do this correctly, the rightmost atomic will alternate between ‘T’ and ‘F’ at every row.
- You’re **required** to follow this convention.

##### Examples

###### Example 1

| P   | Q   | ((P ∧ Q) → P) |
| --- | --- | ------------- |
| T   | T   |               |
| T   | F   |               |
| F   | T   |               |
| F   | F   |               |

###### Example 2

| A   | B   | (¬ (¬ A → B) ∨ A) |
| --- | --- | ----------------- |
| T   | T   |                   |
| T   | F   |                   |
| F   | T   |                   |
| F   | F   |                   |

###### Example 3

- **(C ↔ (D ∨ E)) ∧ ¬C**


### Conditionals

| *A* | *B* | *A* → *B* |
| --- | --- | --------- |
| T   | T   | T         |
| T   | F   | F         |
| F   | T   | T         |
| F   | F   | T         |
- Assuming that the following sentences express material conditionals (that is, that ‘if...then...’ means the same as ‘→’), assess the truth value of the following sentences:
	1. If apples are animals, then apples have mouths.
		- 
	2. If apples are mammals, then apples are fruit.
		- 
	3. If apples are fruit, then apples are mammals.
		- 
	4. If it’s sunny today, then apples are fruit.
		- 
	5. If today is Tuesday and today is Wednesday, then apples are mammals.
		- 

### Quizlet

#### Question 1

- What connective is represented by the truth table below?

| *A* | *B* | *A* \[?\] *B* |
| --- | --- | ------------- |
| T   | T   | T             |
| T   | F   | F             |
| F   | T   | F             |
| F   | F   | F             |
- B. **∧**
	- *and*

#### Question 2

- What connective is represented by the truth table below?

| *A* | *B* | *A* \[?\] *B* |
| --- | --- | ------------- |
| T   | T   | T             |
| T   | F   | T             |
| F   | T   | T             |
| F   | F   | F             |
- A. **∨**
	- *or*

#### Question 3

- What connective is represented by the truth table below?

| *A* | *B* | *A* \[?\] *B* |
| --- | --- | ------------- |
| T   | T   |               |
| T   | F   |               |
| F   | T   |               |
| F   | F   |               |
- C. **↔**
	- *biconditional*


---

Previous: [PHIL 10 Lecture 4](PHIL_10_LE_4.md).
Next: [PHIL 10 Lecture 6](PHIL_10_LE_6.md).