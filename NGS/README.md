## create new env

```
conda create -n ngs python=3.9 scipy -y
```

## add conda channels

```
conda config --add channels defaults
conda config --add channels bioconda
conda config --add channels conda-forge
```

## install jupyter lab

```
conda install -y -c conda-forge jupyterlab
pip install jupyterlab_tabnine
```

## install packages needed for NGS analysis

```
conda install -y -c conda-forge pandas numpy matplotlib seaborn biopython openpyxl
conda install -y -c bioconda htseq minimap2 bwa bedtools flash trimmomatic picard pysam umi_tools fastp
conda install -y CRISPResso2
conda install -y fastqsplitter
```

## install parallel apply ext for pandas

```
pip install pandarallel
```

## add existing software to PATH

```
export PATH=/Users/awu/bin/samtools-1.15.1/bin:$PATH
export PATH=/Users/awu/bin/bcftools-1.15.1/bin:$PATH
export PATH=/Users/awu/bin/htslib-1.15.1/bin:$PATH
```
