# BBtools Guide

### Check for contamination
```bash
sendsketch.sh in= ../4_8.fastq
```

### Remove contamination via gc content
```bash
bbduk.sh in1=Z001_illumina_1.pe.qc.fastq in2=Z001_illumina_2.pe.qc.fastq out1=clean_Z001_illumina_1.fastq out2=clean_Z001_illumina_2.fastq mingc=0.45
```
