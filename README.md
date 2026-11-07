# Mastery-Based C Programming Curriculum

A project-first curriculum for a technical professional. It assumes general
computer literacy, but no prior C experience. Use a current C compiler (such as
GCC or Clang) and a text editor or IDE. Compile examples with warnings enabled
(for example, `-Wall -Wextra -Wpedantic`) and keep each project in version
control.

## How to use this curriculum

The curriculum has eight learning modules and an integrated capstone: **100
estimated hours** in total. Each module allocates its time as **20% theory, 40%
hands-on practice, and 40% real-world project work**. Module estimates are
planning targets; mastery, not elapsed time, determines when you move on.

Complete modules in order. At each gate, demonstrate every mastery criterion
before starting the next module. If a criterion is not met, review the relevant
concepts, revise the work, and retest it. Keep code, test results, and short
design notes as evidence of mastery.

| Module | Focus | Theory | Hands-on practice | Project work | Total |
| --- | --- | ---: | ---: | ---: | ---: |
| 1 | C setup, types, and input/output | 2 h | 4 h | 4 h | 10 h |
| 2 | Decisions and repetition | 2 h | 4 h | 4 h | 10 h |
| 3 | Functions and program structure | 2 h | 4 h | 4 h | 10 h |
| 4 | Arrays, strings, and pointers | 2 h | 4 h | 4 h | 10 h |
| 5 | Data modeling and files | 2 h | 4 h | 4 h | 10 h |
| 6 | Dynamic memory and data structures | 2 h | 4 h | 4 h | 10 h |
| 7 | Errors, testing, and safe C | 2 h | 4 h | 4 h | 10 h |
| 8 | Build, debug, and integrate | 2 h | 4 h | 4 h | 10 h |
| 9 | Capstone: workplace delivery | 4 h | 8 h | 8 h | 20 h |
| **Total** |  | **20 h** | **40 h** | **40 h** | **100 h** |

## Module 1 — C setup, types, and input/output (10 hours)

- **Learning objectives:** Set up a compile/run workflow; explain the basic
  structure of a C program; read input and produce formatted output.
- **Key concepts:** Source files, `main`, compilation and linking, integer and
  floating-point types, variables, constants, operators, conversions,
  `printf`, `fgets`, and basic input validation.
- **Exercises (4 h):** Compile and run a minimal program; practice arithmetic
  and type conversions; format values; read lines and handle empty or malformed
  input.
- **Project deliverables (4 h):** A command-line unit and cost converter with
  clear prompts, validated input, and a short README containing build/run
  instructions.
- **Mastery criteria:** Build with warnings enabled; correctly handle at least
  five representative input cases, including malformed input; explain the
  types and conversions used; and demonstrate that invalid input does not
  produce a misleading result.

## Module 2 — Decisions and repetition (10 hours)

- **Learning objectives:** Express business rules using branches and loops;
  select suitable control flow; prevent common boundary and termination bugs.
- **Key concepts:** Boolean expressions, relational and logical operators,
  `if`/`else`, `switch`, `for`, `while`, `do`/`while`, loop invariants, and
  off-by-one errors.
- **Exercises (4 h):** Implement range checks, menu handling, sentinel-driven
  input, and loops over sets of values; trace branches and loop boundaries by
  hand.
- **Project deliverables (4 h):** A command-line service-time or expense
  estimator that applies configurable bands, accepts multiple records, and
  summarizes valid input.
- **Mastery criteria:** Pass tests for every decision branch and important
  boundary; terminate correctly for both valid and invalid input; and explain
  why each loop ends.

## Module 3 — Functions and program structure (10 hours)

- **Learning objectives:** Decompose a problem into cohesive functions; define
  clear function interfaces; separate implementation from use.
- **Key concepts:** Declarations and definitions, parameters and return values,
  scope and lifetime, pass-by-value, header files, source files, and basic
  compilation units.
- **Exercises (4 h):** Refactor calculations into functions; write and use a
  small header/source pair; trace local-variable scope and function calls.
- **Project deliverables (4 h):** A reusable command-line report calculator,
  split into input, calculation, and reporting modules with documented
  function contracts.
- **Mastery criteria:** Build the multi-file program cleanly; test each public
  function with normal and boundary inputs; avoid duplicated business logic;
  and explain the ownership and purpose of each function.

## Module 4 — Arrays, strings, and pointers (10 hours)

- **Learning objectives:** Process collections and C strings safely; explain
  how arrays and pointers relate; avoid out-of-bounds access.
- **Key concepts:** Array indexing, array parameters, null terminators,
  `size_t`, pointer declarations and dereferencing, pointer arithmetic,
  `const`, and bounded string operations.
- **Exercises (4 h):** Search and summarize arrays; measure and copy strings
  with explicit capacities; trace pointer values; test empty and maximum-size
  inputs.
- **Project deliverables (4 h):** A fixed-capacity log analyzer that reads
  lines, filters matching records, and reports counts without writing outside
  its buffers.
- **Mastery criteria:** Pass tests for empty, typical, and capacity-limit
  cases; demonstrate correct terminators and bounds; explain the difference
  between an array's storage and a pointer value; and compile without
  warnings.

## Module 5 — Data modeling and files (10 hours)

- **Learning objectives:** Represent related values with appropriate types;
  persist and retrieve records; handle file and parse failures explicitly.
- **Key concepts:** `struct`, `enum`, arrays of structures, `typedef`,
  formatted and line-oriented file I/O, file modes, parsing, and checking
  `fopen`, read, and write results.
- **Exercises (4 h):** Define records and status enums; read delimited data;
  reject malformed rows; write records and verify output by reading it back.
- **Project deliverables (4 h):** A small inventory or asset register that
  loads and saves records in a documented text format and supports search and
  summary operations.
- **Mastery criteria:** Correctly round-trip valid data; report missing,
  unreadable, and malformed files without crashing; test empty and
  representative files; and explain the record layout and file format.

## Module 6 — Dynamic memory and data structures (10 hours)

- **Learning objectives:** Manage dynamically allocated resources; choose a
  suitable data structure; prevent leaks, invalid frees, and use-after-free.
- **Key concepts:** `malloc`, `calloc`, `realloc`, and `free`; allocation
  failure; ownership and lifetime; linked lists; and the tradeoffs between
  fixed and dynamic storage.
- **Exercises (4 h):** Build and traverse a list; insert and remove nodes;
  handle allocation failures; audit each allocation against its cleanup path.
- **Project deliverables (4 h):** Extend the prior record tool to hold a
  variable number of records using a dynamically managed collection, with
  cleanup on both success and failure.
- **Mastery criteria:** Pass empty, single-item, and multi-item operations;
  show that all allocated memory has a clear owner and is released; handle
  allocation failure safely; and explain the chosen structure's tradeoffs.

## Module 7 — Errors, testing, and safe C (10 hours)

- **Learning objectives:** Make failures visible and recoverable; test behavior
  systematically; identify undefined behavior and common memory hazards.
- **Key concepts:** Return codes and error reporting, assertions, unit and
  integration tests, boundary and negative testing, integer overflow,
  undefined behavior, compiler warnings, and AddressSanitizer/UndefinedBehaviorSanitizer
  where available.
- **Exercises (4 h):** Write tests for prior modules; reproduce and fix
  deliberately introduced defects; run a sanitizer build; document expected
  behavior for invalid inputs and file failures.
- **Project deliverables (4 h):** A regression test suite and defect report
  for the record application, including reproduction steps, fixes, and test
  evidence.
- **Mastery criteria:** Tests cover normal, boundary, and failure paths;
  available sanitizers report no errors on the exercised paths; errors are
  reported without corrupting data or leaking resources; and each reported
  defect has a regression test.

## Module 8 — Build, debug, and integrate (10 hours)

- **Learning objectives:** Build a maintainable multi-file application; use a
  debugger to diagnose defects; deliver a reproducible program to another
  developer.
- **Key concepts:** Compiler and linker stages, include guards, build targets,
  debug symbols, breakpoints and stack traces, static libraries, command-line
  arguments, version control, and portability.
- **Exercises (4 h):** Build from a clean checkout; debug a failing test;
  split code into modules; review a change and resolve a merge conflict.
- **Project deliverables (4 h):** A release candidate of the record
  application with a repeatable build, usage documentation, example data, and
  a short handoff note.
- **Mastery criteria:** A new user can build and run from the documented
  instructions; the test suite passes from a clean build; the debugger is used
  to explain and fix a seeded defect; and the release has no known failing
  tests or compiler warnings.

## Module 9 — Capstone: workplace delivery (20 hours)

**Scenario:** Your team needs a dependable command-line tool to import a
vendor's asset inventory, validate and reconcile it with a local inventory,
and produce a reviewable exception report. The input may be incomplete or
malformed, and another developer must be able to build, test, and maintain the
result.

- **Learning objectives:** Translate a stakeholder request into acceptance
  criteria; design, implement, test, and document an integrated C application;
  communicate tradeoffs and operational limitations.
- **Key concepts:** Requirements and edge cases, modular design, record
  modeling, parsing and validation, memory/resource ownership, error handling,
  regression testing, reproducible builds, and handoff documentation.
- **Exercises (8 h):** Turn a brief into testable requirements; sketch module
  interfaces and input/output formats; implement parsing and reconciliation
  prototypes; review sample and adversarial records with a peer or checklist.
- **Project deliverables (8 h):** A working command-line inventory
  reconciliation tool; source and build instructions; documented input and
  output formats; automated tests and sample files; an exception report; and
  a concise design, limitations, and handoff note.
- **Mastery criteria:** Demonstrate all agreed acceptance criteria; correctly
  process valid, empty, duplicate, malformed, and boundary-case inputs; fail
  safely on file and resource errors; pass the full test suite and available
  sanitizer checks; build from a clean checkout using only the handoff
  instructions; and explain the design, tradeoffs, and known limitations to a
  reviewer.

## Completion

The curriculum is complete when the capstone meets every mastery criterion
and a reviewer can reproduce its build and tests from the handoff materials.
If any gate fails, remain at that module, address the gap, and demonstrate the
criterion again before proceeding.
