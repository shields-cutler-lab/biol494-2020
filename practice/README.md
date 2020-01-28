# Building familiarity with your computer as a research tool

These exercises will have you practice the text manipulation learned in Chapters 2 and 3

### REGEXP TASKS:
You'll need to use a text editor (BBedit, Sublime Text, Notepad). The files referenced below are in the `example_files` directory.

----
#### Exercise 1
USING: FPexamples.fta, convert sequence names from this:
```
>CAA58790.1= green fluorescent protein [Aequorea victoria]
```
To this:
```
>Aequorea_victoria
```

#### Exercise 2
USING: ctd.txt
Convert data lines from this: 
```
1194458835,11/07/2007 18:07:15,2,vnta,2.78,2,15.299,2,33.132,2,4.24,2,85.25,2,1505.48,2,24.4679,2,36.745953,2,-122.051688,2
```

To this: (rearrange dates and split)
```
2007    11    07    18    07    15    2    vnta    2.78    2    15.299    2    33.132    2    4.24    2    85.25    2    1505.48    2    24.4679    2    36.745953    2    -122.051688    2
```
HINT: Use two or more steps.

#### Exercise 3

Go to http://ims.ucsc.edu/facres/

Copy faculty names and convert to tab delimited
```
Peter\t Raimondi\t raimondi@biology.ucsc.edu
```
HINT: Some last names are hyphenated or doubled. The "ZZZZZ" trick might be handy here. TRY doing it as ONE step, or in multiple steps

#### Exercise 4

Using this GENBANK file:
http://practicalcomputing.org/files/genbank.txt

Use a regular expression (not Process Lines Containing..) to pull out the LOCUS lines. Then format with:
```
Name\tseqlength\tyear\tMonth\tday
```


#### Exercise 5

This is a real example of REGEX re-formatting that I used during winter break while building a new database for microbiome alignments.

In the `example_files` directory, there is a `siva_headers.txt` file (starting point) and a `silva_tax_output.txt` file (ending point). Design a single-step regular expression replacement to go from the headers file to the tax_output file.

