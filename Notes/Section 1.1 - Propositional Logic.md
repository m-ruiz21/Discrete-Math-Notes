## Main Concepts
- [[#Propositions]]
- [[#Logical Operators]]
- [[#Truth Tables]]
- [[#Conditional Statements (if then)]]
- [[#Biconditional Statements (if and only if)]]
## Introduction
Propositional logic is the foundation of logical reasoning, and it allows us to precisely describe our mathematical reasoning. For this reason, it's a foundational concept of the class. 

## Propositions

**TLDR: a proposition is a logical statement that is either true or false**

The book defines a propositions as follows:

> A proposition is a declarative sentence (that is, a sentence that declares a fact) that is either true or false, but not both.

So for example: 
1. Mateo is the best TA (true)
2. New York City is the capital of New York (false)
3. If it rains, then outside will be wet. (true and totally foreshadowing the notes here)

It's a pretty easy concept you should be able to get ahold of quickly.

## Logical Operators

**TLDR: Logical operators are made up of AND, OR, XOR, NOT, IFF (if and only if), and IMPLIES (will cover the last two later on). They are the basic foundation of a logical proposition and they mean exactly what you think they mean.**

Logical operators what we use to string together propositions to create larger and more complex propositions. If you have done programming before, this should be a concept you're familiar with. 

Here's the core four you need to know:

| Operator | Symbol | Meaning |
| -------- | ------- | ------- |
| AND | $\land$ | True if both sides are True |
| XOR | $\oplus$ | True if both sides are different (True-False / False-True) |
| OR | $\vee$ | True as long as only one of the sides are True | 
| NOT | $\neg$ | Only operator that only takes one argument. It only flips the truth value (True -> False / False -> True) |

There's two more: IIF (if and only if) and IMPLIES, but those will be covered after truth tables.

## Truth Tables

**TLDR: We can use truth tables to represent the different possible inputs / outputs of our logical proposition.** 

Ditto to what the TLDR said. You can create a truth table by first writing down all of the possible inputs to your proposition followed by the results of your proposition given those inputs. 

For example, the truth table of the proposition $p \land q$ is:

| $p$ | $q$ | $p \land q$ |
| - | - | - |
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

> Note: I am going to start using 0's and 1's because I'm a computer engineer and it's quicker / what I'm most used to, but in case you're not familiar, 0 = false and 1 = true.

So you might notice two things when creating a truth table:
- The amount of rows is equal to the number of variables squared (you trust your intuition here, I promise it's true). 
- You can always make sure to cover all of the possibilities by making the first variable alternate 0's and 1's every (rows / 2) rows, then make the second variable alternate 0's and 1's every (rows / 4) rows, etc.
	-  For example, when you have three variables, we'll have 8 total rows. The first variable would alternate 0's and 1's every 4 rows, the second variable would alternate 0's and 1's every 2 rows, and the third variable would alternate every single row.

> Hint: you should be using the above facts to help you make sure your truth table makes up every possible input / output ! 

This is going to be a useful tool for us to understand the meaning of our propositions and find logical equivalencies (more on this later).

## Conditional Statements (if then)

**TLDR: Conditional statements (if then or inferring) allow us to link conditions to outcomes.**

A Conditional Statement (otherwise known as inferencing) is a logical operator that allows us to represent the idea of "if x then y". 
Naturally, this means it is made up by two parts: a cause (or a premise / hypothesis) and an effect (or consequence / conclusion).

It is represented by the symbol $\rightarrow$ and is represented by the following truth table:

| $p$ | $q$ | $p \rightarrow q$ |
| - | - | - |
| 0 | 0 | 1 |
| 0 | 1 | 1 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

You can think of an implication as a contract between both variables $p$ and $q$ where the contract is "if $p$ is true then $q$ must also be true".

Note that the contract does not say anything about what happens if $q$ is true.
That's because **the causality only goes one way**. 
If $q$ is true and $p$ is false, that doesn't make our statement false since our contract never mentions any direct effect of $q$ being true.  
In other words, $p$ can force $q$ to be true, but not the other way around.

Implication is a one way road (hence the singular direction of the arrow), so I can logically get to B from A, but I can't get to A from B. 

>For example, I can positively say that "If mark flips on that light switch, then the light will turn on". 
>However, just because the light is turned on doesn't mean that mark was the one that flipped on the light switch. It could have been Rebecca, Alex, John, etc. 
>The logical "cause / effect" connection only goes in one direction.

### Converse, Contrapositive, and Inverse
In particular, there are three related conditional statements that occur so often that they have special names : converse, contrapositive, and inverse.

Here's the four relations based on $p \rightarrow q$ 

| Name | Relationship |
| - | -| 
| Converse |  $q \rightarrow p$ |
| Contrapositive |  $\neg q \rightarrow \neg p$ |
| Inverse | $\neg p \rightarrow \neg q$ |

## Biconditional Statements (if and only if)

**TLDR: Biconditional statements (IFF / if and only if) is a conditional statement that goes both ways.**

A Biconditional statements is a logical operator that allows us to represent the idea (x if and only if y) only evaluates to true when both sides are true / false.  
You can think of it as a two way conditional statement. 

It is represented by the symbol $\leftrightarrow$ and has the following truth table:

| $p$ | $q$ | $p \leftrightarrow q$ |
| - | - | - |
| 0 | 0 | 1 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |