># Conda commands
>
>## Command for creating the **qc** environment
>-First ensure you are on conda base
>then use the command `conda create -n qc`
>to enter the environment or activate it I used the command `conda activate qc`
>to confirm its existance use the command `conda list`.
>
>## Command for Installing **fastqc** and **multiqc** packages
>First you need to be in the environment you are installing the packages for instance I was in the qc environment.
>To install fastqc package I used the command `conda install -c conda-forge -c bioconda -c defaults fastqc`
>To install multiqc Iused the command `conda install -c conda-forge -c bioconda -c defaults multiqc`
>To confirm their existance I used the command `conda list`
>and to check the version of the packages I used the command `fastqc -v` and `multiqc -v` respectively.
