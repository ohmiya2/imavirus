# imavirus

<Pipeline to identify integration of HBV genome>
1. Quality check by FastQC

2. Quality control by PRINSEQ
    Trimming reads with lower than 20 phred quality score
    Discarding reads with shorter than 30 length
    Keeping read paires which pass all filters
  
3. Mapping reads to hg19 + HBV (NC_003977) reference genome by minimap2
  
4. Extracting paired-end reads which are mapped with one end to hg19 and with another to HBV.
  
5. Discarding PCR duplicates
  
6. Determining integration sites by mapping reads to hg19 and HBV (Blat)
