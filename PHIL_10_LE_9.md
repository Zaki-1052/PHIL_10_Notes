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

#### Introduction & Elimination Rules

- Most of the basic inference rules in our deduction system consist of “**introduction rules**” and “**elimination rules**” for each of the truth-functional connectives.
	- Let ‘△’ be an arbitrary truth-functional connective.
##### Introduction
> [!NOTE] Introduction Rules
> The inference rule △-Introduction allows you to make an inference **to** a sentence whose **main logical connective** is △.
>(So you’re introducing a new △ into the proof.)
- **Example**:
	1. (P ∧ Q)
	2. R
	- ---
	3. (P ∧ Q) **∧** R ∧I 1,2
		- (New conjunction introduced on line 3.)
##### Elimination
> [!NOTE] Elimination Rules
> The inference rule △-Elimination allows you to make an inference **from** a sentence whose **main logical connective** is △ (and perhaps other sentences).
>(So you’re “eliminating” an old △ to move forward.)
- **Example**:
	1. (L ∨ M) **∧** N
	2. (L ∨ M) ∧E 1
		- (Old conjunction on line 1 eliminated from line 2.)
#### Interpreting Rules

- *A* and *B* can be replaced with **any sentence in TFL**, 
	- including sentences that are logically complex.
- Lines *m* and *n* need not appear immediately after each other: 
	- they **can be separated** by other lines of the proof.
- An inference rule that takes two input sentences applies the same 
	- **regardless of what order** the lines appear in.
		- (So *m* and *n* could appear in reversed order.)

### More Inference Rules

#### Disjunction Introduction

- A disjunction is true just in case at least one of its disjuncts is true.
- So for any A, if we assume A is true, then we can deduce the disjunction of A with literally **any other sentence**.
- The style of reasoning here:
	- Example 1:
		1. Alex is angry.
		2. ∴ Alex is hungry or Alex is angry.
			- A little weird, but has to be valid.
	- Example 2:
		1. Alex is angry.
		2. ∴ Alex is angry or the Padres are a football team.
			- A little weirder, but has to be valid.
- Remember the truth table for ‘∨’: 
	- if at least one of the disjuncts is true, the disjunction is true.
- So the inference is valid.
- We’ll see later: 
	- some new disjuncts are more strategic to introduce than others.

$$
\begin{array}{l|l}
m & \mathcal{A} \\
  & \mathcal{A} \lor \mathcal{B} & \lor\text{I } m \\
\hline
\text{or} & \\
\hline
m & \mathcal{A} \\
  & \mathcal{B} \lor \mathcal{A} & \lor\text{I } m
\end{array}
$$

#### Provability
- `‘⊢’` is the **provability** symbol: 
	- from the lefthand side, you can prove the righthand side. 
		- Premises (separated by commas) go on the left; 
		- the conclusion goes on the right.
	- Show: (P ∧ Q) ⊢ (Q ∨ R)
- Proof:

#### Conditional Elimination
- Conditional elimination (→E) is sometimes called **modus ponens**:

> [!Proof] →Elimination
> *m* | A → B
>*n*  | *A*
>...| B →E m, n
- The style of reasoning here:
	1. If Jane is well, she came to class.
	2. Jane is well.
	3. Therefore, Jane came to class.
- Note that, as usual:
	- the rule applies the same when the lines **m** and **n** appear in reversed order
- *A* and *B* can be replaced with any TFL sentences
- lines *m* and *n* need not appear immediately after each other: 
	- they might be separated by other lines of the proof.
- Prove the following:
	- D, E, (D ∧ E) → F ⊢ F
		1. D :PR
		2. E :PR
		3. (D ∧ E) → F :PR
		4. D ∧ E :∧I  1,2
		5. F :→E  3,4
	- (N ∨ O) → (R ∨ S), M ∧ N ⊢ R ∨ S
		1. (N ∨ O) → (R ∨ S) :PR
		2. M ∧ N :PR
		3. N :∧E 2
		4. N ∨ O :∨I 3
		5. R ∨ S :→E 1,4

#### Biconditional Elimination
<-->E
$$
\begin{array}{l|l}
m & \mathcal{A} \leftrightarrow \mathcal{B} \\
n & \mathcal{A} \\
  & \mathcal{B} & \leftrightarrow\text{E } m,n \\
\hline
\text{or} & \\
\hline
m & \mathcal{A} \leftrightarrow \mathcal{B} \\
n & \mathcal{B} \\
  & \mathcal{A} & \leftrightarrow\text{E } m,n
\end{array}
$$
- The style of reasoning here:
	1. David is angry if and only if Cian is hungry.
	2. David is angry.
	3. ∴ Cian is hungry.
- or
	1. David is angry if and only if Cian is hungry.
	2. Cian is hungry.
	3. ∴ David is angry.
- Biconditionals behave like conditionals that go in both directions:
	- Biconditionals’ introduction and elimination rules are almost exactly like →I and →E — 
		- but you can use them in either direction.
- Show the following argument:
	- A ∧ B, A ↔ C ⊢ B ∧ (C ∨ D)
- Proof:
	1. A ∧ B
	2. A ↔ C
	3. ---
- Is this a correct use of biconditional elimination?
	1. C ↔ D
	2. ¬D
	3. ¬C ?
		- NO
- If you have a biconditional and you have one side of the biconditional, 
	- you can infer the other side.
		- ‘¬D’ is not the lefthand side or the righthand side of the biconditional on line 1.
			- So we don’t have both a biconditional and one side of the biconditional. 
				- So we’re not in a position to use that rule.
	- **Objection**: 
		- But isn’t this a valid inference?
	- **Reply**:
		- It is—but with proofs, you have to **prove** that it is, using only the rules.
			- You can’t just assume it!
- A proof is a step-by-step breakdown of the reasoning.
	- Even if the reasoning is obvious to you, the task of a proof is to demonstrate it to someone else—someone who only accepts the specific rules of the deduction system.

#### General Guidelines for Proofs
- You should always start by trying to **work backwards**: 
	- thinking about how you’d be able to reach that conclusion.
		- Example: 
			- think about what it would take to apply the **introduction** rule 
				- for the main logical operator of the conclusion.
- **Remember**: 
	- for a given argument, you can correctly apply various rules to the premises to infer various sentences. 
		- But that doesn’t mean you “have most of the proof”.
	- You can establish twenty lines from the premises, using rules perfectly, and have made **no progress whatsoever** on the proof.
- Whatever comes between your premises and your conclusion should be a stepping stone that **helps you toward the conclusion**.
	- Otherwise you’re just muddling around in the dark.
- Compare: 
	- I’ve walked ten miles. Does that mean I’m most of the way to Downtown? 
		- No—not if I’m walking in some random direction, or in circles!

### Inference Rules that use Subproofs
#### Conditional Introduction
> [!Proof] →Introduction
>*m*  |  | *A*
>.....|   ---
>*n*  |   | *B*
>
>....|  A → B →I m–n

$$
\begin{array}{l|ll}
m & \begin{array}{l|l} & \mathcal{A} \\ & \mathcal{B} \end{array} \\
n & \mathcal{A} \rightarrow \mathcal{B} & \rightarrow\text{I }m\text{-}n
\end{array}
$$

- → Introduction is a more complex rule. 
- Its form:
	1. Introduce a new temporary assumption: A
	2. Prove that this additional assumption allows us to establish that B.
	3. Conclude that, even without the temporary assumption, we may 
		- deduce the conditional: A → B.
- This style of reasoning:
	- ***Suppose** it’s the May 12. Sarah told me the deadline was in the first week of May. So in that case, the deadline will have already passed. Now, I’m not sure what date today actually is. But I do know that **if** it’s May 13th, **then** the deadline has already passed.*
- To visually represent that we’re adding a new, **temporary** assumption, and seeing what follows from it, we introduce a **subproof**.
- The extent of the subproof is represented in the Fitch system with a vertical line.
	- When that line ends, the subproof closes.
- When we make an inference from a subproof (e.g. A → B), we must
	- cite the subproof as a whole, e.g. 
		- “10-12” rather than “10, 11, 12”.
##### Example

- **Refresher**: 
	- P → Q is logically equivalent to:
		1. A. P ∨ Q
		2. B. ¬P ∨ Q
		3. C. P ∨ ¬Q
		4. D. ¬P ∨ ¬Q
	- A helpful rule: 
		- **reiteration** (R).
- Given this entailment, we can prove the following:
	- Q ⊢ P → Q
		1. -
#### Citation Rule


> [!info] **Citations**
> Any rule whose citation requires mentioning individual lines can mention any earlier lines, **except** for those lines which occur within a closed subproof.
> After a subproof ends, you **cannot** make use of individual lines it.
- **After a subproof ends, you cannot make use of individual lines it.**
	- Otherwise, the following terrible “proof” would be allowed:
		1. P
			2. Q
			3. Q ∧ Q :∧I 2,2
		2. 4. Q  ∧E 3
	- But then we could prove any ‘Q’ from any ‘P’. 
		- Anything would follow from anything!
#### Closing a Subproof
- When you close a subproof, you are discharging the assumptions of that subproof.
- **Rule**: 
	- You cannot refer back to any line that was obtained using discharged assumptions.
		- Once the subproof ends, you can only refer back to the subproof as a whole—
			- and only using specific rules, like →I, that take subproofs as input.
#### Subproofs

> [!info] Citations cont.
> Any rule whose citation requires mentioning an entire subproof can mention any earlier subproof, **except** for those subproofs which occur **within some other** closed subproof.
- A consequence of this: 
	- it **never** makes sense to close two subproofs at the same time.
##### Common mistake with subproofs
- Remember: 
	- to prove an argument, its conclusion can’t be inside a subproof.
		- Otherwise you haven’t shown that the conclusion follows from the premises—
			- you've at best shown that it follows from the premises plus your temporary assumptions. 
				- But that’s not what you were asked to prove.

##### Important strategy advice
- In principle, it is always permissible to open a new subproof with any additional assumption you find helpful.
	- But if you open a new subproof just because the conclusion would be easier to prove if you had an extra premise, **you’re wasting your time**.
- **Don’t open a subproof unless** you believe, from working backwards, that you’ll eventually want to be able to apply a **specific rule** that requires a subproof as an input, in order to establish a **specific sentence**.
	- That specific rule will determine what the **first and last lines** of your subproof ***have*** **to be** in order to use that rule.
##### Example


---

Previous: [PHIL 10 Lecture 8](PHIL_10_LE_8.md).
Next: [PHIL 10 Lecture 10](PHIL_10_LE_10.md).