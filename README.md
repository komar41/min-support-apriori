# MSApriori Algorithm Implementation

This project implements the Multiple Support Apriori (MSApriori) algorithm from scratch using Python, based on the given input and output specifications.

## Input

The program takes two input files in plain text format:

1. **Data File**: Contains transactions, with each line representing a transaction and items represented by integer numbers.
   Example:
   ```
   10, 50, 30, 40
   1, 2, 4, 6, 8, 9, 10
   3, 4, 5
   7, 9, 20
   ```
2. **Parameter File**: Contains MIS (Minimum Item Support) values for items and SDC (Support Difference Constraint).
   Example:
   ```
   MIS(1) = 0.02
   MIS(2) = 0.04
   ...
   MIS(rest) = 0.01
   SDC = 0.003
   ```
