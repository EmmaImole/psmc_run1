# psmc_run1
The large sam file created by bwa mem during gene mapping needed to be converted to a smaller compressed file format 'bam'. The bam file was sorted and aligned to be make ready for the consensus analysis. Thereafer, the variant calling was done using the samtools and bcftools to check the variants between the sequence data and the reference genome.
The variant calling generated a FASTQ file which needed to be converted into a PSMCFA recognized by PSMC which runs in python.
# PSMC installation
The PSMC used for this study was from
$ git clone https://github.com/lh3/psmc.git
And I moved the fq2psmcfa.c file to the same directory location where the psmc.c, kseq.h, and Makefile files are present
$ mv /exports/eddie/scratch/s2749646/psmc/utils/fq2psmcfa.c /exports/eddie/scratch/s2749646/psmc
and built the PSMC using
$ make
The fq2psmcfa was compiled using the command below, however, this must be in -lz as a zip file to prevent large memory usage.
$ gcc -O2 -o fq2psmcfa -I /exports/eddie/scratch/s2749646/psmc fq2psmcfa.c -lz
