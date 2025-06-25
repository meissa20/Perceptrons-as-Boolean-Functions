# Perceptrons-as-Boolean-Functions

## Description

This project implements a Boolean logic circuit using **perceptrons**.

The circuit takes four binary inputs: `A`, `X`, `Y`, and `Z`, and computes a final output using layered perceptron-based gates (AND, OR, NOT). The logic has been implemented and tested using Python and NumPy.

## Objective

To simulate a combinational logic circuit using only **perceptron units**, and test it on specific input combinations provided by the assignment.

## Logic Design

The circuit is built from multiple perceptron layers as follows:

- **Layer 1:**
  - `AXnotZ = A AND (NOT X) AND Z`
  - `AYnot = A AND (NOT Y)`
  - `XY = X AND Y`
  - `XZ = X AND Z`

- **Layer 2:**
  - `OR1 = AXnotZ OR AYnot`
  - `OR2 = 1 if XY ≥ XZ`

- **Final Output:**
  - `Output = OR1 AND OR2`

Each logic gate is simulated using a perceptron with appropriate weights and thresholds.

## Test Cases

The circuit is tested on the following 4 input combinations:

| A | X | Y | Z | Output |
|---|---|---|---|--------|
| 0 | 0 | 0 | 0 |   0    |
| 1 | 1 | 1 | 1 |   0    |
| 1 | 1 | 0 | 0 |   1    |
| 0 | 1 | 0 | 1 |   0    |

## Files

- `Perceptrons-as-Boolean-Functions.py` — Contains the implementation of the perceptron and the logic circuit.
- `README.md` — Project description and documentation.

## Requirements

- Python 3.x
- NumPy

Install dependencies using:

```bash
pip install numpy
