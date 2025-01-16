---
course: PHIL 10
type: lecture
lecture_num: "2"
date: 1/10
---

# PHIL 10 Lecture 2
- ## 1/10
	- ## Elementary Concepts of Logic

## Arguments and Validity

### Arguments
- An **argument** is any series of premises together with a conclusion.
	- Example:
		1. Wally is a wombat
		2. Therefore, Wally is a marsupial.
	- Example:
		1. I'm hungry.
		2. I'm in a position of power.
		3. ∴ Therefore, one of you should bring me a burrito.
- There are good arguments and bad arguments.

#### Evaluating Arguments

- Ways of evaluating an argument:
	- plausibility of premises
	- degree to which the premises make the conclusion likely
	- substantiveness/vacuity of conclusion
	- substantiveness/vacuity of the inference
	- desirability of the conclusion
	- authority of the speaker
	- civility/insultingness of the presentation
	- . . .

### Validity

- The concern of logic: 
	- evaluating **deductive** arguments: 
		- arguments where the premises are intended to prove the conclusion.
- Our criterion of evaluation for arguments: 
	- validity.
- In other words, we are concerned with:
	- whether the premises entail the conclusion
	- whether the conclusion follows from the premises
#### Official Definition

- An argument is **valid** if and only if it is impossible for all of its premises to be true and its conclusion false.
- In other words: an argument is valid if and only if, in any possible circumstances where all of its premises are true, its conclusion must also be true.
- An argument can be valid even if...
	- some or all of its premises are false.
	- its conclusion is false.

##### Examples

- Argument 1:
	1. It's sunny.
	2. It's cold.
	3. ∴ It's sunny and it's cold.
		- **Valid**
- Argument 2:
	1. If Hanti was well, then he came to class.
	2. Hanti came to class.
	3. ∴ Hanti was well.
		- **Invalid**

### Atomic Sentences

- Logically complex sentences are composed out of logically simpler sentences.
	- If Alex went to the party, then Bob stayed home.
- The simplest sentences do not contain any subsentences.
	- These are atomic sentences.
- In this class, these will generally be symbolized with individual capital letters:
	- A: Alex went to the party.
	- B: Bob stayed home.
- This exposes the logical structure of a complex sentence:
	- If *A*, then *B*.

#### Validity in Truth-Functional Logic

- The form of logic we’ll be learning in this course is **truth-functional logic** (TFL).
	- Also known as propositional logic, sentential logic, or zeroth-order logic.
- TFL can help us identify whether an argument is valid in virtue of its sentences’ form or structure.
##### Example

| Argument                                                                                                              | Logical Form                                        |
| --------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------- |
| 1. If Alex went to the party, then Bob stayed home.<br>2. Alex went to the party.<br>3. ∴ Therefore, Bob stayed home. | 1. If A, then B.  <br>2. A.  <br>3. ∴ Therefore, B. |

## Necessity and Contingency

- Most everyday sentences are **contingent**: 
	- true in some possible circumstances and false in other possible circumstances.
		- The cat is sleeping.
		- The first midterm is in less than two weeks.
- Some individual sentences are **necessary truths**: 
	- they cannot possibly be false.
		- If it’s raining, then it’s raining.
		- Either it’s Wednesday or it’s not Wednesday.
- Some individual sentences are **necessary falsehoods**: 
	- they cannot possibly be true.
		- (They are self-contradictory.)
			- Jeff Goldblum is from Ohio and Jeff Goldblum isn’t from Ohio.
### Other Terms
#### Joint Possibility
##### Definition
- Sentences are jointly possible if and only if it is possible for them all to be true together.
- Other terminology:
	- Jointly possible sentences are consistent with each other.
	- There is some possible scenario where all are true.
#### Joint Impossibility
##### Definition
- Sentences are **jointly impossible** if and only if it is impossible for both to be true together. 
	- At least one must be false.
- Other terminology:
	- Jointly impossible sentences are **inconsistent** or **incompatible** with each other.
		- There is no possible scenario where all are true.
#### Necessary Equivalence
##### Definition
- Two sentences are **necessarily equivalent** if they must have the same truth value.
	- In other words, in any possible scenario, either both are true or both are false.
		- Ann is older than Bob.
		- Bob is younger than Ann.
- If you know the truth value of one, you know the truth value of the other.

## Practice

### Comprehension
- If two sentences are necessarily equivalent, can each sentence be contingent?
	- A. **yes**
	- B. no
- If two sentences are necessarily equivalent and each sentence is contingent, are the two sentences jointly possible?
	- A. **yes**
	- B. no
### Validity exercises
- Argument I
	1. Either all dogs are male or Bo Obama is female.
	2. Not all dogs are male.
	3. ∴ Bo Obama is female.
		- A. **valid** 
		- B. not valid
- Argument II
	1. Marijuana should be illegal.
	2. Alcohol is protected by religious freedoms.
	3. ∴ Marijuana should be illegal.
		- A. **valid** 
		- B. not valid

## Validity and Contradictions
### Contradictions

- ***Contradiction*** Definition:
	- A **contradiction** is any well-formed sentence that cannot possibly be true.
		- Examples:
			- ‘A ∧ ¬ A’; ‘¬( P → P) 
- ***Joint Impossibility*** Definition:
	- Sentences P*1*, . . . , P*n* are jointly impossible just in case it’s impossible for all to be true together.
		- If some sentences are jointly impossible, does that mean that each of the sentences is necessarily false?
			- No?
### Validity

- **Validity** Definition:
	- An argument is **valid** if and only if it’s impossible for the premises to all be true while the conclusion is false.
- Suppose you’re evaluating the following argument:
	1. A ∧ ¬ A
	2. ∴ B ∧ C
		- Is this a valid argument? 
			- (Is the conclusion a logical consequence of the premises?)
				- Surprisingly: **yes**!
- **General fact**: 
	- If it’s impossible that *P*, then it’s impossible that *P* **and** \[whatever\].
	- It’s **impossible** for premise 1 (a **contradiction**) to be true.
	- So it’s impossible for premise 1 to be true **and** the conclusion false.
	- So the argument is valid. 

---
Previous: [PHIL 10 Lecture 1](PHIL_10_LE_1.md)
Next: [PHIL 10 Lecture 3](PHIL_10_LE_3.md)
