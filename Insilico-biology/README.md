This is the part of my insilico tentame.\
This assignment is mixed with python scrypts and shell scripts

The casus:\
there are 4 genes where 1 one of genes is able to produce a heat resistance protein in the batch of a chemostat\
the question is which possible genes is it and what can is do?

As first is the suspected genome with the tool Augustes translated to protein sequences.\
where a python scrypt is used to get it in an usable fasta format.
To select the ones who are exstracellulair SingalP must be detected.\
Only SignalP can only handle one sequence at a time. so the fasta file created is parsed into mutliple files containing one protein sequence\
This is all combined in one python script and if an error occours. you will start where you left so no progress is lost (duration of python script is around 12 hours, it should be improved to send the job to the super cluster)

Due loads of files are created by SignalP, a pythons crypt was used to make a summary of it.


OrthoMCL is preformed to select all genes from the 4 species and group them together in the orthologue group.\
This is done by a shell script, who uses a tarzip of OrthoMCL containing all scripts

To gain all avaible knowledge about the proteins of the proteins HMM search is used with the HMM package. a shell script is used to preform this

a python script is used to generate a summary of OrthoMCL and HMM search for the requested gene ID of cellulose

![alt text](https://github.com/Dirowa/Python-scripts/blob/master/Insilico-biology/Pipeline_donny.png)

From these files is MUSCLE and RAXML shell command use to create a phylogenetic tree and a python script is used to generate a final table of all exstra cellular proteins who have cellulase funcion and are orphans of orthologue groups


