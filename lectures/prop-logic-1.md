---
title: Propositional logic 1
subtitle: Defining the language
author:
  name: Erik Hoversten
  affiliation: Rutgers University
course: LRP, fall 2014
date: October, 22, 2014
---

# A formal logic is defined by its language

The key parts of any language are:

> - Vocabulary
    - Logical vocabulary
    - Non-logical vocabulary
> - Syntax
    - Rules for putting vocabulary together into propositions
> - Semantics
    - Rules for interpreting the meaning of propositions

## Categorical logic

In categorical logc, our language was:

> - Vocabulary
    - Logical: Quantifiers and copula
    - Non-logical: Subject and predicate terms
> - Syntax
    - [Quantifier]+[Subject term]+[copula]+[Predicate term]
> - Semantics
    - Specification of each proposition's meaning in terms of set *inclusion* and *exclusion*

## Propositional logic

Propositional logic is another formal logic with a slightly different language:

> - Vocabulary
    - Logical: Connectives
    - Non-logical: Propositions
> - Syntax
    - [1-place connective]+[proposition]
    - [proposition]+[2-place connective]+[propostition]
> - Semantics
    - Specification of each proposition's meaning in terms of its **truth conditions**

# Propositional logic

We define the formal logic by specifying completely each component of the language used to express the logic

## Vocabulary

The words of propositional logic

> * Logical
    + 1-place connective: takes 1 proposition and makes a compound proposition
        - **\~** : *not*, *it is not the case that*
    + 2-place connective: take 2 propositions an make a compound proposition
        - **&2219**: *and*, *in addition*, *both...and___*
        - **&2228**: *or*, *either...or___*
        - **&2283**: *if...then___*, *...only if___*, *...unless___*
    + Parentheses: **\(** and **\)**
> * Non-logical
    + Atomic propositions: *John went to the store*, *Mary ate baked tofu*
    + We abstract over the content of propositions by replacing them with propositional variables: *A, B, C, ...*

## Syntax

The sentences of propositional logic

> - [proposition]
    - **A**, **B**, **C**, ...
> - [1-place connective]+[proposition]
    - **\~A**
> - [proposition]+[2-place connective]+[proposition]
    - **A &2219 B**
    - **C &2228 D**
    - **E &2283 F**

## Formulas

A *formula* is any combination of bits from the vocabulary of the language. But not all possible formulas belong to the language of propositional logic.  The good ones must follow the syntax on the previous slide.

> - WFFs
    - Any syntactic unit that meets the specification above is a **well-formed formula** (*WFF*)
    - The WFFs compose the entire language of propositional logic
    - Propositional variables can stand for *any* WFF, either atomic or compound
> - Recursion
    - Compound propositions are also propositions, so we can use connectives to connect compound propositions as well as atomic ones. 
    - When we do, we surround each compound proposition with parentheses
    - This is known as **recursion*
    - ex: *(A &2219 B) &2283 (C &2228 D)*, *(\~M &2283 Q) &2219 R* 


## Semantics

In propositional logic, we specify the meaning of WFFs in terms their **truth conditions**.

Truth conditions specify the **way the world must be** in order for the proposition to be true.

+ Another way to say this is: What a proposition *means* is the situations in which it is true.

Examples:

> + *Jack went to the store* is true **just in case** Jack went to the store.
> + *Felicity got a perm and Mike likes it* is true **just in case** *both* Felicity got a perm *and* Mike likes Felicity's perm
> + *Garth is at the party or he had a fight with Wayne* is true **just in case** *either* Garth is at the party *or* Garth had a fight with Wayne

# Truth tables

In order to provide the meaning for a WFF, we need to outline the different *ways* it can be true or false. We do this by constructing a **truth table** for the WFF.

Atomic propositions can only be either true or false, so their truth table is pretty boring.
- We put a *T* to stand for true and an *F* to stand for false

Table: Truth table for atomic propositions

  A
-----
  T
  F

Notice that we list **one row** for each *distinct* way that the WFF might turn out. For atomic propositions, there are two distinct ways, thus two rows appear on the table.

## Truth tables for compound propositions

Compound propositions have more *moving parts* than atomic ones, so their truth tables are more interesting.

To construct a truth table for a compound proposition we:

1. Make a *column* for every distinct propositional variable in the WFF
2. Add a column for the complete WFF
2. Make a *row* for every distinct combination of truth values those variables can have
    - As a rule, if there are *n* propositional variables in the WFF, there will be *2^n^* combinations of truth values
    - If the WFF includes an *A* and a *B*, there will be **2^2^ = 4** rows in the table
    - If the WFF includes a *C*, a *D*, and an *E*, there will be **2^3^ = 8** rows in the table
3. To fill the columns:
    - Divide the number of rows in half. In the first column, fill the first have rows with *T*s, and the second half rows with *F*s
    - Divide the rows in half again. In the second column, fill the first quarter rows with *T*s, the second quarter with *F*s, and continue on, laternativng every quarter.
    - Continue this process until the column for your last propositional variable has alternating *T*s and *F*s all the way down.





