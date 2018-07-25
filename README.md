# star_rsem
Snakemake pipeline to run STAR 2-pass alignment followed by RSEM quantification. 

# Usage
Paths to STAR, RSEM, GTFs, reference fasta are included in the Snakefile, `star_rsem.sm`
```bash
snakemake -p -s star.sm -j 24
```
# Preparation step
FASTQ files should be in the `fastq` folder in the same level as `star_rsem.sm`. FASTQ files can be directly placed inside the `fastq` folder or can simply be a soft link. Relative path from the Snakefile should be `./fastq/[0-9A-Za-z_]+_R1.fastq.gz` and `./fastq/[0-9A-Za-z_]+_R2.fastq.gz`.

Example folder structure is shown below:
```bash
.
├── ~
├── fastq
│   ├── 2685_pos_R1.fastq.gz -> /home/users/cjyoon/Projects/myeloma/rnafastq/2685_pos_R1.fastq.gz
│   └── 2685_pos_R2.fastq.gz -> /home/users/cjyoon/Projects/myeloma/rnafastq/2685_pos_R2.fastq.gz
├── star_rsem.sm
├── README.md
```

