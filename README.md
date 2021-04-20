# Programming for life sciences

#**Write a function that reverse complements this sequence (10mks)
DNA="ATCGATCGATCAGATTTAAACGGCATATCATAGCACGTACATGACG"**

def inverseComplement(input):
    output = ''
    for letter in input:
        letter = letter.upper()

        if letter == 'A':
            output += 'T'
        elif letter == 'T':
            output += 'A'
        elif letter == 'G':
            output += 'C'
        else:
            output += 'G'

    return(output[::-1])
DNA="ATCGATCGATCAGATTTAAACGGCATATCATAGCACGTACATGACG"
print(inverseComplement(DNA))

# Write a for loop that prints values 4-10 (2.5mks)
for value in range(4,11):
        print(value)

**#Create a while loop that starts with x = 0 and increments x until x is equal to 5. Each iteration should print to the console. (2.5mks)
**

x = 0
while x <= 5:
  print(x)
  x += 1

# **Using a DNA sequence read from file, answer the following questions: (20mks)
Show that the DNA string contains only four letters.
**

#counting DNA nucleotides
DNA="ATCGATCGATCAGATTTAAACGGCATATCATAGCACGTACATGACG"
from collections import Counter
print(Counter(list(DNA)))

**#How many ’ATG’s are in the DNA string?
**

#counting DNA nucleotides
DNA="ATCGATCGATCAGATTTAAACGGCATATCATAGCACGTACATGACG"
from collections import Counter
print(Counter(list(DNA)))

print(DNA.count("ATG"))

**#Create a bash script called hello.sh that takes a command line input of name, bash hello.sh Brian, prints: (5mks)
**
Hello Brian.
How are you?

#!/bin/bash
echo "Hello $1"
echo "How are you?"

**#Write a script that counts the number of sequences in each fasta file in the Exam_dataset. It should print to console the name of the file and the number of sequences, each separated by a tab. For example, if sequence1.fasta has 10 sequences, it should print:
sequence1.fasta: 10 (10mks)
**

for file in `ls *fasta`
do
S=`grep ">" -c $file`
echo $file :$S
done

**#Write a script that extracts the sequence headers of all the provided fasta files, and writes the output in the Results directory to a file all_sequence_headers.txt. (10mks)
**

for file in `ls *fasta`
do
grep ">" $file >>all_sequence_headers.txt
done

