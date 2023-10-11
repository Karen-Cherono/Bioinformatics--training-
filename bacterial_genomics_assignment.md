# **Generate a fastqc report from the downloaded file, assemble the genome and visualize using bandage.**

> I downloaded the file **SRR26270940.fastq.gz** an *E.coli* genome then i used the command  `gunzip SRR26270940.fastq.gz` in oder to access the file. The command decompresses a file.
> I then checked the contents of the directory to confirm wether the decompressed file exists i.e `ls` and the file **SRR26270940.fastq** now without the suffix gz was created.
> 
> I then navigated to the qc environment where fastqc was installed i.e  `conda activate qc` then used the command `fastqc SRR26270940.fastq` to generate a fastqc report for the *E.coli* genome.
> To confirm wether the fastqc report has been generated I did `ls` and **SRR26270940_fastqc.html** it was created. You can find the report here [fastqc report](file://wsl.localhost/Ubuntu-22.04/home/karencherono/SRR26270940_fastqc.html)
