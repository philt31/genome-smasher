**GenomeSmasher** is a set of tools used to create diploid fasta files with containing snps, indels, duplications, deletions, and translocations.  These FASTA files can then be used in conjunction with next-gen sequencing simulators to artificially create sequencing experiments.  The utitlity of these tools are to assess the performance and reliability of data analysis in next-gen sequencing pipelines.

We also provide 2 scripts to help prepare input files for GenomeSmasher
  1. [SNP\_mutator\_v2.pl](http://code.google.com/p/genome-smasher/wiki/SNP_mutator)
  1. [SV\_generator.sh](http://code.google.com/p/genome-smasher/wiki/SV_generator)

Input parameters to the script
  * 'refgenome\_dir' => Path to the genome directory (Each chromosome must have separate fasta file Ex: Chr1.fa).
  * 'input\_vcf\_like’ => Structural Variants to be implemented must be described in the VCF like file(Fist 8 columns mandatory).
  * 'process\_dir' => Path to the directory where temporary files and results will be created.(Temporary files are deleted in the directory).
  * 'ins\_files\_dir' => Path to the directory with all input insertion sequences.(Must be in fasta format).

```
USAGE: perl perl_genome_simulator.pl  -refgenome_dir <REF CHR DIREC> -input_vcf_like <INPUT vcf likefile> -ins_files_dir <INSERT FILES DIR> -process_dir <TEMPDIR>
```
OUTPUT:
  1. New pairs of Chromosome files are generated with structural variants mentioned in the VCF file.
  1. A new VCF file is generated describing about all the structural variants implemented.
  1. Log file is created.

NOTE
  1. No two structural variants should exist on the same line (A single line consists of 50 bases) except for snps and translocations.
  1. No event will be added if the reference genome base = "N".

For help, see our [FAQ](http://code.google.com/p/genome-smasher/wiki/FAQ) page.