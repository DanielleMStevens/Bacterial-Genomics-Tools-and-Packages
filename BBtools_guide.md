# BBtools Guide

### Check for contamination
```bash
sendsketch.sh in= ../4_8.fastq
```

### Remove contamination via gc content
```bash
bbduk.sh in1=Z001_illumina_1.pe.qc.fastq in2=Z001_illumina_2.pe.qc.fastq out1=clean_Z001_illumina_1.fastq\
out2=clean_Z001_illumina_2.fastq mingc=0.45
```

### Remove contamination via mapping reads to genomes
```bash
bbsplit.sh in1=./raw_reads/DMS92_2_S159_R1_001.fastq.gz in2=./raw_reads/DMS92_2_S159_R2_001.fastq.gz\
ref=/media/danimstevens/Second_storage/Genomes/DNA_contigs/CM_CASJ002.fasta,./GCF_000725365.1.fa.gz,\
./GCF_900110015.1.fa.gz basename=out_%.fq outu1=clean1.fq outu2=clean2.fq
```

### Determining read coverage
```bash
bbmap.sh in=reads.fq ref=contigs.fa covstats=covstats.txt
```
