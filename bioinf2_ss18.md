# Bioinformatics 2
Summer Semester 2018  
Prof. Dr. Rolf Backofen  
[Course website](http://www.bioinf.uni-freiburg.de/Lehre/Courses/2018_SS/V_BioinfoII/)

## 1. ProbCons
- Given:
  - Pair HMM  
  <img src = "https://www.researchgate.net/profile/Yasuo_Tabei/publication/5636990/figure/fig3/AS:216410460352514@1428607682909/A-pair-HMM-for-pairwise-sequence-alignment-A-pair-HMM-is-used-for-alignment-of-loop.png" height="300px"></img>

1. Two sequences given: `A` and `B`.  
Write down all the possible alignments of the sequences produced by the given HMM.  
Also write down the state sequences and path probabilities (without the starting state probabilites π).

2. Given alignments: `a*`, `a1`, `a2`.  
Calculate the accuracies `acc(a*, a1)` and `acc(a*, a2)`.

3. ProbCons prefers pairwise alignments with the high probability edges.  
__True / False__

## 2. Probalign
1. Explain the difference between ProbCons and Probalign.

2. If a partition function `Z(T)` is given, write down the formula to calculate `Pr[x_i ~ y_j | x, y]`
(does not have to be efficient).

3. In ProbCons, functions for the efficient computation of `Pr[x_i ~ y_j | x, y]` are called forward and backward
variable. What is the name of such functions in Probalign?

## 3. Hidden Markov models (HMMs)
- Given:
  - transition probabilities table
  - emission probabilities table

1. Draw the HMM defined by the two tables.

2. Observation `O` is given (sequence of symbols).  
How many possible paths are there?

3. Calculate the most probable path for the given observation `O` using the Viterbi algorithm
(fill the table and do the traceback).

## 4. T-Coffee
1. The alignment of sequences `a` and `b` is given. Specify all entries in the primary library (`L`) different than 0.

2. The following alignments and weights are given:  
  `a - b`  
  `a - c`  
  `b - c`  
  `weight (a - c) = 67`  
  `weight (b - c) = 50`  
  
  Calculate the extended library (`EL`) for `a` and `b`.

3. Given:
  - sequences `d`, `e` and `f`
  - filled Needleman-Wunsch (NW) matrix that aligns `e` to already aligned `d` and `f`
  - extended library (`EL`) for the sequences
  
  Sketch the guide tree. Do the traceback to calculate the final alignment (`d - e - f`).

## 5. BLAST
- Given:
  - PAM/BLOSUM scoring matrix (for amino acids)
  - query
  - database
  - `k`
  - `T1` (threshold)

1. Write down all the k-mers with score `>= T1`.

2. Find the maximum scoring pair (MSP).

3. How to accelerate this approach and what would be the drawbacks? 

## 6. Suffix trees 
- Given:
  - text `T`

1. Sketch the suffix tree for the given text.

2. Pattern `P` is given.  
List the steps of the counting query.

3. Pattern `P` is given.  
List the steps of the reporting query.

4. Two sequences `A` and `B` are given.  
Sketch the corresponding suffix tree and find all the maximum unique matches (MUMs).

## 7. High throughput sequencing (HTS)
1. Explain the concept of high throughput sequencing.

2. Name one use case of sequencing and the method associated with it.
