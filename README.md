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
2. Run the MSApriori algorithm:
   ```python
   python msapriori.py data_file.txt parameter_file.txt
   ```
3. The output will be generated in a file named output.txt.

## Important Notes
- The implementation strictly follows the input and output format specifications.
- No additional symbols or punctuation marks are used in the output beyond what is specified.
- The indentation in the output is not significant, but the round brackets must be placed correctly.

## Future Improvements
- Implement error handling for various input file formats
- Optimize the algorithm for larger datasets
- Add command-line options for customizing output file name and location

## References
- R. Agrawal and R. Srikant. "Fast algorithms for mining association rules." In Proc. 1994 Int. Conf. Very Large Data Bases (VLDB'94), pages 487-499, Santiago, Chile, Sept. 1994.
- B. Liu, W. Hsu, and Y. Ma. "Mining association rules with multiple minimum supports." In Proceedings of the fifth ACM SIGKDD international conference on Knowledge discovery and data mining, pages 337-341. ACM, 1999.
