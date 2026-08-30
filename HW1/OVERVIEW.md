# Homework 1 — What's in It

PHYS 7810: Quantum Error Correction, Fall 2026. Due September 8.

Three problems.

## Problem 1 — How a qubit actually loses information

An excited atom can randomly emit a photon and fall to its ground state. This problem
turns that real physical process into the kind of error model we use in error
correction (Kraus operators).

- **A**: Do the math showing that "the atom might emit a photon" is the same thing as
  a specific 2-operator error channel. Then check the math is self-consistent (a valid
  channel).
- **B**: Given that error, could one of our known error-correcting codes fix it? How
  would you actually detect and fix the error in the lab?

## Problem 2 — Storing a qubit in a single bigger particle

Normally we spread one logical qubit across several physical qubits. Here, instead,
we try to hide a qubit inside a single particle that has more than 2 levels (a
"qudit") — the idea behind GKP codes used in real superconducting-circuit experiments.

- **A**: Set up a specific 8-level example and check it correctly holds one qubit's
  worth of information.
- **B**: Figure out which errors this code can fix, and whether that's the only
  possible choice.
- **C**: Write down and explain, in physical terms, how you'd actually correct an
  error if one happened.
- **D**: Show there's a fundamental limit — some pairs of errors can't both be fixed
  by the same code, and explain why.
- **E–F**: Build a better version (10 levels) that fixes a bigger, more natural set of
  errors, and show why you need at least 10 levels to do it.

## Problem 3 — How good does your hardware need to be?

This one is about the simplest error-correcting code there is — just repeating a bit
many times — but asks a harder question: what if the errors aren't random, but placed
by an adversary trying to trick the decoder? And what if your error-checking
measurements are themselves sometimes wrong?

- **A**: Prove that as long as the error rate and measurement-error rate are both
  below a certain threshold, the standard decoding strategy is *guaranteed* to work,
  even against worst-case (not just random) errors.
- **B**: Even if the decoder gets the right answer overall, does it also get every
  single bit right? Explain why or why not.

## The big picture connecting all three

- Problem 1 shows where an error model comes from physically; Problems 2 and 3 assume
  an error model and ask how to correct it.
- Problem 2 pushes on the limits of what a code can fix; Problem 3 pushes on how much
  noise a code can tolerate before it stops working.
- Together they cover the three basic questions of error correction: what causes
  errors, what can be fixed, and how much noise is too much.
