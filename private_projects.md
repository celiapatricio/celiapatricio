## 🔒 Private Projects

[🔙 Back to general overview](README.md)

### [2024] AJS Compiler

This project implements a complete compiler for the AlmostJavaScript (AJS) language. AJS is an imperative, weakly typed language inspired by JavaScript, supporting basic types, objects, control structures, and user-defined functions.

Implemented features:

- Lexical analysis with `ply.lex`:
  - Token recognition: numbers in multiple bases (decimal, binary, octal, hexadecimal), floating point, characters, booleans, `null`, and reserved keywords.
  - Proper handling of comments (`//` and `/* */`).

- Syntax analysis with `ply.yacc`:
  - BNF-style grammar defining declarations, expressions, assignments, objects, functions, and control structures.
  - Rules are organized hierarchically to avoid ambiguities.

- Semantic analysis:
  - Symbol table with inferred types for variables.
  - Record table for objects and their properties.
  - Type checking and conversions (e.g., char → int, int → float).
  - Function validation: parameter count, types, and return value.

[*AJS Compiler Repository*](https://github.com/NathaliaMoniz/P2-Practica-Final-PDL.git)


### [2024] Lexical and Syntax Analyzer for AJSON

This project consists of building a lexical and syntax analyzer for a JSON-like language called AJSON using Python’s `PLY` library. The goal is to parse and display the structure of extended JSON files, and perform evaluations on values and comparisons.

- Lexer (`ajson_lexer.py`)
  - Recognizes:
    - Numeric types: integers, reals, scientific notation, binary, octal, and hexadecimal
    - Strings (quoted and unquoted)
    - Operators (`<`, `>`, `==`, `<=`, `>=`)
    - Keywords (`null`, `true`, `false`)
    - Syntax structure: `{`, `}`, `:`, `,`

- Parser (`ajson_parser.py`)
  - Supports:
    - Evaluation of values and comparisons
    - Interpretation of nested structures
    - Merging dictionaries as output
    - Structured printing of the nested tree

[*AJSON Analyzer Repository*](https://github.com/NathaliaMoniz/P1-Introduccion-PDL.git)


### [2023] Constraint Satisfaction and Heuristic Search

This project is composed of two parts, each addressing a problem through constraint satisfaction and heuristic search techniques.

1. *[Nov 2023]* Constraint Satisfaction: Ambulance parking assignment.

   Assign ambulances (some with special needs like power connection or maneuverability) to parking spots while respecting a set of constraints.

   - Modeled as a CSP:
     - Variables: ambulances
     - Domains: available spots (with/without power supply)
     - Constraints:
       - One ambulance per spot
       - No two ambulances can share a spot
       - Freezer ambulances require power
       - TSU ambulances must have free spots nearby
       - TNU ambulances cannot block TSUs
   - Implemented in Python with `python-constraint`
   - Evaluated under multiple scenarios:
     - Solvable vs. unsolvable cases
     - Performance improved from 15 to ~5 minutes on large instances

2. *[Dec 2023]* Heuristic Search: Patient transport with A*.

   Transport patients (contagious and non-contagious) to medical centers minimizing energy cost using A*.

   - Model elements:
     - State: ambulance position, seat occupancy, pending pickups
     - Operators: move, pick up, drop off patients
     - Constraints:
       - Ambulance: 10 seats (2 for contagious)
       - Contagious patients must be dropped off before others
       - Limited energy (50 units)
     - Heuristic: Manhattan distance to base

[*Constraint Satisfaction & Heuristic Search Repository*](https://github.com/celiapatricio/p2-471979-471948.git)


### [2023] Pixar Bites Website

A responsive, interactive web app for a fictional restaurant called *Pixar Bites*. Educational goal: apply web design, UX, accessibility, and modular HTML/CSS/JS structure.

Features:

- Main page (`index.html`):
  - Responsive layout with hamburger navigation
  - Internal sections:
    - Our Story
    - Our Venue
    - Our Kitchen (carousel of Pixar-inspired dishes)
  - Interactive gallery and custom styles (Google Fonts)

- Online reservation (`reserva.html`)

- Login and ordering (`inicio_sesion.html`, `pedido.html`)

- Reviews (`resenas.html`)

- Themed mini-game (`juego.html`)

- Contact form (`contacto.html`)

- Dynamic promotions (`promociones.html`)

[*Pixar Bites Web Repository*](https://github.com/Nachofc333/ProyectoInterfaces.git)


### [2023] Linear Programming: Optimal Call Center Planning

Two optimization problems regarding call assignment to locations, minimizing total response time or cost. Solved with mixed integer linear programming.

1. *[Oct 2023]* Assignment with 3 existing locations

   Assign calls from districts D1–D5 to L1–L3, minimizing response time.

   - Key constraints:
     - Max calls per location
     - Max allowed response times
     - Balanced workload

   - Results:
     - Minimum total time: 483800
     - Efficient distribution among L1, L2, and L3
     - All constraints met; solution is optimal

2. *[Oct 2023]* Expansion with new locations (L4, L5, L6)

   Reformulated to include decisions on opening new sites (build or not) and assignment.

   - Additional constraints:
     - Construction cost per site
     - Minimum district coverage
     - Binary variables for build/assign

   - Results:
     - Minimum total cost: 866700
     - Build L4 and L5, skip L6
     - All constraints met

[*Linear Programming Project Repository*](https://github.com/celiapatricio/p1-471979-471948.git)


### [2023] Optimal Thermostat Control with Dynamic Programming

Simulates thermostat behavior using dynamic programming to reach a target state (22.0°C) with minimal energy cost.

Main features:

- Reads transition data from CSV files (`t1.csv`, `t2.csv`)
- Computes optimal policy using Bellman equations
- Step-by-step simulation with user input (time and state)

[*Thermostat MDP Repository*](https://github.com/celiapatricio/practica_termostato.git)


### [2023] Software Development Project

A set of exercises covering essential software development topics, both technical and ethical.

1. *[Jan 2023]* Ethics and Legal Aspects

   Ana, a software engineer, faces a dilemma. This case study encourages critical thinking based on the CCII Code of Ethics.

2. *[Feb 2023]* Code Style and Best Practices

   Defines and applies Python style rules (PEP8) using `pylint`.

   [*Code Style Repo*](https://github.com/celiapatricio/G80.2023.T10.EG2.git)

3. *[Mar 2023]* Test-Driven Development

   Implements order management features using TDD:

   - Request order: validate inputs and generate ID
   - Ship product: validate JSON and hash
   - Deliver product: validate tracking and create file

   [*TDD Repo*](https://github.com/100471979/G80.2023.T10.EG3.git)

4. *[Apr 2023]* Refactoring and Simple Design

   Refactors code from EG3:

   - Removes code smells (long functions, duplication, poor names)
   - Applies Singleton pattern
   - Adapts to PEP8 with `pylint`
   - Tracks changes via GitHub commits and XML tests

   [*Refactoring & Design Repository*](https://github.com/100471979/G80.2023.T10.EG4.git)
