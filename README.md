# INFO6205_Team231
Final project for course INFO6205

PROBLEM STATEMENT :
The problem we are attempting to solve with using genetic algorithm is that of finding the correct key for a substitution cipher from all 26! possible keys that will enable us to decrypt the cipher text into plain text.

A substitution cipher is a cipher that encrypts plain text by replacing each instance of a letter in the plain text with a substitution key. On the surface this cipher seems to be a strong one except that this cipher is vulnerable to frequency analysis;that is examining the subsets of letters in the encrypted text that occur repeatedly and storing them in a table against the values repeated subset of letters in the encrypted text.
We iterate through multiple generations to find the key that closely matches our cipher key. In each generation we apply:

CHROMOSOME:
Our population consists of a set of chromosomes, each of which contains a string of shuffled alphabets. That could be the possible key to the encrypted text.
We go about this problem by crossing over multiple chromosomes in each generation the chromosomes are selected in such a way such that 
1. SELECTION: the chromosomes are selected based on their fitness
2. We define a probability: The highest probalility is that is closest to the key of the cipher  
3. FITNESS: The fitness of each chromosome is determined by the probability 
4. ELITISM: We keep an elitism count. Elitism count keeps track of the fittest chromosomes in each generation. This is necessary because this helps to find the global maxima.
5. MUTATION: We mutate a subset of the fittest chromosome to generate a new chromosome this allows us to pass on the fitness of the chromosome into the next generation
6. CROSSOVER:  The fittest chromosomes are passed in each generation and are crossed over with the chromosomes of the current generation to generate a new chromosome population for the next generation.

By repeatedly doing this in subsequent generations we converge to a key that is closest to the key of the cipher.






