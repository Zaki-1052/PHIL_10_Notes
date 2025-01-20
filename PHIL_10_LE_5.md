---
course: PHIL 10
type: lecture
lecture_num: 5
date: 1/19
---
# PHIL 10 Lecture 4
- ## 1/17
	- ## Truth-Functional Logic

## Sentences of TFL

### Terminology

- 'A ∧ B'
	- 'A' and 'B' are conjuncts
- 'A ∨ B'
	- 'A' and 'B' are disjuncts
- 'A → B'
	- 'A' is the antecedent; 'B' is the consequent
- 'A ↔ B'
	- 'A' is the lefthand side; 'B' is the righthand side

### Symbolization Exercise

- 'If you bring me some pizza, I'll give you ten dollars and a firm handshake.'
	- P: You bring me some pizza
	- T: I'll give you ten dollars 
	- H: I'll give you a firm handshake
	- Options:
		- A. (P → T)
		- B. (P → (T ∧ H))
		- C. ((P → T) ∧ H)
		- D. ((P → T) ∨ H)

### Symbols of TFL

- Atomic sentences
	- A, B, C, . . . Z, A₁, A₂, . . . B₁, B₂, . . .
- Logical connectives
	- ¬, ∧, ∨, →, ↔
- Brackets
	- (, )

#### Notes
- Any string of these symbols will count as an expression of TFL
- Not all expressions of TFL are well-formed sentences of TFL
	- Examples of non-well-formed:
		- AB∧
		- → ¬P(

### Rules for TFL

1. Every atomic sentence is a sentence
2. If A is a sentence, then ¬A is a sentence
3. If A and B are sentences, then (A ∧ B) is a sentence
4. If A and B are sentences, then (A ∨ B) is a sentence
5. If A and B are sentences, then (A → B) is a sentence
6. If A and B are sentences, then (A ↔ B) is a sentence
7. Nothing else is a sentence

#### Example Construction: '(P ∧ (Q ∨ R))'
- By rule 1: 'Q' and 'R' are both sentences
- So, by rule 4: '(Q ∨ R)' is a sentence
- By rule 1: 'P' is a sentence
- So, by rule 3: '(P ∧ (Q ∨ R))' is a sentence
- Note: '∧' is the main logical operator (the outermost connective)

### Main Logical Operator

- Every sentence of TFL has a main logical operator
- The main logical operator is the connective that is introduced last
- Examples:
	- (A → (B ∨ C)) → main operator
	- ¬(A ∧ B) → ¬ main operator
	- ((¬E ∨ F)→ ¬¬G) → → main operator
	- (P ∧ (¬(R ∧ S)↔ Q)) → ∧ main operator

### Scope

#### Definition
- The scope of a connective (in a sentence) is the subsentence for which that connective is the main logical operator

#### Example
- In ((¬E ∨ F)→ ¬¬G):
	- Scope of first ¬: E
	- Scope of ∨: (¬E ∨ F)
	- Scope of →: ((¬E ∨ F)→ ¬¬G)
	- Scope of second ¬: ¬G
	- Scope of third ¬: ¬¬G

### Bracketing Conventions

- Brackets around each subsentence with exceptions:
	- No brackets around atomic sentences
	- No brackets around negations
	- Outermost brackets optional for non-negations
	- Round and square brackets are interchangeable
		- '[P ∨ Q]' equivalent to '(P ∨ Q)'

### Use vs. Mention

- Using language vs. talking about language
- Example:
	1. Leslie Knope is deputy director of the Parks Department
	2. 'Leslie Knope' is a proper name
	3. ∴ The deputy director of the Parks Department is a proper name
- Expression 'Leslie Knope' is:
	- used in sentence 1
	- mentioned in sentence 2

### Object Language vs. Metalanguage

- Object language: language being talked about
	- TFL for this class
- Metalanguage: language used to talk about object language
	- English
- Metavariables:
	- 'A', 'B', 'C', ... used to talk about any TFL expression
	- Used in augmented English
	- Different from particular atomic sentences of TFL ('A', 'B', 'C')

---

Previous: [PHIL 10 Lecture 3](PHIL_10_LE_3.md).
Next: [PHIL 10 Lecture 5](PHIL_10_LE_5.md).