# Bioinformatics 1
Winter Semester 2017 / 2018  
Prof. Dr. Rolf Backofen  
[Course website](http://www.bioinf.uni-freiburg.de/Lehre/Courses/2017_WS/V_Bioinformatik_1/)

## 1.  Molecular biology
1. Complete the given figures by filling in the following terms:
  - _replication_
  - _transcription_
  - _translation_
  - _base pairs_
  - _amino acids_

2. Why scientists considered 95% of DNA junk?
3. What are ncRNAs?

## 2. Levenshtein distance
- Given:
  - sequence alignment
1. What is the score of the given alignment?
2. Maximal optimal alignment
3. Maximal edit distance

## 3. Needleman-Wunsch algorithm
- Given:
  - dynamic programming (DP) matrix
1. From the given matrix, determine the scoring scheme and the optimal alignment(s)
2. What is the minimal space complexity?
3. ?

## 4. Your approach
- Given:
  - PAM scoring matrix
  - Weird gap penalty function: `g(l) = -l + sin(l)`
  - Sequences `S1` and `S2`
  - 20th amino acid of `S1` and 25th amino acid of `S2` have to be aligned
1. How would you approach this problem?
2. What is time complexity and how to make it better?

## 5. Markov chain
- Given:
  - 2 states
  - only 2 transition probabilities (other are 1 - given)
1. What is the Markov property and why is it useful?
2. Draw a graphical representation of the given chain.
3. Calculate the stationary distribution of the chain.
4. A sequence of states is given. Calculate the probability of the sequence.

## 6. PAM matrices
?

## 7. Phylogenetic tree construction
- Given:
  - distance matrix
  - tree sketch
1. Under the assumption that tree is additive, fill the missing edges (distances) in the tree.
2. Perform the tree construction using the distance matrix and UPGMA.
3. What does UPGMA stand for?

## 8. Quadtree sampling
?
