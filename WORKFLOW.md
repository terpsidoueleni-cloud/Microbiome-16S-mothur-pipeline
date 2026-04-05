# Mothur 16S Workflow Explanation

This document explains each step of the microbiome analysis pipeline.

## Step 1 - Create input file

```bash
make.file(inputdir=., type=fastq, prefix=stability)

Creates a .files file describing paired-end FASTQ reads.

## Step 2 - Assemble paired-end reads

make.contigs(file=stability.files)

Merges forward and reverse reads into contigs.

## Step 3 - Quality filtering

screen.seqs(maxambig=0, maxlength=275)

Removes low-quality sequences and ambiguous bases.

## Step 4 - Dereplication

unique.seqs()
count.seqs()

Collapses identical sequences and tracks abundance.

## Step 5 - Alignment

align.seqs(reference=silva.v4.fasta)

Aligns sequences to the SILVA 16S reference database.

## Step 6 - Alignment filtering
screen.seqs()
filter.seqs()

Keeps only the correct alignment region.

## Step 7 - Pre-clustering

pre.cluster(diffs=2)

## Step 8 - Chimera removal

chimera.vsearch()
remove.seqs()

Removes PCR artefacts.

##Step 9 - Abundance filtering

split.abund(cutoff=1)

Removes rare sequencing noise.

## Step 10 - Distance matrix

dist.seqs(cutoff=0.03)

Creates OTU-ready distance matrix.