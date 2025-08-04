# Genetic Algorithm Series - #1 Generate
## My solution:
```bash
import random
def generate(length):
    return ''.join(random.choice('01') for _ in range(length))
```

## Instructions
A genetic algorithm is based in groups of chromosomes, called populations. To start our population of chromosomes we need to generate random binary strings with a specified length.

In this kata you have to implement a function generate that receives a length and has to return a random binary strign with length characters.

Example:
Generate a chromosome with length of 4 generate(4) could return the chromosome 0010, 1110, 1111... or any of 2^4 possibilities.

Note: Some tests are random. If you think your algorithm is correct but the result fails, trying again should work.

# Genetic Algorithm Series - #2 Mutation
## My solution:
```bash
import random
def mutate(chromosome, p):
    res = []
    
    for bit in chromosome:
        randomBit = random.random()
        
        if randomBit < p:
            if bit == '0':
                res.append('1')
            else:
                res.append('0')
        else:
            res.append(bit)
            
    return ''.join(res)
```

## Instructions
Mutation is a genetic operator used to maintain genetic diversity from one generation of a population of genetic algorithm chromosomes to the next.
A mutation here may happen on zero or more positions in a chromosome. It is going to check every position and by a given probability it will decide if a mutation will occur.
A mutation is the change from 0 to 1 or from 1 to 0.


Next:
https://www.codewars.com/kata/genetic-a
https://www.codewars.com/kata/genetic-algorithm-series-number-5-roulette-wheel-selectionlgorithm-series-number-4-get-population-and-fitnesses


