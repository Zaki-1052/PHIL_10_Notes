---
course: PHIL 10
type: lecture
lecture_num: "4"
date: 1/17
---
# PHIL 10 Lecture 4
- ## 1/17
	- # Truth-Functional Logic

## Sentences of TFL

### Terminology

- '*A* ∧ *B*'
	- 'A' and 'B' are **conjuncts**.
- '*A* ∨ *B*'
	- 'A' and 'B' are **disjuncts**.
- '*A* → *B*'
	- 'A' is the **antecedent**; 
	- 'B' is the **consequent**.
- '*A* ↔ *B*'
	- 'A' is the **lefthand side**; 
	- 'B' is the **righthand side**.

### Symbolization Exercise

- 'If you bring me some pizza, I'll give you ten dollars and a firm handshake.'
	- *P*: You bring me some pizza
	- *T*: I'll give you ten dollars 
	- *H*: I'll give you a firm handshake
	- Options:
		- A. (P → T)
		- **B. (P → (T ∧ H))**
		- C. ((P → T) ∧ H)
		- D. ((P → T) ∨ H)

### Symbols of TFL

### Symbols

> [!Symbols]
> - Atomic sentences
> 	- A, B, C, . . . Z, 
> 	- A₁, A₂, ... B₁, B₂, ...
> - Logical connectives
> 	- `¬`, `∧`, `∨`, `→`, `↔`
> - Brackets
> 	- `(`
> 	- `)`

#### Notes
- Any string of these symbols will count as an **expression of TFL**
- Not all expressions of TFL are well-formed **sentences** of TFL
	- Examples of non-well-formed:
		- *AB*∧
		- `→ ¬P(`
	- How can we determine whether some string of symbols is a sentence of a language?

### Sentences of TFL

#### Rules for TFL

> [!Rules]
> 1. Every atomic sentence is a sentence
> 2. If A is a sentence, then ¬A is a sentence
> 3. If A and B are sentences, then (A ∧ B) is a sentence
> 4. If A and B are sentences, then (A ∨ B) is a sentence
> 5. If A and B are sentences, then (A → B) is a sentence
> 6. If A and B are sentences, then (A ↔ B) is a sentence
> 7. Nothing else is a sentence

#### Example Construction:

- **'(P ∧ (Q ∨ R))'**
	- By rule 1: 'Q' and 'R' are both sentences
		- So, by rule 4: '(Q ∨ R)' is a sentence
	- By rule 1: 'P' is a sentence
		- So, by rule 3: '(P ∧ (Q ∨ R))' is a sentence
- In the construction of this sentence out of atomic sentences and the rules for introducing connectives, ‘∧’ was the last connective introduced. 
	- That is, ‘∧’ is the main logical operator of the sentence (the outermost connective).

### Main Logical Operator

- Every complex sentence of TFL has a main logical operator
- Suppose that each sentence is constructed using rules 1–7 of TFL. 
	- The **main logical operator** of a sentence is the connective that is introduced *last*.
#### Examples
- What is the main logical operator for each of the following sentences?
- Examples:
	- (A → (B ∨ C)) 
		- → 
	- ¬(A ∧ B)
		- ¬
	- ((¬E ∨ F)→ ¬¬G)
		- →
	- (P ∧ (¬(R ∧ S)↔ Q))
		- ∧

### Scope

#### Definition of Scope

> [!Definition]
> - The **scope** of a connective (in a sentence) is the subsentence for which that connective is the main logical operator

#### Examples
- What is the scope of the highlighted connective?
- In ((¬E ∨ F)→ ¬¬G):
	- Scope of first ¬: 
		- ¬E
	- Scope of ∨: 
		- (¬E ∨ F)
	- Scope of →: 
		- ((¬E ∨ F)→ ¬¬G)
	- Scope of second ¬: 
		- ¬¬G
	- Scope of third ¬: 
		- ¬G
- ((¬E==<==4 > ∨F)==<==2 > →==<==3 > ¬==<==1 > ¬G)
- `((¬E<󰇉 > ∨F)<󰇇 > →<󰇈 > ¬<󰇆 > ¬G)`
- Setting aside A., which of these is *not* a subsentence of the sentence above?

#### Main Logical Operator

- If a sentence’s main logical operator is ‘∧’, we call the sentence as a whole a ‘**conjunction**’.
- If its main logical operator is a ¬, we call the sentence as a whole a ‘**negation**’.
	- And so on.

### Bracketing Conventions

- Generally, we place brackets (parentheses) around each subsentence of a sentence—with some conventional exceptions:
	- We don’t put brackets around atomic sentences.
	- We don’t put brackets around negations 
		- (i.e. sentences whose main operator is a negation).
	- The outermost brackets of a sentence that is not a negation are optional.
	- Round and square brackets are interchangeable: ‘`[P ∨ Q]`’ is equivalent to ‘`(P ∨ Q)`’

### Use vs. Mention

- Using language vs. talking about language:

- Sometimes we use language to talk about language:
	- Example:
		1. Leslie Knope is deputy director of the Parks Department
		2. 'Leslie Knope' is a proper name
		3. ∴ The deputy director of the Parks Department is a proper name
			- Is this valid?
				- (A. yes, B. no.)
	- To talk about expressions in a language, we **mention** those expressions.
	- To talk about other things in the world, we **use** linguistic expressions.
- The expression ‘Leslie Knope’ is: 
	- *used* in sentence and 
	- *mentioned* in sentence 2.

#### Use/Mention Conventions

- When an expression is **mentioned**, we should indicate this by: 
	- using quotation marks, or by oﬀsetting the expression.
		- ‘Leslie Knope’
			- Leslie Knope
> [!Offset]
> Leslie Knope

1. Leslie Knope is deputy director of the Parks Department
- ---
2. Someone is deputy director of the Parks Department

### Object Language vs. Metalanguage

> [!Comparison]
> - When we talk about a language, the language that we are talking about is called the ‘**object language**’.
> - The language that we use to talk about the object language is called the ‘**metalanguage**’.
- Example:
	- Object language for this class: TFL.
	- Metalanguage: English.

#### Metavariables

- Sometimes it’s useful to talk, not about specific sentences in TFL, but about an **arbitrary** sentence of TFL.

> [!Metavariables]
> '*A*', '*B*', '*C*', ... are symbols (called '**metavariables**') in augmented English, which we use to talk about any TFL expression.
> '*A*', '*B*', '*C*', ... are particular atomic sentences of TFL.

- If *A* is a sentence, then ¬*A* is a sentence.
	- ⇒ If ‘*C*’ is a sentence, ‘*¬C*’ is a sentence.
- If ‘A’ is a sentence, then ‘¬A’ is a sentence.
	- ⇒ If ‘*C*’ is a sentence, ‘*¬C*’ is a sentence.

#### Extra

- Why don’t we put quotation marks around the metavariables?
	- Consider the TFL sentence: 
		- ‘(Q → R)’.
	- I can refer to this sentence in a number of ways:
		- **‘(Q → R)’** is a conditional.
		- Let the sentence ‘(Q → R)’ be named ‘Fred’
			- **Fred** is a conditional.
		- *The sentence mentioned in the second line of this slide* is a **conditional**.
		- There is some sentence *A* in TFL such that *==A==* is a conditional.
	- No quotations around metavariables needed.

---

Previous: [PHIL 10 Lecture 3](PHIL_10_LE_3.md).
Next: [PHIL 10 Lecture 5](PHIL_10_LE_5.md).