---
course: PHIL 10
type: lecture
lecture_num: 11
date: 3/5
---

# PHIL 10 Lecture 11
- ## 3/5

## Logic Rules

- Rules of Logic
	- Our logical system—consisting just of the **basic rules** that you learned in Part 3 of the course—can be used to prove **any valid argument** in truth-functional logic.
		- Some proofs are more unwieldy than others.
	- To allow for simpler proofs, we permit some additional rules.
	- As we’ll see next week, these rules are derivable from our basic rules:
		- Using only basic rules, we can prove that inferences in the additional rules are valid.
			- These additional rules are merely for convenience.
### Disjunctive Syllogism

- Example of disjunctive syllogism:
	- “John has a dog or a cat. He doesn’t have a cat. So he has a dog.”
- Remember: 
	- if a disjunction is true, **at least one** of its disjuncts must be true.
		- So if one is false, the other one has to be true.
$$
\begin{array}{l|ll}
m & \mathcal{A} \lor \mathcal{B} & \\
n & \neg\mathcal{A} & \\
  & \mathcal{B} & \text{DS }m,n
\end{array}
$$
$$
\begin{array}{l|ll}
m & \mathcal{A} \lor \mathcal{B} & \\
n & \neg\mathcal{B} & \\
  & \mathcal{A} & \text{DS }m,n
\end{array}
$$
### Modus Tollens

- You proved the validity of Modus Tollens on the exam.
	- Remember Modus Ponens, aka conditional elimination.
$$
\begin{array}{l|ll}
m & \mathcal{A} \rightarrow \mathcal{B} & \\
n & \neg\mathcal{B} & \\
  & \neg\mathcal{A} & \text{MT }m,n
\end{array}
$$
$$
\begin{array}{l|ll}
m & \mathcal{A} \rightarrow \mathcal{B} & \\
n & \mathcal{A} & \\
  & \mathcal{B} & \rightarrow\text{E }m,n
\end{array}
$$
### Double Negation Elimination

- This one’s easy. You know that ‘A’ is logically equivalent to ‘¬¬A’.
	- ‘John isn’t not eating.” ⇒ ‘John’s eating.’
- Remember: 
	- you can only remove two negations at a time.
$$
\begin{array}{l|ll}
m & \neg\neg\mathcal{A} & \\
  & \mathcal{A} & \text{DNE }m
\end{array}
$$
### Law of the Excluded Middle
- We know that ‘**A ∨ ¬A**’ is a tautology.
- LEM allows us to reason just as though we were using disjunction elimination on ‘A ∨ ¬A’—without first proving that the tautology follows from our premises.
	- Called ‘law of the excluded middle’ because there is **no middle ground** between ‘A’ and ‘¬A’. No third option. One or the other *must* be true.
$$
\begin{array}{l|ll}
i & \begin{array}{l|l} & \mathcal{A} \\ & \mathcal{B} \end{array} \\
j & & \\
k & \begin{array}{l|l} & \neg\mathcal{A} \\ & \mathcal{B} \end{array} \\
l & \mathcal{B} & \text{LEM }i\text{-}j,k\text{-}l
\end{array}
$$

### De Morgan’s rules
- De Morgan’s rules (or laws):
	- ‘¬(P ∧ Q)’ is logically equivalent to ‘¬P ∨ ¬Q’.
	- ‘¬(P ∨ Q)’ is logically equivalent to ‘¬P ∧ ¬Q’.
- These are obvious if you remember what the sentences individually mean:
	- ‘Not both’ is equivalent to ‘either not this one or not that one’.
	- ‘Neither’ is equivalent to ‘not this one and not the that one’.
- Heuristic: 
	- When you push the negation through the parentheses, you flip the ‘∧’ or ‘∨’.
$$
\begin{array}{l|ll}
m & \neg(\mathcal{A} \land \mathcal{B}) & \\
  & \neg\mathcal{A} \lor \neg\mathcal{B} & \text{DeM, }m
\end{array}
$$
$$
\begin{array}{l|ll}
m & \neg\mathcal{A} \lor \neg\mathcal{B} & \\
  & \neg(\mathcal{A} \land \mathcal{B}) & \text{DeM, }m
\end{array}
$$
$$
\begin{array}{l|ll}
m & \neg(\mathcal{A} \lor \mathcal{B}) & \\
  & \neg\mathcal{A} \land \neg\mathcal{B} & \text{DeM, }m
\end{array}
$$
$$
\begin{array}{l|ll}
m & \neg\mathcal{A} \land \neg\mathcal{B} & \\
  & \neg(\mathcal{A} \lor \mathcal{B}) & \text{DeM, }m
\end{array}
$$


---

Previous: [PHIL 10 Lecture 10](PHIL_10_LE_10.md).
Next: [PHIL 10 Lecture 12](PHIL_10_LE_12.md).