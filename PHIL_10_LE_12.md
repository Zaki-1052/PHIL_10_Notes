---
course: PHIL 10
type: lecture
lecture_num: 12
date: 3/7
---

# PHIL 10 Lecture 12
- ## 3/7

## Logical Concepts for Proofs

### Proof Theoretic Concepts

#### Extending our logical concepts to proofs!

| Part I                   | Part II                        | Parts III & IV           |
| ------------------------ | ------------------------------ | ------------------------ |
| **Analytic**             | **Logical**                    | **Provable**             |
| *semantic*               | *logical form*                 | *syntactic*              |
| (meanings of all words)  | (meanings only of connectives) | (no meanings—just rules) |
| ---                      | ---                            | ---                      |
| analytic/necessary truth | logical truth/tautology        | theorem                  |
| valid arguments          | logically valid arguments      | provable arguments       |
| necessary equivalence    | logical equivalence            | provable equivalence     |
| joint possibility        | joint logical consistency      | can't prove ⊥            |
| joint impossibility      | logical inconsistency          | can prove ⊥              |
### Provability

- A new symbol, which is not in our object language (TFL), but instead in our metalanguage:
	- ‘⊢’.
- When we say..
	- A1, A2, . . . An ⊢ C
- we mean: 
	- Conclusion C is **provable** from assumptions 
		- A1, A2, . . . An.
#### Theorems

> [!Theorem]
> - A **theorem** is a sentence that can be proven without any assumptions.
- This corresponds to the notion of a **logically necessary truth**, aka a **tautology**.
- Given that our natural deduction system only allows us to prove valid arguments, every theorem will be a tautology.
- Notation: if A is a theorem:
	- ⊢ A
#### Provable equivalence

> [!Definition] Provable Equivalence
> - Two sentences *A* and *B* are **provably equivalent** iﬀ each can be proved from the other; 
> 	- i.e., both A ⊢ B and B ⊢ A.

- To demonstrate provable equivalence, you will require two proofs.

#### Provable Inconsistency

> [!Definition] Provable Inconsistency
> - The sentences A1, A2, . . . An are **provably inconsistent** iﬀ a contradiction can be proven from them, i.e. A1, A2, . . . An ⊢ ⊥.

### Reminder of my general recommendations for proofs
#### Try working backwards:
- To prove a **negation** ¬A, try using negation introduction: 
	- temporarily assume A and see whether you can prove a contradiction ⊥.
- To prove **conditional** A → B, try using conditional introduction: 
	- temporarily assume A and see whether you can prove B. 
		- (Similarly for a biconditional, with its introduction rule.)
- **In general**: 
	- look at the main logical connective of your **conclusion**
	- and consider how you could apply its **introduction** rule.
- Sometimes it’s useful to try indirect proof. 
	- Temporarily suppose the negation of your conclusion, 
		- and see whether you can prove a contradiction.
#### Try working forwards:
- In general: look at the main logical connectives of your **premises** and consider how you could apply their **elimination** rules.
	- Especially if you have a **disjunction** as a premise! 
		- Very often disjunction elimination is the way to go.
- Careful: 
	- To prove a **theorem**, there’s no real option of working forwards:
		- working backwards is your best bet.
- **Try out different strategies.**

---

Previous: [PHIL 10 Lecture 11](PHIL_10_LE_11.md).
Next: [PHIL 10 Lecture 13](PHIL_10_LE_13.md).