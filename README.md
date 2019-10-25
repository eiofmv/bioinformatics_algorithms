**Table of Contents**

- [1. Alignments](#1-alignments)
  * [Needleman–Wunsch algorithm]
  * [Alignment with the matrix of weights]
  * [Smith–Waterman algorithm]
  * [Affinity gaps]
- [2. BLAST](#2-blast)

# [1. Alignments](./1_ALIGNMENTS/1_alignments.ipynb)

## Needleman–Wunsch algorithm
**Task:**

To implement the global alignment algorithm, which receives two sequences at the input, and produces their optimal alignment. A fixed penalty for mismatch and gap and a reward of 1 for each match.

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
 --------- | --------- | --------- | --------- | -----
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

1. GGACC
The expected number of paired bases is 1.
2. AAACAUGAGGAUUACCCAUGU
The expected number of paired bases is 7.
