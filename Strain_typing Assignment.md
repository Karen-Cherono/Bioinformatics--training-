> # SRAIN TYPING
>
> Strain typing is a microbial characterization process that is used to distinguish members of the same species at the strain level.
> Multilocus sequence typing (MLST) is a technique in molecular biology for the typing of multiple loci, using DNA sequences of internal fragments of multiple housekeeping genes to characterize isolates of microbial species.
>
> ## Assignment
> ### Install mlst
>
> Firts I did create an environment and named it mlst i.e `conda create -n mlst` then installed mlst `conda install -c "bioconda/label/cf201901" mlst` to confirm its existance I used `conda list`.
>
> ### Download five *E.coli* sequences and do strain typing using mlst 
>
> I installed sratoolkit `sudo apt install sra-toolkit` then tried downloading the SRX files i.e `prefetch SRX22170666, SRX22170665, ERX1144545, SRA22024893, SRX22024889` but ran into errors since SRX files are not specified.
> I then used the same command `prefetch SRR26466680, SRR26466681, ERR12103628, SRR263166222, SRR26316626` and ran into errors. I tried using the `wget` to download the sequences. First I created a file called **multipledownloads.txt** i.e `touch multipledownloads.txt` then edited the file and added the links to the sequences in different lines i.e `nano multipledownloads.txt`. I then downloaded using `wget multipledownloads.txt` the command downloaded the three files but upon strain typing I ran into these error **_Unfamilar format with first line: <?xml version="1.0" encoding="utf-8"?>_**.
> I finally opted to download on windows assembled files and could now manipulate the data on the terminal.
> To run mlst, I activated the environment mlst i.e `conda activate mlst` then `mlst sequence.fasta.txt` the sequence.fasta.txt is the sequence I downloaded and these is the result I got **_sequence.fasta.txt      ecoli_achtman_4 3570    adk(6)  fumC(4) gyrB(12)        icd(1)  mdh(9)  purA(281)       recA(7)
[13:51:57] Thanks for using mlst, I hope you found it useful.
[13:51:57] Done._**.
>
> ### Create a loop that will loop through your sequences and give you one combined output and the output should only include sequence id and and strain type id i.e  ecoli_achtman_4 3570
>
> First i created a .sh file where i would create my loop i.e `touch mlstscript.sh`
> I then edited the file i.e `nano mlstscript.sh` and added my bash script.
>
> > A bash script is composed of two main lines and the first line is usually the shebang i.e # !/bin/bash or usr/bash depending on the type of bash you have. To confirm the type of bash you have you use the command `which bash`. The second line is your command or code.
> >` #! /bin/bash
for s in sequence.fasta.txt 1sequence.fasta.txt
do
mlst $s -q | cut -f2,3 >>1mlst_results.tsv
done`
> >
> > I used for loop in my script and my codes were `mlst $s -q` to run mlst on quiet mode then `cut -f2,3` to cut segreget only field two and three which are the sequence id and and strain type id then `>>1mlst_results.tsv` to redirect the output to the file imlst_results.tsv. These were the results
> >
> > sequence id strain type id
> > |..........|..............|
> > ecoli_achtman_4    3570
    ecoli_achtman_4    3570

> 
