# SNP\_mutator\_v2.pl #

SNP\_mutator\_v2.pl is a perl script that will generate a vcf file of positions of single nucleotide variations, as well as small insertions and deletions that can be used as input for GenomeSmasher.


# Usage #
```
usage: SNP_mutator.pl -f <chr##.fa> [-omid]

```
  * -o Output File. Default = snp\_mutator\_output.vcf
  * -m Total number of Desired point Mutations
  * -i Total number of Desired Insertions
  * -d Total number of Desired Deletions

## Special Notes ##
If the nucleotide in the reference is "N", that poistion will be skipped and no mutation will not be made