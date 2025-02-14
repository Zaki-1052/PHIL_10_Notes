---
course: PHIL 10
type: lecture
lecture_num: 8
date: 2/7
---

# PHIL 10 Lecture 8
- ## 2/7
	- ## Proofs

## Introduction to Proofs

### Truth Tables Shortcomings

- The central concern of logic is **valid inference**.
- Truth tables can be used to demonstrate: 
	- whether arguments in truth-functional logic are valid.
- But they’re not always **convenient**: consider the following argument:
	- A, A → B, B → C, C → D, D → E, E → F, F → G, G → H, H → I, I → J, J → K ∴ K
- Questions:
	- Is this argument valid?
		- A. Yes
		- B. No
	- This contains 11 atomic sentences.
	- How many rows would its truth able have?
		- A. 11
		- B. 11^2
		- C. 2^11
- A second shortcoming of truth tables: 
	- they obscure the kind of reasoning or inferences that we use to understand arguments.
		- A, A → B, B → C, C → D, D → E, E → F, F → G, G → H, H → I, I → J, J → K ∴ K
	- We know this is valid because we know that A together with A → B entails B, and that B together with B → C entails C, etc.
		- That is, we know that for any *A*, *B*, the following argument schema is valid:
			1. *A*
			2. *A* → *B*
			3. ∴ *B*
- **Henceforth**...
	- For the rest of the course, we will be learning a diﬀerent way of demonstrating that an argument is valid.
		- Part III of the course: 
			- simple proofs in a natural deduction system
		- Part IV of the course: 
			- complex proofs

### Natural Deduction System

- A **natural deduction system** includes a series of rules of good inference.
	- These rules are meant to allow us to move from sentences to their entailments. 
		- (Hence “deduction” system.)
- Natural deduction systems allow us to give formal proofs that an argument is valid.
> [!Definition] Formal Proof
> A **formal proof** is a sequence of sentences, some of which are marked as premises, that provide a step-by-step demonstration that a conclusion follows from some premises.
#### The Fitch system
- Proofs in the Fitch system look like this:
```
| premise 1
| ...
| premise *n*
|---
| subconclusion 1     justification
| :                   :
| subconclusion *m*   justification
| conclusion.         justification
```
- ***Above* the horizontal line**: 
	- premises (assumptions).
- ***Below* the horizontal line**: 
	- entailments of the premises.
##### Example
- ¬(A ∧ B), A ∨ B, A ↔ B ∴ B
	- In the Fitch system, we can represent this argument as follows:
- Proof:
	1. ¬(A ∧ B)
	2. A ∨ B
	3. A ↔ B
	- ---
	- :
	- *n*.      *B*      Justification
- A formal proof will demonstrate, step by step, why premises 1–3 license the inference to the conclusion on line *n*.
#### Proofs Without Meanings
- Interpreted vocabulary of TFL: 
	- ¬, ∧, ∨, →, ↔, (, ) etc.
- If an argument in TFL is valid, we can establish that it is valid *without* *knowing the meaning of anything else*. 
	- It’s valid just by virtue of its **logical structure**.
		- So we don’t need to worry about ambiguity or context-sensitivity
- Example:

> [!Example] Proof
> 1. | A
> 2. | A -> B
> | \-\-\-
> 1. | C
#### Simple Inference Rule
- An (almost confusingly simple) example of an inference rule: 
	- If P is true and Q is true, then (obviously) P ∧ Q is true.
> [!Proof]
> 1. | P
> \| :
> 8. | Q
> \| :
> 1. P ∧ Q ∧I 3, 8
- The inference on line 12 is justified because we apply the inference rule:
	- **∧ Introduction**.

### ∧ Introduction

> [!Proof] ∧ Introduction
> *m* | *A*
> *n* | *B*
> ...| *A* ∧ *B* ∧I *m*, *n*
- For any two sentences (simple or complex), if you have both as premises or subconclusions in your argument, then you can infer their **conjunction**.
#### Example
$$\quad (A \land B) \leftrightarrow \neg(C \lor \neg D)$$
$$\quad (E \lor B) \lor (A \land \neg C)$$
$$\quad [(A \land B) \leftrightarrow \neg(C \lor \neg D)] \land [(E \lor B) \lor (A \land \neg C)] \quad \land I \; 1, 2$$

- Notice that by applying ∧ Introduction, we introduce a new ‘∧’ into the proof.

### Inference rules

- Most of the basic inference rules in our deduction system consist of “introduction rules” and “elimination rules” for each of the truth-functional connectives.
	- Let ‘△’ be an arbitrary truth-functional operator.

> [!NOTE] Introduction Rules
> The inference rule △-Introduction allows you to make an inference to a sentence whose main logical connective is △.

> [!NOTE] Elimination Rules
> The inference rule △-Elimination allows you to make an inference from a sentence whose main logical connective is △ (and perhaps other sentences).

#### Elimination Rule
- Conjunction also has a very simple elimination rule: 
	- if you know that it’s windy and it’s rainy, then (obviously) you can infer that it’s windy. 
		- (You can also infer that it’s rainy.)

> [!NOTE] Proof
> 21. | W ∧ R
> | :
> 25. | *W* ∧E 21
- Whenever the sentence on line 21 is true, the sentence on line 25 is guaranteed to be true.

### ∧ Elimination

> [!Proof] ∧ Elimination
*m* | A ∧ B  
....| A ∧E --- *m*
or
*m* | A ∧ B  
....| B ∧E --- *m*
- If you have a conjunction as a premise or subconclusion in your argument, 
	- then you can infer either of its **conjuncts**.
#### Example

```
1. | (A ∨ B) ∧ (D ∨ E)
----
2. D ∨ E     ∧E 1
```
- **Caution**: 
	- we are only able to apply ∧ Elimination to conjunctions—
		- that is, to sentences with ‘∧’ as their main logical operator.
- A **misapplication** of ∧ Elimination:
```
1. | P ↔ (Q ∧ R)
----
2. R     ∧E 1
```
- This is not even a valid inference...
	- When might 1 be true while 2 is false? 
#### Comparison
- Similarly:
	- we can only use ∧ Introduction to infer sentences with ‘∧’ as their main logical operator.
> [!warning] A misapplication of ∧ Introduction  
1 | P ∨ Q  
2 | R  
3 | P ∨ (Q ∧ R) ∧I 1, 2

> [!success] A correct application of ∧ Introduction  
1 | P ∨ Q  
2 | R  
3 | (P ∨ Q) ∧ R ∧I 1, 2

### Justifications
- When we correctly apply an inference rule, we are showing that some sentence **conclusively follows from** some other sentence(s).
- Apart from the premises, each line of the proof is entailed by some previous lines, given some inference rule within our natural deduction system.
- Every line of the proof (apart from the premises) all need a justification.
- These justifications will involve:
	1. an appropriate **inference rule**
	2. **citation** of all previous lines that the inference rule takes as input, 
		- in order to deliver the new line as output.
- (Premises are assumptions: 
	- they don’t need justifications. 
	- We have to start somewhere!)
#### Example
- `‘⊢’` is the provability symbol: 
	- ‘A<sub>1</sub>, . . . , A<sub>n</sub> ⊢ C’ can be read as:
	- ‘from ‘A<sub>1</sub>, . . . , A<sub>n</sub> one can prove that C’.
- Let’s prove that the following argument is valid:
	- (P → Q) ∧ (R → S) ⊢ (R → S) ∧ (P → Q)

| 1   | (P → Q) ∧ (R → S) | :PR      |
| --- | ----------------- | -------- |
| 2   | (P → Q)           | :∧E 1    |
| 3   | (R → S)           | :∧E 1    |
| 4   | (R → S) ∧ (P → Q) | :∧I 4, 3 |

---

Previous: [PHIL 10 Lecture 7](PHIL_10_LE_7.md).
Next: [PHIL 10 Lecture 9](PHIL_10_LE_9.md).