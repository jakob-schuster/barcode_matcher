# match_cell_barcode_advanced

Adapted from [Luyi Tian's barcode matcher in FLAMES](https://github.com/LuyiTian/FLAMES), this searches fastq files for barcodes. Includes a few more parameters for more customization.

# Parameters

### 1. fastq folder

The directory of a folder containing only the fastq files you want to search through.

### 2. output cell barcode statistics file

A file to log the number of matches in a search, in CSV format.

### 3. fastq output reads that matched cell barcode

A file that the reads with matches will be printed to, as a compressed fastq (.fq.gz). Unwrap this with `gz -dk [filename]` to access it.

### 4. barcode reference from 10X data

A file that contains the barcodes you want to search for. 

```
cell_id,barcode
```

### 5. max edit distance

The maximum number of mismatches that will be tolerated in matching the barcodes.

### 6. UMI length (optional)

The expected length of a UMI.
Default is 10.

### 7. Left-flanking sequence (optional)

A static sequence, always expected to occur directly before the barcode.
Default is 'CTACACGACGCTCTTCCGATCT'.

