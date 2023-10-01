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


## How the Program Works
The program takes two command-line arguments: the name of the CSV file containing the STR counts and the name of the text file containing the DNA sequence to identify.

It reads the CSV file into memory, assuming the first row contains column names, and the first column is labeled "name."

It reads the DNA sequence from the text file into memory.

For each STR listed in the CSV file, the program computes the longest run of consecutive repeats of that STR in the DNA sequence using the provided helper function longest_match.

If the STR counts match exactly with any individual in the CSV file, the program prints the name of the matching individual.

If there is no exact match, the program prints "No match."

