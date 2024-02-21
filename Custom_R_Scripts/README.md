Here you can find the custom R scripts used in this work.

For all scripts, you will need the output.html, reference.bam and the reference.bam.bai files obtained after running the Breseq pipeline.

- Post-Breseq_filtering.Rmd

This custom script performs the following steps: 

a) removal of the predicted mutations already present in the ancestral strains ran with the same parameters as the sequenced populations; 

b) calculation of the e14 excision frequency, in which we first perform the ratio of the e14 median coverage and the coverage in the left and right flank. The final frequency is obtained as the average of both ratios;

c) BLAST all the reads of each predicted mutations against the recipient and donor reference genomes (if reads that 100% match with the incorrect reference genome are at a frequency above 0.01, the predicted mutation is removed from the list and considered as a potential HGT event); 

d) removal of predicted mutations if they are detected in the reads of the ancestral clones at a frequency higher than 0.015 and with more than 3 reads.

- Checking_for_deletions.Rmd

This custom script calculates the frequency of the deletions that were observed in populations from the Donor strain and which were not detected by Breseq.
