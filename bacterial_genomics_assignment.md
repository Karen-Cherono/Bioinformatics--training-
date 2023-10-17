# **Generate a fastqc report from the downloaded file, assemble the genome and visualize using bandage.**

> I downloaded the file **SRR26270940.fastq.gz** an *E.coli* genome then i used the command  `gunzip SRR26270940.fastq.gz` in order to access the file. The command decompresses a file.
> I then checked the contents of the directory to confirm wether the decompressed file exists i.e `ls` and the file **SRR26270940.fastq** now without the suffix gz was created.
> 
> I then navigated to the qc environment where fastqc was installed i.e  `conda activate qc`. Fastqc is a tool used as a quality control check on raw sequence data coming from high throughput sequensing pipelines. Then used the command `fastqc SRR26270940.fastq` to generate a fastqc report for the *E.coli* genome.
> To confirm wether the fastqc report has been generated I did `ls` and **SRR26270940_fastqc.html**  was created. You can find the report here  [fastqc report](file://wsl.localhost/Ubuntu-22.04/home/karencherono/SRR26270940_fastqc.html)
>
> Then i navigated to the environment where i installed flye i.e `conda activate flye`. Flye is a tool used to assemble long reads normally sequenses from nanopore sequensing. I then used the command `flye --nano-raw SRR26270940.fastq -o SRR24415235.fasta` to assemble the genome. To confirm assembly I listed the contents of the directory and **SRR24415235.fasta** directory was created.
>
> To visualize my assembly I used the tool Bandage which is a tool for visualizing de novo assemlies. You can zoom into specific areas of the graph and interact with it by moving nodes, adding labels,changing colors and extracting sequenses. I used the windows version that i downloaded from github and uploaded my file i.e **assembly_graph.gfa** from the **SRR24415235.fasta** directory.
