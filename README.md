# MSApriori Algorithm Implementation

The Apriori algorithm is a fundamental data mining technique for finding frequent itemsets in transaction databases. It works by identifying individual items that meet a minimum support threshold, then extends to larger itemsets, pruning those that don't meet the threshold.

Key concepts:
- Itemset: Collection of items
- Support: Frequency of an itemset
- Frequent itemset: Itemset with support above a threshold

Example:

Transaction database:
- T1: {A, B, C}
- T2: {B, C, D}
- T3: {A, C, D}
- T4: {B, C, D}

Minimum support: 50% (2 transactions)

Process:

- Find frequent 1-itemsets: {A}, {B}, {C}, {D}
- Generate 2-itemsets: {A,B}, {A,C}, {A,D}, {B,C}, {B,D}, {C,D}
- Prune infrequent: {A,B}
- Continue until no more frequent itemsets found

Result: Frequent itemsets {A}, {B}, {C}, {D}, {B,C}, {B,D}, {C,D}

This project implements the Multiple Support Apriori (MSApriori) algorithm from scratch using Python, based on the given input and output specifications.

<p>
  <img src="https://github.com/user-attachments/assets/a6ce000a-6e8a-4e0a-b70c-bf61ca64243f" width="60%">
</p>

(image source: [Datacamp](https://www.datacamp.com/tutorial/market-basket-analysis-r))

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

Note: 'rest' refers to all other items not given specific MIS values.

## Output
The output file follows a specific format:
```
(Length-1 <number of length 1 frequent itermsets>
<length-1 itemset 1>
<length-1 itemset 3>
...
)
(Length-2 <number of length 2 frequent itermsets>
<length-2 itemset 1>
<length-2 itemset 3>
...
)
...
```

Example output:
```
(Length-1 3
(1)
(2)
(11)
)
(Length-2 2
(1 2)
(2 3)
)
```

## Implementation Details

- The algorithm reads the data and parameter files to initialize the transaction database and MIS values.
- It then performs the MSApriori algorithm to find frequent itemsets.
- The output is generated according to the specified format, listing frequent itemsets of each length.

## Usage

1. Prepare the data file and parameter file as per the specified format.
2. Run the MSApriori algorithm through the jupyter notebook: `MSApriori Final Version.ipynb`
3. The output will be generated in a file named output.txt.

## Important Notes
- The implementation strictly follows the input and output format specifications.
- No additional symbols or punctuation marks are used in the output beyond what is specified.
- The indentation in the output is not significant, but the round brackets must be placed correctly.


## References
- R. Agrawal and R. Srikant. "Fast algorithms for mining association rules." In Proc. 1994 Int. Conf. Very Large Data Bases (VLDB'94), pages 487-499, Santiago, Chile, Sept. 1994.
- B. Liu, W. Hsu, and Y. Ma. "Mining association rules with multiple minimum supports." In Proceedings of the fifth ACM SIGKDD international conference on Knowledge discovery and data mining, pages 337-341. ACM, 1999.

## Team
- Kazi Shahrukh Omar
- Soham Pradhan
