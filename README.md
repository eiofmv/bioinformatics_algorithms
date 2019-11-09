**Table of Contents**

- [1. Alignments](#1-alignments)
  * Needleman–Wunsch algorithm
  * Alignment with the matrix of weights
  * Smith–Waterman algorithm
  * Affinity gaps
- [2. BLAST](#2-blast)
- [3. RNA](#3-rna)
- [4. TREES](#4-trees)
  * Weighted Pair Group Method with Arithmetic Mean
  * Unweighted Pair Group Method with Arithmetic Mean
  * Neighbor Joining

# [1. Alignments](./1_ALIGNMENTS/1_alignments.ipynb)

## Needleman–Wunsch algorithm
**Task:**

Implement the global alignment algorithm, which receives two sequences at the input, and produces their optimal alignment. A fixed penalty for mismatch and gap and a reward of 1 for each match.

**Tests:**
                
1. To come up with fines and sequences of the same length so that there are discrepancies and gaps in the resulting alignment.
2. For sequences from test 1, run the algorithm with weights 1 (match), -1 (mismatch), -0.499 (gap).
                

## Alignment with the matrix of weights
**Task:**

In the previous problem, instead of a fixed fine, use any weight matrix. Enough size is (3 + 1) on (3 + 1).

**Tests:**
                
1. To come up with a sequence and a matrix, align the sequence. Change one number in the matrix so that the alignment changes.
                

## Smith–Waterman algorithm
**Task:**

Find the optimal alignment of all possible subwords of two sequences, that is, local alignment. From the output should be clear where local alignment begins and ends.

**Tests:**
                
1. To come up with two sequences for which local and global alignment with the same penalties give different results (in the local alignment section).
                

## Affinity gaps
**Task:**

Implement a global alignment algorithm with affine gaps.

**Tests:**

Sequences:
TCCCAGTTATGTCAGGGGACACGAGCATGCAGAGAC, AATTGCCGCCGTCGTTTTCAGCAGTTATGTCAGATC
                
 Test case | Match | Mismatch | Gap opening | Gap continuation
 :---------:|:---------:|:---------:|:---------:|:-----:
 1  | 1 |-1 |  0 | -1
 2 |  1 | -1 | -100 | -0.01
 3 | 1 | -1 | 0.5 | -0.3

# [2. BLAST](./2_BLAST/2_BLAST.ipynb)

**Task:**

Generate 3 random nucleotide sequences of length 100, 1000 and 10 000. Use the [blastn tool](https://blast.ncbi.nlm.nih.gov/Blast.cgi) to search for the obtained sequences by `Nucleotide collection (nr / nt)`. 
Save screenshots with search options and search results. `E-value` should be visible in the screenshots with the results.

# [3. RNA](./3_RNA/3_RNA.ipynb)

**Task:**

Implement the Nussinov algorithm, which obtains the secondary structure of the RNA sequence with the maximum number of paired bases. The minimum size of the stem is 3. The output can be either graphic or a list of paired bases.

**Tests:**

Test case | RNA | Expected number of paired bases 
 :---------:|:---------:|:---------:
 1  | GGACC | 1
 2 | AAACAUGAGGAUUACCCAUGU | 7

# [4. Trees](./4_TREES/4_Trees.ipynb)

## Weighted Pair Group Method with Arithmetic Mean 
## Uneighted Pair Group Method with Arithmetic Mean
## Neighbor Joining
**Task:**

Implement a program that implements algorithms WPGMA, UPGMA, NJ.

**Tests:**
1. Test case 1
  | A | B | C | D  
 :-:|:-:|:-:|:-:|:-:
A |  | 16 | 16 | 10
B |  | | 8 | 8
C | | | | 4
D | | | | 

2. Test case 2
  | A | B | C | D | E | F
 :-:|:-:|:-:|:-:|:-:|:-:|:-:
A |  | 5 | 4 | 7 | 6 | 8
B |  | | 7 | 10 | 9 | 11
C | | | | 7 | 6 | 8
D | | | | | 5 | 9
E | | | | | | 8
F | | | | | | |

