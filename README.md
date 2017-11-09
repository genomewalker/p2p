# p2p

This repository contains the P2P course material for Wednesday and Friday.

## Wednesday

Tutorial for Wednesday: <https://github.com/genomewalker/p2p/wiki/Wednesday>

### File contents:

There are two main folders:

-   data: data used in the tutorials
    -   fastq: original reads after demultiplexing
    -   fastq_ac: reads after clipping the adapters
    -   fastq_merged: sequences after the read merging
    -   fastq_merged_bad: sequences after the read merging without restrictions
    -   fastq_qual_filt: sequences after filtering by the maximum number expected of errors
    -   fastq_qual_trim: sequences after trimming by Qscores
    -   fastq_qual_trim_filt: sequences after trimming by Qscores and filtering by the maximum number expected of errors
    -   fastqc_output: fastqc and multiqc output
    -   resources: Illumina adapters for bbduk.sh
-   figures: Plots created for the tutorial

## Friday

Tutorials for Friday:

-   [R crash course](https://rawgit.com/genomewalker/p2p/master/friday/P2P_r_crash_course.html)
-   [DADA2]((https://rawgit.com/genomewalker/p2p/master/friday/P2P_dada_intro.html))

First we will need to add `export https_proxy=http://webproxy:3128` to `~/.bashrc` with your favourite editor or in a terminal with:

```bash
echo "export https_proxy=http://webproxy:3128" >> ~/.bashrc
source ~/.bashrc
```

Once this is ready we can clone the repo if we already didn't do it. Open a terminal and go to your home directory and run this if it's the first time you are cloning the repository:

```bash
mkdir -p ~/thursday
cd ~/thursday
git clone https://github.com/genomewalker/p2p.git
```

And if you already cloned this repository run:

```bash
cd ~/thursday
git pull https://github.com/genomewalker/p2p.git
```

You can download a zipped file from [here](https://github.com/genomewalker/p2p/archive/master.zip). Save it in your home folder and rename it to **p2p**

```bash
cd ~/thursday
wget https://github.com/genomewalker/p2p/archive/master.zip
unzip p2p-master.zip
mv p2p-master p2p
```

We will follow the instructions from [here](https://github.com/genomewalker/p2p/wiki/Wednesday#getting-ready) and we will create a virtual environment where we are going to install R and some packages:

```bash
conda create -n R-3.4.1 r=3.4.1 rstudio r-devtools r-curl r-rjson r-rcpp r-tidyverse r-vegan bioconductor-dada2 bioconductor-phyloseq r-nycflights13 bioconductor-metagenomeseq r-ggrepel
```

Once everything is installed let's activate it:

```bash
source activate R-3.4.1
```

Now we will be able to start [**rstudio**](https://www.rstudio.com/) with:

```bash
cd ~/thursday/p2p/friday
rstudio &
```

### Other resources

GUide to STatistical Analysis in Microbial Ecology (GUSTA ME): <https://mb3is.megx.net/gustame>
