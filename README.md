# p2p

This repository contains the P2P course material for Wednesday and Friday.

## Wednesday

Tutorial for Wednesday: https://github.com/genomewalker/p2p/wiki/Wednesday

### File contents:

There are two main folders:
- data: data used in the tutorials
 - fastq: original reads after demultiplexing
 - fastq_ac: reads after clipping the adapters
 - fastq_merged: sequences after the read merging
 - fastq_merged_bad: sequences after the read merging without restrictions
 - fastq_qual_filt: sequences after filtering by the maximum number expected of errors
 - fastq_qual_trim: sequences after trimming by Qscores
 - fastq_qual_trim_filt: sequences after trimming by Qscores and filtering by the maximum number expected of errors
 - fastqc_output: fastqc and multiqc output
 - resources: Illumina adapters for bbduk.sh
- figures: Plots created for the tutorial

## Friday
Tutorial for Friday: [here](https://cdn.rawgit.com/genomewalker/p2p/master/friday/P2P_r_crash_course.html)

Open a terminal and in your home directory run this if it's the first time you are cloning the repository:

```{bash}
git clone https://github.com/genomewalker/p2p.git
```

And if you already cloned this repository run:

```{bash}
git pull https://github.com/genomewalker/p2p.git
```
You can download a zipped file from [here](https://github.com/genomewalker/p2p/archive/master.zip). Save it in your home folder and rename it to **p2p**

```{bash}
unzip p2p-master.zip
mv p2p-master p2p
```

Once you have the folder ready we need to add the module system to your user:

```{bash}
/bioinf/software/Modules/default/bin/add.modules
source ~/.bash_profile
```

Now we will be able to start [**rstudio**](https://www.rstudio.com/) with:
```{bash}
rstudio &
```



