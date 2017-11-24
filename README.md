

# IGV Batch Generator

Given an input of a CSV file containing gene loci and a mapping of
samples to their corresponding BAM files, creates an IGV batch script
that will save images of the corresponding genetic loci.

The generated file must be run by IGV in order to generate the specified
images.

## Input Data

This script expects the following headers in the input CSV file.
There currently is no support for .xls or .xlsx files.

    SampleID
    CHROM
    POS

## Installation

Change the SAMPLE_BAM_MAPPING_LOCATION variable in batch_generator.py
to reflect the location of the sample map file. Alternatively, supply
the -m flag when running `batch_generator.py`.

## Running batch_generator on Orchestra

On Orchestra, execute the following command at the command prompt (omit
the `$`, which is a customary indicator of the command prompt line):

```sh
$ /opt/java/jdk1.8.0_45/bin/java -Xmx3000m -jar /opt/IGV_2.3.57/igv.jar -b BATCH_FILE_PATH
```

* NB: Certain commands may fail when the batch file is run directly from
  the command-line, notably `maxPanelHeight` and `expand`



