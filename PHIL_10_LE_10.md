---
course: PHIL 10
type: lecture
lecture_num: 10
date: 2/14
---

# PHIL 10 Lecture 10
- ## 2/14

## A Natural Deduction System 2

### Inference Rules that use Subproofs
#### Conditional Introduction
> [!Proof] →Introduction
>*m*  |  | *A*
>....| |---
>*n*  |..| *B*
>
>...|  A → B →I m–n

$$
\begin{array}{l|ll}
m & \begin{array}{l|l} & \mathcal{A} \\ & \mathcal{B} \end{array} \\
n & \mathcal{A} \rightarrow \mathcal{B} & \rightarrow\text{I }m\text{-}n
\end{array}
$$

- → Introduction is a more complex rule. 
- Its form:
	1. Introduce a new **temporary assumption**: *A*
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
		2. **B. ¬P ∨ Q**
		3. C. P ∨ ¬Q
		4. D. ¬P ∨ ¬Q
	- A helpful rule: 
		- **reiteration** (R).
- Given this entailment, we can prove the following:
	- Q ⊢ P → Q
		- 1. Q :PR
			- 2. P :AS
			- 3. Q :R 1
		- 4. P → Q   :→I 2-3

#### Citation Rule

> [!info] **Citations**
> Any rule whose citation requires mentioning individual lines can mention any earlier lines, **except** for those lines which occur within a closed subproof.
> After a subproof ends, you **cannot** make use of individual lines it.
- **After a subproof ends, you cannot make use of individual lines it.**
	- Otherwise, the following terrible “proof” would be allowed:
		- 1. P
			- 2. Q
			- 3. Q ∧ Q :∧I 2,2
		- 4. Q  ∧E 3
	- But then we could prove any ‘Q’ from any ‘P’. 
		- Anything would follow from anything!
	- This isn't valid and isn't allowed.
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
- Suppose I’m trying to prove that the following argument is valid:
	- P ⊢ Q → (P ∧ Q)
		- Often, to prove a conditional, it’ll be helpful to use a subproof that you can use for →I.
			- But for →I, the subproof should begin with the **antecedent** and establish the **consequent**.
	1. P
	2. (P
	3. ...)
	4. -
#### Proving Theorems
- **Fun fact**: 
	- we can use subproofs as a means of proving theorems!
- A theorem is a sentence that you can prove without any premises.
	- Example: 
		- let’s prove the following: 
			- ⊢ A → A.
	1. (A  :AS
	2. A   :R 1)
	3. A → A   :→I 1-2
		- Do we need a subproof to prove this?
#### Biconditional Introduction
$$
\begin{array}{l|ll}
i & \begin{array}{l|l} & \mathcal{A} \\ & \mathcal{B} \end{array} \\
j & \\
k & \begin{array}{l|l} & \mathcal{B} \\ & \mathcal{A} \end{array} \\
l & \mathcal{A} \leftrightarrow \mathcal{B} & \leftrightarrow\text{I }i\text{-}j,k\text{-}l
\end{array}
$$
- Biconditional introduction is very similar to conditional introduction, 
	- except you have to work in both directions:
		- It’s though you’re establishing 
			- *A* → *B* and *B* → *A*.
		- Hence two subproofs.
- A ∧ B ⊢ A ↔ B
#### Disjunction Elimination
$$
\begin{array}{l|ll}
m & \mathcal{A} \lor \mathcal{B} & \\
i & \begin{array}{l|l} & \mathcal{A} \\ & \mathcal{C} \end{array} & \\
j & & \\
k & \begin{array}{l|l} & \mathcal{B} \\ & \mathcal{C} \end{array} & \\
l & \mathcal{C} & \lor\text{E }m,i\text{-}j,k\text{-}l
\end{array}
$$
- An example of the style of reasoning used in disjunction elimination:
	- *I have either apples or blueberries. Suppose I have apples. That entails that I have fruit. Now, suppose instead that I have blueberries. That also entails that I have fruit. So either way, I have fruit.*
- Disjunction elimination is sometimes called ‘**proof by cases**’
	- Introduce a new subproof for each disjunct. 
		- If something follows from both of the disjuncts considered individually, then it must follow from the disjunction.
	- Note: when we assume that *A* is true, we’re **not** assuming that *B* is false. 
		- (And vice versa.)
	- So no need to consider separately what would follow if both *A* and *B* are true.
- **Example**:
	- A, (A → B) ∨ (A → C) ⊢ B ∨ C
#### Negation and Contradiction
- For negation introduction and elimination, we make use of the notion of **contradiction**, symbolized as “⊥”
- We have a contradiction whenever both a sentence and its negation appear within the proof.
- ¬E
$$
\begin{array}{l|ll}
m & \mathcal{A} & \\
n & \neg\mathcal{A} & \\
  & \bot & \neg\text{E }m,n
\end{array}
$$
	- For any sentence A, it’s clear that A and¬A contradict each other:
		- It cannot be the case that both are true.
#### Negation Introduction
- ¬I
$$
\begin{array}{l|ll}
i & \begin{array}{l|l} & \mathcal{A} \\ & \bot \end{array} & \\
j & \neg\mathcal{A} & \neg\text{I }i\text{-}j
\end{array}
$$
- Negation introduction is often called:
	- “Reductio ad absurdum”
	- “Proof by contradiction”
- **Basic procedure**: 
	- to prove ¬*A* using this method, assume *A* and prove a contradiction ⊥.
- If our premises ensure that assuming that *A* leads to a contradiction,
	- then our premises rule out the truth of A.
		- So they entail that¬A.
#### Indirect Proof
- A closely related inference rule that is also part of our proof system is indirect proof:
- IP:
$$
\begin{array}{l|ll}
i & \begin{array}{l|l} & \neg\mathcal{A} \\ & \bot \end{array} & \\
j & \mathcal{A} & \text{IP }i\text{-}j
\end{array}
$$
- Here we temporarily assume a negated sentence ¬A. 
	- If a contradiction follows, then it must be that¬A is false, and so A is true.
##### Example: Double Negation
- Using these two rules, we can show that P ⊢¬¬P and that¬¬P ⊢ P. 
	- (In other words: P and¬¬P are logically equivalent.)
		- What rule should we cite on line 4? 
			- A. ¬E 
			- B. IP 
			- C. ¬I
#### Explosion
- Recall: 
	- Given our definition of validity, 
		- **every argument with contradictory premises is valid**.
	- (After all: 
		- *an argument is valid iﬀ it’s impossible for the premises to be true while the conclusion is false*.)
	- So: 
		- *a contradiction entails anything and everything*! 
			- This is the **Principle of Explosion**.
$$
\begin{array}{l|ll}
m & \bot & \\
  & \mathcal{A} & \text{X }m
\end{array}
$$
	- As with disjunction introduction, 
		- you’ll find that only some inferences are actually useful.
### Examples

#### Example 1

---

Previous: [PHIL 10 Lecture 9](PHIL_10_LE_9.md).
Next: [PHIL 10 Lecture 11](PHIL_10_LE_11.md).