# psmc_run1
The large sam file created by bwa mem during gene mapping needed to be converted to a smaller compressed file format 'bam' this is completed done on a shell. The bam file was sorted and aligned to be make ready for the consensus analysis. Thereafer, the variant calling was done using the samtools and bcftools to check the variants between the sequence data and the reference genome.
The variant calling generated a FASTQ file which needed to be converted into a PSMCFA recognized by PSMC which runs in python.
