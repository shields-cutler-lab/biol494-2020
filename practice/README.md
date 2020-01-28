# Lab 1. Building familiarity with your computer as a research tool

#### Goals
0.5. Change the key repeat speed on your computer so you can move around in text more rapidly. Trust me.
1. Set up shell/command line access on your machine, or use a lab machine.
2. Learn how to navigate your computer via the command line by working through Chapter 4 of Practical Computing.
3. Read up about [Conda](https://docs.conda.io/en/latest/). What does "open-source" refer to?
4. Use [the install instructions to install Miniconda](https://docs.conda.io/projects/conda/en/latest/user-guide/install/macos.html) on your machine (if not already installed). Check with Robin before running the installation.
5. Work through chapters 1-3 of PCfB to learn the basics of text manipulation. If you don't already have a text editor installed, you'll need one. I prefer the one that is used for examples in the book: [BBedit](https://www.barebones.com/products/bbedit/) (free version; used to be TextWrangler); [SublimeText](https://www.sublimetext.com/) is also very popular, and Notepad++ for Windows also works.
6. Complete the exercises below.


### REGEXP TASKS:
These exercises will have you practice the text manipulation learned in Chapters 2 and 3. Exercises 1-4 are adapted from the PCfB authors.

You'll need to use a text editor (BBedit is preferred). The files referenced below are in the [example_files](../example_files/) directory of this GitHub repo.

The PCfB website has a handy Appendix PDF ([here](http://practicalcomputing.org/files/PCfB_Appendices.pdf)) that includes cheatsheets for many of the commands and regex terms.

----
#### Exercise 1
USING: `FPexamples.fta`, convert sequence names from this:
```
>CAA58790.1= green fluorescent protein [Aequorea victoria]
```
To this:
```
>Aequorea_victoria
```

#### Exercise 2
USING: `ctd.txt`, convert data lines from this: 
```
1194458835,11/07/2007 18:07:15,2,vnta,2.78,2,15.299,2,33.132,2,4.24,2,85.25,2,1505.48,2,24.4679,2,36.745953,2,-122.051688,2
```

To this: (rearrange dates and split)
```
2007    11    07    18    07    15    2    vnta    2.78    2    15.299    2    33.132    2    4.24    2    85.25    2    1505.48    2    24.4679    2    36.745953    2    -122.051688    2
```
HINT: Use two or more steps.

#### Exercise 3

The file `ims_faculty.txt` has a text dump from a [faculty directory at UC Santa Cruz](https://ims.ucsc.edu/people/institute-of-marine-sciences-all-people.php).

Extract faculty names and emails and convert to tab delimited as follows:
```
Peter\t Raimondi\t raimondi@biology.ucsc.edu
```
HINT: Some last names are hyphenated or doubled. Try to do as much in one step as possible; you may use two or three steps if needed.

#### Exercise 4

Using this GENBANK file:

`http://practicalcomputing.org/files/genbank.txt`

Use a regular expression (not Process Lines Containing..) to pull out the LOCUS lines. Then format with:
```
Name\tseqlength\tyear\tMonth\tday
```


#### Exercise 5

This is a real example of REGEX re-formatting that I used during winter break while building a new database for microbiome alignments.

In the `example_files` directory, there is a `siva_headers.txt` file (starting point) and a `silva_tax_output.txt` file (ending point). Design a single-step regular expression replacement to go from the headers file to the tax_output file.

