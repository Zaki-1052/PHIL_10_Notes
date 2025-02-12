---
course: PHIL 10
type: lecture
lecture_num: 9
date: 2/12
---

# PHIL 10 Lecture 9
- ## 2/12

## A Natural Deduction System

### Proofs

#### Natural Deduction System

> [!info]
> - A **natural deduction system** includes a series of rules of valid inference, allowing us to give **formal proofs** that an argument is valid.
- Proofs in the **Fitch system** look like this:
```
1    | premise 1
     | ...
n    | premise *n*
     |---
n+1  | subconclusion 1     justification
     | :                   :
n+*m*| subconclusion *m*   justification
n+m+1| conclusion.         justification
```
- ***Above* the horizontal line**: 
	- premises (assumptions).
- ***Below* the horizontal line**: 
	- entailments of the premises.
- Right column: citing 
	- (**i**) *inference rules* and 
	- (**ii**) *relevant previous lines*.
#### Justifications

- When we correctly apply an inference rule, we are showing that 
	- some sentence **conclusively follows from** some other sentence(s).
- Apart from the premises/assumptions, 
	- each line of the proof is entailed by some previous lines, 
		- given some inference rule within our natural deduction system.
- Every line of the proof (apart from the premises/assumptions) all need a **justification**. 
- These justifications will involve:
	1. an appropriate **inference rule**
	2. **citation** of all previous lines that the inference rule takes as input,
		- in order to deliver the new line as output.
- (Premises are assumptions: 
	- they don’t need justifications. 
	- We have to start somewhere!)

### Conjunction & Inference

#### Reiteration

> [!Proof] Reiteration
>m | *A*
>    | *A*    R  *m*
- Reiteration allows you to repeat a line from earlier in your proof
	- (except closed subproofs).
- The style of reasoning here:
	1. It’s snowing.
	2. ∴ It’s snowing.
		- We’ll see later on why a rule like this could be useful.
#### ∧ Introduction

> [!Proof] ∧ Introduction
> *m* | *A*
> *n* | *B*
> ...| *A* ∧ *B* ∧I *m*, *n*
- For any two sentences (simple or complex), if you have both as premises or subconclusions in your argument, then you can infer their **conjunction**.
- The style of reasoning here:
	1. Jamie’s happy.
	2. Sammy’s angry.
	3. ∴ Jamie’s happy and Sammy’s angry.
#### ∧ Elimination

> [!Proof] ∧ Elimination
*m* | A ∧ B  
....| A ∧E --- *m*
or
*m* | A ∧ B  
....| B ∧E --- *m*
- If you have a conjunction as a premise or subconclusion in your argument, 
	- then you can infer either of its **conjuncts**.
- The style of reasoning here:
	1. It’s Monday and the sun is shining.
	2. ∴ The sun is shining.
##### Example
- **∧ Elimination**
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
##### Comparison
- **Rules only look at main logical operators**
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

### Introduction & Elimination Rules

- Most of the basic inference rules in our deduction system consist of “**introduction rules**” and “**elimination rules**” for each of the truth-functional connectives.
	- Let ‘△’ be an arbitrary truth-functional connective.
#### Introduction
> [!NOTE] Introduction Rules
> The inference rule △-Introduction allows you to make an inference **to** a sentence whose **main logical connective** is △.
>(So you’re introducing a new △ into the proof.)
- **Example**:
	1. (P ∧ Q)
	2. R
	- ---
	3. (P ∧ Q) **∧** R ∧I 1,2
		- (New conjunction introduced on line 3.)
#### Elimination
> [!NOTE] Elimination Rules
> The inference rule △-Elimination allows you to make an inference **from** a sentence whose **main logical connective** is △ (and perhaps other sentences).
>(So you’re “eliminating” an old △ to move forward.)
- **Example**:
	1. (L ∨ M) **∧** N
	2. (L ∨ M) ∧E 1
		- (Old conjunction on line 1 eliminated from line 2.)


---

Previous: [PHIL 10 Lecture 8](PHIL_10_LE_8.md).
Next: [PHIL 10 Lecture 10](PHIL_10_LE_10.md).