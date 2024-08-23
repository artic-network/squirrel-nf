# squirrel-nf
Workflow to run [squirrel](https://github.com/aineniamh/squirrel) through a GUI

**S**ome **QUI**ck **R**earranging to **R**esolve **E**volutionary **L**inks

A full walkthrough of this workflow can be found [here](https://artic.network/mpxv/mpxv-phylogenetics-epi2me-sop.html)

Squirrel allows the following analyses of MPXV Clade I or Clade II sequences:
1. Generate an alignment 
2. Run basic sequence QC on the alignment looking for standard errors arising from consensus building pipelines or low sequencing depth
3. Build a phylogenetic tree
4. Build a phylogenetic tree and run additional sequence QC based on this phylogeny

When QC is performed, the pipeline produces a CSV file of suggested sites which are likely to be errors and should be masked. This file can be provided to a rerun of squirrel to improve the alignment.

## 1. Generate a quick MPXV alignment
Provide a FASTA file of consensus sequences and select the appropriate clade from the drop down menu.

## 2. Run basic sequence QC
If you check the `seq_qc` option, it will run additional QC

## 3. Build a phylogenetic tree
If you check the `run_phylo` option, it will construct a tree using IQtree. You will need to specify the outgroups (which need to be in the input FASTA file) and these are used to help root the phylogeny so that ancestral reconstruction can be performed in the appropriate direction.

## 4. Additional phylogenetic QC
If you check both the `run_phylo` and `seq_qc` options, and additional step is performed to generate a more informed mask file.

## More information
More information on the input parameters and methods can be found on [the main page for squirrel](https://github.com/aineniamh/squirrel).
