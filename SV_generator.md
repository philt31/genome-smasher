# SV\_generator.sh #

SV\_generator. sh is a useful shell script that calls several perl scripts that help to generate structural variations to insert into a synthetic genome.

# Usage #

```
Usage: SV_Generator.sh <SCRIPTS_DIR> <Genome_DIR> <OUTPUT_VCF> <NUM_BASES_FASTAFILE_EACHLINE>"
```

The inputs are defined below:

  * SCRIPTS\_DIR
    * The scripts directory is the full path to a series of perl scripts that will generate different types of structural variations:
      1. Copy\_number\_changes.pl
      1. Inversions.pl
      1. Large\_Deletions.pl
      1. Novel\_insertions.pl
      1. Translocations.pl

  * Genome\_DIR
    * The scripts directory is a directory that contains chromosome files for an individual reference genome assembly.  They must be stored by chromosome, beginning with "chr" and ending with ".fa".

  * OUTPUT\_VCF
    * This is the name of the final vcf-like file to create

  * NUM\_BASES\_FASTAFILE\_EACHLINE
    * some FAST files are 60 nucleotides long, whereas others are 50.  Make sure to select the corresponding length for your reference FASTA file inputs.

## Special Notes ##
No mutations will be added if the nucleotide where the event is being inserted is "N".