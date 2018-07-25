# star_rsem
Snakemake pipeline to run STAR 2-pass alignment followed by RSEM quantification. 

# Usage
Searches for all paired-end fastq.gz files that are in side `./fastq` folders. 
Fastq files should have the following path  `./fastq/[0-9A-Za-z_]+_R1.fastq.gz` `./fastq/[0-9A-Za-z_]+_R1.fastq.gz`  

Paths to STAR, RSEM, GTFs, reference fasta are included in the Snakefile, `star_rsem.sm`
```bash
snakemake -p -s star.sm -j 24
```
will run the pipeline using 24 cores. 

