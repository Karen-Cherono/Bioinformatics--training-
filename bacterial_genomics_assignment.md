># **Principle of nanopore sequensing and illumina sequencing**
>
>Nanopore sequencing is a technology that enables real-time analysis of long DNA or RNA fragments. It works by monitoring changes to an electrical current as nucleic acids are passed through a protein nanopore.The nitrogenous bases i.e thymine, adenine,guanine and cytosine distrupts the electrical current at different intensities The resulting signal is decoded to provide the specific DNA or RNA sequence.
>
>Illumina NGS technology uses the method sequencing by synthesis (SBS) technology – tracking the addition of labeled nucleotides as the DNA chain is copied. As DNA polymerase adds marked DNA nucleotides to the chain the specific bases will be used to get the sequence.
>
># **Install shovill, flye, Bandage and quast**
>
> I used the following commands to install the packages but first you need to create or navigate to the enviroment that the packages will 
  be installed i.e `conda create -n (name of the environment)` or `conda activate (name of the environment)`
>
> `conda install -c "bioconda/label/cf201901" shovill`
>
> `conda install -c "bioconda/label/cf201901" flye`
>
> `conda install -c "bioconda/label/cf201901" bandage`
>
> `conda install -c "bioconda/label/cf201901" quast `
>
># **Generate a fastqc report from the downloaded file, assemble the genome and visualize using bandage.**

> I downloaded the file **SRR26270940.fastq.gz** an *E.coli* genome then i used the command  `gunzip SRR26270940.fastq.gz` in order to access the file. The command decompresses a file.
> I then checked the contents of the directory to confirm wether the decompressed file exists i.e `ls` and the file **SRR26270940.fastq** now without the suffix gz was created.
> 
> I then navigated to the qc environment where fastqc was installed i.e  `conda activate qc`. Fastqc is a tool used as a quality control check on raw sequence data coming from high throughput sequensing pipelines. Then used the command `fastqc SRR26270940.fastq` to generate a fastqc report for the *E.coli* genome.
> To confirm wether the fastqc report has been generated I did `ls` and **SRR26270940_fastqc.html**  was created. You can find the link to the report here [fastqc report](\\wsl.localhost\Ubuntu-22.04\home\karencherono\SRR26270940_fastqc.html)
>
> Then i navigated to the environment where i installed flye i.e `conda activate flye`. Flye is a tool used to assemble long reads normally sequences from nanopore sequencing. I then used the command `flye --nano-raw SRR26270940.fastq -o SRR24415235.fasta` to assemble the genome. To confirm assembly I listed the contents of the directory and **SRR24415235.fasta** directory was created.
>
> To visualize my assembly I used the tool Bandage which is a tool for visualizing de novo assemblies. You can zoom into specific areas of the graph and interact with it by moving nodes, adding labels,changing colors and extracting sequences. I used the windows version that i downloaded from github and uploaded my file i.e **assembly_graph.gfa** from the **SRR24415235.fasta** directory.
>
> # **Reads, contigs, scaffolds and N 50**
>
> Reads are the smallest and the most basic unit of sequencing. They are short sequences obtained after next generation sequencing of fragmented DNA liblaries. If sequencing is done from one end of the read it is called single end read and paired end sequence reads from both sides.
>
> Contigs are assembled reads they are much larger than reads however not large enough to cover entire chromosomal DNA.
>
> Scaffolds are chained contigs, one scaffold should idearlly represent chromosomal DNA without any missing sequence information or gaps.
>
> N 50 is the sequence length of the shortest contig at 50% of total assembly length.
>
> # **Structure of the DNA**
> [DNA structure](https://www.google.com/url?sa=i&url=https%3A%2F%2Fkids.britannica.com%2Fstudents%2Farticle%2FDNA%2F398123&psig=AOvVaw0z1vOpfuHCZd2LvTpSo6Bk&ust=1697635451262000&source=images&cd=vfe&opi=89978449&ved=0CBEQjRxqFwoTCMDK4oKX_YEDFQAAAAAdAAAAABAR)
