# DNA Identification Program README

This repository contains a Python program that identifies a person based on their DNA using Short Tandem Repeats (STRs). The program compares a given DNA sequence with a CSV database containing STR counts for a list of individuals.

## Getting Started

To get started, follow these steps:

1. Log into [cs50.dev](https://cs50.dev) or your development environment.

2. Open a terminal window and navigate to the desired directory where you want to clone this repository.

3. Execute the following commands to download and set up the project:
   
   ```bash
   wget https://cdn.cs50.net/2022/fall/psets/6/dna.zip
   unzip dna.zip
   rm dna.zip
   cd dna

## Background
DNA profiling is a technique used in forensic science to identify individuals based on their DNA sequences. DNA is composed of nucleotides, and certain sequences called Short Tandem Repeats (STRs) are known to have high genetic diversity among individuals. The program uses a CSV file that stores the STR counts for different individuals to make DNA identifications.

DNA is really just a sequence of molecules called nucleotides, arranged into a particular shape (a double helix). Every human cell has billions of nucleotides arranged in sequence. Each nucleotide of DNA contains one of four different bases: adenine (A), cytosine (C), guanine (G), or thymine (T). Some portions of this sequence (i.e., genome) are the same, or at least very similar, across almost all humans, but other portions of the sequence have a higher genetic diversity and thus vary more across the population.

One place where DNA tends to have high genetic diversity is in Short Tandem Repeats (STRs). An STR is a short sequence of DNA bases that tends to repeat consecutively numerous times at specific locations inside of a person’s DNA. The number of times any particular STR repeats varies a lot among individuals. In the DNA samples below, for example, Alice has the STR AGAT repeated four times in her DNA, while Bob has the same STR repeated five times.
![Dna reference](https://cs50.harvard.edu/x/2023/psets/6/dna/strs.png)


## How the Program Works
The program takes two command-line arguments: the name of the CSV file containing the STR counts and the name of the text file containing the DNA sequence to identify.

It reads the CSV file into memory, assuming the first row contains column names, and the first column is labeled "name."

It reads the DNA sequence from the text file into memory.

For each STR listed in the CSV file, the program computes the longest run of consecutive repeats of that STR in the DNA sequence using the provided helper function longest_match.

If the STR counts match exactly with any individual in the CSV file, the program prints the name of the matching individual.

If there is no exact match, the program prints "No match."





## Usage
To run the program, use the following command:

```bash
   Copy code
   python dna.py databases/large.csv sequences/5.txt
   Replace databases/large.csv and sequences/5.txt with the paths to your CSV database and DNA sequence files, respectively.
```

### Example Output
If there is a match, the program will print the name of the matching individual. If there is no match, it will print "No match."

## Additional Information
For more details on the problem statement , refer to the [CS50 DNA Problem](https://cs50.harvard.edu/x/2023/psets/6/dna/) .




















