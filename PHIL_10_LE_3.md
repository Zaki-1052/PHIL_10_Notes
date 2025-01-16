---
course: PHIL 10
type: lecture
lecture_num: "3"
date: 1/15
---

# PHIL 10 Lecture 3
- ## 1/15
	- ## Elementary Concepts of Logic \#2

## Possible Worlds

### Definition

- Many concepts of logic are easier to understand in terms of **possible worlds**.
	- Total universes (or multiverses).
	- The actual world is one among the many possible worlds.
	- Every *possible* way things could have been.
- “Metaphysically” possible worlds: 
	- a very general form of possibility
		- might be incompatible with our knowledge in the actual world 
			- (and so allow for things that are “epistemically impossible”)
		- might have different laws of physics 
			- (and so allow for things that are physically impossible)
- There are **no metaphysically possible worlds** where logical or mathematical falsehoods are true. 
	- (A ∧ ¬ A; 1 + 1 = 45) 
		- They are *necessarily false*.

> [!NOTE] Lecture
> Something happened in this world, but in another possible world, it didn't.
> There is another possible world where the laws of physics are different.
> Could *have* been late, but incompatible with observation.
> Ruling out the possibility of worlds where (mathematically/logically) truths are false.

### In Action

- **Modal** notions—necessity, possibility, contingency, etc.—are often understood in terms of *possible worlds*.
- ***Necessity*** Definition:
	- A proposition is **necessary** (or necessarily true) iff it’s true in every possible world.
- ***Possibility*** Definition
	- A proposition is **possible** iff it’s true in least one possible world.
- (Different kinds of possibility and necessity: 
	- metaphysical, epistemic, physical/nomological, etc.)
- ***Contingency*** Definition:
	- A proposition is contingent iff it’s true in some possible worlds and false in others.

### Applications

- ***Joint possibility*** Definition:
	- A set of sentences is **jointly possible** iff there’s some possible world where all of the sentences are true.
		- Can you infer how to define, in possible worlds terms, **joint impossibility** 
			- (aka logical incompatibility)?
				- *There are **no possible worlds** in which all the sentences are true.*
- ***Necessary equivalence*** Definition:
	- Two sentences are **necessarily equivalent** iff they have the same truth values as each other at every possible world.
- ***Validity (PW)*** Definition
	- An argument is valid iff there are *no possible worlds* where all of its premises are true and its conclusion is false.

## Validity

- In most cases, an arguments premises are **jointly possible** and its conclusion is **contingent**.
	- But there are special cases where an argument’s premises are jointly impossible. 
	- In these cases, the argument is automatically valid—no matter what its conclusion says!
		1. A
		2. ¬ A
		3. ∴ B
	- There are no possible worlds where the premises are all true.
		- So there are no possible worlds where the premises are all true and the conclusion is false. 
			- (Def. of valid.)
				- No possible worlds where all the premises are true.
				- Thus: can't be true *and* the conclusion false.
- Slogan:
	- Everything follows from a contradiction.

### Valid Arguments

#### Example 1

1. Yuri is a painter.
2. Yuri is not a painter.
3. ∴ Therefore, bumblebees are fluffy.
	- **Valid**.

- In general:
	1. ⊥
	2. ∴ A

#### Example 2

1. Either we have eggplants or we have broccoli.
2. We don’t have eggplants.
3. We don’t have broccoli.
4. ∴ Therefore, the next pope will be Justin Bieber.
	- **Valid**.

> [!NOTE] Lecture
> Jointly impossible premises, so any conclusion is true.
> **`⊥`** == contradiction.

### Intuition

#### Intuitive interpretation
- Students often find this idea unintuitive.
- Consider the following idioms:
	- “If what you say is true, then I’ll be a monkey’s uncle.”
	- “I’ll do what you ask when pigs fly”
	- (or “. . . when hell freezes over.”)
- **General idea**: 
	- if we’re going to accept something impossible/ridiculous, then we might as well accept any other impossible ridiculous thing.
- These idioms are called “*adynata*”. 
	- Examples from other languages: 
		- Malay: 
			- *when cats grow horns;* 
		- Turkish: 
			- *when fish climb poplar trees;* 
		- Russian: 
			- *when the crawfish whistles on the mountain.*

## Connectives and Symbolization

### Atomic Sentences

- **Atomic sentences** are sentences that contain no subsentences.
- In the artificial language we are using, TFL, we symbolize atomic sentences with letters: 
	- *A, B, C*,...
- In cases where we might need more than 26 distinct sentences, we can also use subscripts: 
	- *A<sub>1</sub>, A<sub>2</sub>,...A<sub>285</sub>,...*
- The artificial language that we'll be using has, as its basic vocabulary, **atomic sentences** and **connectives**.

### Truth-Functional Connectives

- The connectives conventionally used in truth-functional logic:

| symbol we'll use | you might also see | name          | rough meaning               |
| ---------------- | ------------------ | ------------- | --------------------------- |
| ¬                | ~                  | negation      | 'It's not the case that...' |
| ∧                | &, ·               | conjunction   | '...and...'                 |
| ∨                | \|                 | disjunction   | '...or...'                  |
| →                | ⊃, >               | conditional   | 'If..., then...'            |
| ↔                | ≡                  | biconditional | '...if and only if...'      |

### Connectives

- Connectives are pieces of language that can be used to make new sentences out of other sentences.
	- *P: Paulina is at the party*
	- *Q: Quinton is at the party*
- Simpler sentences can be combined into more complex sentences:
	- (P ∧ Q)
	- ¬P ∨ (P → Q)
	- (P ∧ Q) ∨ (¬P ∧ ¬Q)
	- etc.
- From finite sentences, infinitely many sentences.
### Negation

- The sentence 'It's not the case that dogs are made of paper' contains an atomic subsentence:
	- *D: dogs are made of paper*
- The **negation** of 'D' is '¬D': 
	- *'It's not the case that dogs are made of paper'*
		- A negation is true iff the sentence it negates is false.
		- Negation is a **one-place connective**: it takes one sentence as input and generates another sentence as output.
		- All four other connectives in TFL are **two-place connectives**:
			- they take two sentences as input and generate another sentence as output.

### Conjunction

- *A*: Avital is hungry
- *B*: Ben is hungry
- The **conjunction** of '*A*' with '*B*' is written '(*A* ∧ *B*)':
	- 'Avital is hungry and Ben is hungry'.
- The **conjuncts** of '(*A* ∧ *B*)' are the subsentences that are conjoined:
	- '*A*', '*B*'
- Notes:
	- A conjunction is true if and only if both of its conjuncts are true.
	- Conjunctions are symmetric: 
		- '(*A* ∧ *B*)' is necessarily equivalent to '(B ∧ A)'
	- '∧' can be used to symbolize 'and', 'but', 'although',...

### Disjunction

- A **disjunction** consists of two sentences linked by 'or':
	- (*A* ∨ *B*): Avital is hungry or Ben is hungry.
- The two sentences are called the **disjuncts**.
	- A disjunction is true if and only if **at least one** of its disjuncts is true.

#### Example

- NB. Sometimes in ordinary language, when we use 'or', we implicitly suggest that exactly one of the disjuncts is true, not both. 
	- (‘Nan is in Prague or she’s in Stuttgart.’)
		- That logical connective is called *exclusive 'or'*
- In TFL, 'or' and '∨' are always used to mean the *inclusive* 'or', not the exclusive 'or'.
- '*A* ∨ *B*' always means at least one, and possibly both, of the disjuncts *A* and *B* is true.
	- (Exclusive 'or' can easily be defined out of other truth-functional operators.)
- Comic:
	- "Either someone's smoking pot or it's a skunk"
		- (Showing a skunk smoking pot)
- Comprehension: 
	- *M*: UCSD is in California
	- *W*: UCSD is in San Diego
	- Is the following sentence true or false?
		- (*M* ∨ *W*)
			- True
### Conditionals

#### Conditional

- A sentence can be symbolized as *A* → *B* if it can be paraphrased in English as:
	- 'If A, then B'
	- or 'A only if B'
	- or 'B if A'.
- These sentences are **conditionals**.
- In '*A* → *B*', '*A*' is the **antecedent** (the if-clause) and '*B*' is the **consequent**.
	- N.B. Conditionals in TFL are a **severe simplification** of natural language conditionals.
	- TFL conditionals (often called 'material conditionals') do not require any connection whatsoever between the subject matter of the antecedent and the consequent.
	- '*A* → *B*' only claims that *A* and ¬*B* aren't both true.
	- Note also that, unlike conjunction and disjunction, conditionals are **not symmetric**!

#### Biconditional

- *D*: I'll give you ten dollars.
- *B*: You bring me a burrito.
- (*D* ↔ *B*): I'll give you ten dollars if and only if you bring me a burrito.
- Sentences of this form are **biconditionals**.
	- Biconditional links a lefthand side and a righthand side.
		- **A biconditional tells us that either the lefthand and righthand sides are both true, or they're both false.**
		- Again, there need be no connection between the subject matters of the lefthand and righthand sides!

#### Symbolization Exercises

1. 'If you bring me a burrito, I'll give you ten dollars.'
	- (*B* → *D*)
2. Exercise 2:
	- *A*: Avital is hungry
	- *B*: Ben is hungry.
	- 'Neither Avital nor Ben is hungry.'
		- ¬(*A* ∨ *B*)

## Recap

### Content

#### Part 1

- A pair of sentences are **necessarily equivalent** iﬀ they have the same truth value in every possible world.
- A sentence is **contingent** iﬀ it’s true in some possible worlds and false in other worlds.
- **Comprehension quizlet**: 
	- If two sentences are necessarily equivalent, can each sentence be contingent?
		- A. yes
		- B. no
	- If two sentences are necessarily equivalent, can each sentence be non-contingent (necessarily true or necessarily false)?
#### Part 2

- Two sentences are **jointly possible** if there’s some possible world in which both are true.
- **Comprehension quizlet**: 
	- If two sentences are necessarily equivalent and each sentence is contingent, are the two sentences jointly possible?
		- A. yes
		- B. no

### Validity

- An argument is **valid** if and only if it's impossible for all of its premises to be true and its conclusion false.
	- Argument I:
		1. Michael is wearing blue.
		2. Michael is not wearing blue.
		3. ∴ It's foggy today.
			- A. **Valid**
	- Argument II:
		1. Marijuana should be illegal.
		2. Alcohol is protected by religious freedoms.
		3. ∴ Marijuana should be illegal.
			- A. **Valid**
	- Argument III:
		1. Bo is a dog.
		2. Barack Obama likes Bo.
		3. Michelle Obama likes Bo.
		4. ∴ Bo is a good dog.
			- B. **not valid**



---

Previous: [PHIL 10 Lecture 2](PHIL_10_LE_2.md).
Next: [PHIL 10 Lecture 4](PHIL_10_LE_4.md).