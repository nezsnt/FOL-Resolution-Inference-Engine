# FOL Resolution Inference Engine

A First Order Logic (FOL) inference engine implemented in Python using **Resolution by Refutation** and **Unification** techniques.

This project was developed as san academic implementation of classical symbolic Artificial Intelligence concepts, allowing automatic theorem proving from a user-defined knowledge base.

---

## Overview

The system allows users to define facts and rules in First Order Logic and automatically determine whether a query can be logically inferred from the knowledge base.

The inference process is based on:

- Knowledge Representation
- First Order Predicate Logic
- Unification
- Resolution by Refutation
- Automated Theorem Proving

---

## Features

- Knowledge Base representation in First Order Logic (FOL)
- Support for facts, implications and disjunctions
- Simplified transformation of rules into Conjunctive Normal Form (CNF)
- Query negation for proof by contradiction
- Unification algorithm for variable substitution
- Resolution by Refutation inference engine
- Automatic theorem proving
- Interactive console interface

---

## Project Structure

```text
FOL-Resolution-Inference-Engine/
│
├── src/
│   └── motor_inferencia.py
│
├── examples/
│   └── example_criminal_west.txt
└── README.md
```

---

## How It Works

The inference process follows these steps:

1. The user enters a Knowledge Base in First Order Logic.
2. Rules are transformed into a clause form suitable for resolution.
3. The query is negated.
4. Unification is applied to match variables and constants.
5. Resolution by Refutation is executed.
6. If the empty clause is generated, a contradiction is found and the theorem is proven.

### Inference Pipeline

```text
First Order Logic
        ↓
Clause Transformation
        ↓
Negated Query
        ↓
Unification
        ↓
Resolution by Refutation
        ↓
Empty Clause ?
        ↓
Theorem Proven
```

---

## Supported Syntax

### Facts

```text
Missile(M1)
Owns(Nono,M1)
Enemy(America,Nono)
```

### Implications

```text
Missile(x) & Owns(Nono,x) => Sells(West,x,Nono)
```

```text
Sells(West,x,Nono) & Enemy(America,Nono)
=> Criminal(West)
```

### Disjunctions

```text
Roman(x) | Greek(x)
```

---

## Example

### Knowledge Base

```text
Missile(M1)

Owns(Nono,M1)

Missile(x) & Owns(Nono,x)
=> Sells(West,x,Nono)

Sells(West,x,Nono)
=> Criminal(West)
```

### Query

```text
Criminal(West)
```

### Result

```text
CONTRADICTION REACHED (Empty clause generated)
THE THEOREM IS TRUE
```

---

## Artificial Intelligence Concepts

This project implements several classical AI concepts:

- Knowledge Representation
- First Order Predicate Logic
- Automated Reasoning
- Symbolic Artificial Intelligence
- Unification Algorithm
- Resolution Principle
- Theorem Proving

---

## Unification

The inference engine uses a unification algorithm to determine substitutions that make two literals compatible.

Example:

```text
Human(x)
Human(Socrates)
```

Substitution obtained:

```text
{x → Socrates}
```

This substitution allows the resolution process to continue and derive new clauses.

---

## Resolution by Refutation

The theorem proving strategy used is Resolution by Refutation.

Instead of directly proving a query, the system:

1. Negates the query.
2. Adds it to the knowledge base.
3. Applies resolution repeatedly.
4. Attempts to derive the empty clause.

If the empty clause is generated, a contradiction has been found, proving that the original query logically follows from the knowledge base.

---

## CNF Support

The current implementation supports a simplified clause transformation for Horn-like clauses and implications commonly used in academic examples.

For example:

```text
A(x) & B(x) => C(x)
```

is transformed into:

```text
~A(x) v ~B(x) v C(x)
```

This transformation is sufficient for many educational examples involving resolution and theorem proving.

---

## Current Limitations

This project was developed for academic purposes and does not implement the full First Order Logic resolution pipeline.

The current version does **not** include:

- Full CNF conversion for arbitrary FOL expressions
- Explicit quantifier handling
- Variable standardization apart
- Skolemization
- Occurs Check in unification
- Tautology elimination
- Subsumption optimization

Because of these limitations, the engine should be considered an educational implementation rather than a complete automated theorem prover.

---

## Technologies

- Python
- Object-Oriented Programming (OOP)
- First Order Logic (FOL)
- Resolution by Refutation
- Unification Algorithm
- Symbolic Artificial Intelligence


## Future Improvements

Potential future enhancements include:

- Complete FOL to CNF transformation
- Quantifier support
- Skolemization
- Variable standardization
- Occurs Check implementation
- Graphical user interface
- Knowledge base file loading
- Resolution tree visualization
- Performance optimizations


## Authors

- Santiago Ibañez
- Sophie Mejía
- Joel Martinez
- Esteban Blanco

