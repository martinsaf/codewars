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

### Example:
Generate a chromosome with length of 4 generate(4) could return the chromosome 0010, 1110, 1111... or any of 2^4 possibilities.

---

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

---

# Genetic Algorithm Series - #3 Crossover

## My solution

```bash
def crossover(chromosome1, chromosome2, index):
    new1 = chromosome1[:index] + chromosome2[index:]
    new2 = chromosome2[:index] + chromosome1[index:]
    return [new1, new2]
```

## Instructions

In this kata you have to implement a function that receives two chromosomes chromosome1, chromosome2 and a zero-based index and it has to return an array with the crossover result on both chromosomes [chromosome1, chromosome2].

### Example:
```bash
chromosome1 = "111000"
chromosome2 = "000110"
index = 3
# should return ["111110", "000000"]
```

---

# Genetic Algortihm Series - #4 Get population and fitnesses

## My solution:
```bash
def map_population_fit(population, fitness):
    return [ChromosomeWrap(chromosome, fitness(chromosome)) for chromosome in population]
```

## Instructions

In a genetic algorithm, a population is a collection of candidates that may evolve toward a better solution.

We determine how close a chromosome is to a ideal solution by calculating its fitness. https://www.codewars.com/kata/567b468357ed7411be00004a/train You are given two parameters, the population containing all individuals and a function fitness that determines how close to the solution a chromosome is.

Your task is to return a collection containing an object with the chromosome and the calculated fitness.

```bash
[
  { chromosome: c, fitness: f },
  { chromosome: c, fitness: f },
  ...
]
```

Note: you have a pre-loaded namedtuple ChromosomeWrap and you should return a collection of it instead.

```bash
ChromosomeWrap = namedtuple("ChromosomeWrap", ["chromosome", "fitness"])
```

