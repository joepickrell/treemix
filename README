Mirror of http://bitbucket.org/nygcresearch/treemix made on 5/22/2026

Quick installation:

./configure
make
make install

Full instructions and additional downloads available at:
http://bitbucket.org/nygcresearch/treemix


# TreeMix

Authors: JK Pickrell and JK Pritchard

TreeMix is a method for inferring the patterns of population splits and mixtures in the history of a set of populations. In the underlying model, the modern-day populations in a species are related to a common ancestor via a graph of ancestral populations. We use the allele frequencies in the modern populations to infer the structure of this graph.

The details of the TreeMix model are presented in:
Pickrell JK and Pritchard JK, [Inference of population splits and mixtures from genome-wide allele frequency data](http://www.plosgenetics.org/article/info%3Adoi%2F10.1371%2Fjournal.pgen.1002967).

Some extensions are presented in:
Pickrell JK, Patterson N, Barbieri C, Berthold F, Gerlach L, Güldemann T, Kure B, Mpoloka SW, Nakagawa H, Naumann C, Lipson M, Loh PR, Lachance J, Mountain J, Bustamante CD, Berger B, Tishkoff SA, Henn BM, Stoneking M, Reich D, Pakendorf B. [The genetic prehistory of southern Africa](http://www.ncbi.nlm.nih.gov/pubmed/23072811).

We describe an application of this model to looking for natural selection in humans and dogs at [Genomes Unzipped](http://www.genomesunzipped.org/2012/03/identifying-targets-of-natural-selection-in-human-and-dog-evolution.php).

## What's new:

### 11/22/16
TreeMix 1.13 released in the download section. 

- Merges a bugfix branch from Mikkel Schubert that fixes a compilation error many users were coming across. Many thanks to Mikkel for the fix!

### 6/18/14
- Transfer of codebase to Bitbucket
- Minimal changes to output of errors - errors start with 'ERROR' and warnings start with 'WARNING'.

### 6/5/13:
TreeMix 1.12 released.

- Fixes a bug that caused the reported relative likelihoods to be incomparable between trees and graphs. Many thanks to Mait Metspalu and Mike DeGiorgio for working through this.
- Also adds a -seed option for setting the random seed from the command line

### 11/20/12:
The TreeMix paper has been published in PLoS Genetics:
 
Pickrell JK and Pritchard JK, [Inference of population splits and mixtures from genome-wide allele frequency data](http://www.plosgenetics.org/article/info%3Adoi%2F10.1371%2Fjournal.pgen.1002967).

### 10/22/12:
Release of version 1.11.

- Fixes a bug that sometimes caused crashes when using microsatellite data

### 10/1/12:
Release of version 1.1.

- Allows input of microsatellite data. For a description of the microsatellite model, see downloads section on Bitbucket (pdf)
- Allows incorporation of known migration events
- Small other bug fixes

### 7/25/12:
Preprint: ["The genetic prehistory of southern Africa"](http://arxiv.org/abs/1207.5552) is available on arXiv. The new features in TreeMix described in this preprint will be available in the next release (estimated Sept. 2012).

### 5/24/12:
Release of version 1.04.

- Forces migration edges to have weight less than 0.5
- Include three- and four- population tests for treeness from [Reich et al. 2009](http://www.nature.com/nature/journal/v461/n7263/abs/nature08365.html) (programs are called threepop and fourpop, respectively)

To run threepop or fourpop, the input is standard TreeMix input. Then run (e.g.)

>threepop -i input.gz -k 500

This will print f3 statistics for all populations to stdout, and calculate standard errors in blocks of 500 SNPs. For example, running this on the test input files will give a set of output like:

```

Estimating f_3 in 59 blocks of size 500

total_nsnp 29999 nsnp 29999

Dai;Han,Sardinian 0.00112445 0.000276542 4.06609

Han;Sardinian,Dai 0.000536062 0.000211323 2.53669

Sardinian;Han,Dai 0.0289054 0.000867602 33.3165

```

The line Sardinian;Han,Dai 0.0289054 0.000867602 33.3165 tells you that f3(Sardinian;Han,Dai) is ~0.03, with a standard error of 0.0009, which corresponds to a z-score of 33. For information on how to interpret these tests, see Reich et al. (2009).

### 3/12/12:
Added a small script to convert stratified allele frequencies output from plink into TreeMix format. This will be incorporated into the next release, but for the moment must be downloaded separately. To run this, let's say you have data in plink format (e.g., data.bed, data.bim, data.fam) and a plink cluster file matching each individual to a population (data.clust).

Now you run:

>plink --bfile data --freq --missing --within data.clust

>gzip plink.frq

>plink2treemix.py plink.frq.gz treemix.frq.gz

The file treemix.frq.gz can now be used as input for TreeMix.

### Version 1.0.3:
- small bug fixes

### Version 1.0.2:
- removed an unnecessary header that sometimes caused compilation problems
- small big fixes

### Version 1.0.1:
- this is the first major release
