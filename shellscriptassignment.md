>#USING `LS` COMMAND WITH DIFFERENT FLAGS
>## `ls -l`
>
>This will give you more details about your files.
>
 | File rights |directory name |date and time last edited | file name |
 | ----------- | ------------- | ------------------------ | ---------- |
 |-rw-r--r-- 1| karencherono karencherono|       323 Aug 16 15:21| 4sequences.fasta|
 |drwxr-xr-x 1| karencherono karencherono |     4096 Aug 15 16:10| BLUE-STATE-STATION|
 | -rw-r--r-- 1 |karencherono karencherono |103219356 Aug 16 16:45 |Miniconda3-latest-Linux-x86_64.sh|
 |drwxr-xr-x 1| karencherono karencherono|      4096 Aug 16 11:59 |cars|
 |-rw-r--r-- 1| karencherono karencherono|       102 Aug 16 15:06 |content.notes|
 |-rw-r--r-- 1| karencherono karencherono|        88 Aug 16 15:06 |content.txt|
 |-rwxr-xr-x 1| karencherono karencherono|        32 Aug 30 08:07|| hello.sh|
 |drwxr-xr-x 1| karencherono karencherono |     4096 Aug 16 11:05| karen-maintenance-charts|
 |-rw-r--r-- 1| karencherono karencherono|         0 Aug 16 15:42| karen-sequence.fasta|
 |-rw-r--r-- 1| karencherono karencherono |      109 Aug 16 15:11 |kc.txt|
 |drwxr-xr-x 1| karencherono karencherono |     4096 Aug 16 17:11| miniconda3||
 |-rw-r--r-- 1| karencherono karencherono |       19 Aug 16 15:24 |no.of-lines.fasta|
 |-rw-r--r-- 1| karencherono karencherono|        43 Aug 16 14:40| notes|
 |drwxr-xr-x 1| karencherono karencherono |     4096 Aug 29 16:26| projects|
 |-rw-r--r-- 1| karencherono karencherono|       824 Aug 16 14:52| seq.fasta|
 |-rw-r--r-- 1 |karencherono karencherono |        8 Aug 16 15:02| seq2.fasta|
 |drwxr-xr-x 1| karencherono karencherono|      4096 Aug 23 16:40 |shell-lesson-data|
 |-rw-r--r-- 1| karencherono karencherono |   460289 Aug 22 03:22| shell-lesson-data.zip|


>## `ls -a`
>This shows you all the files including the hidden or system files.
>
 | File rights | directory name | Date and time last edited | file name |
 | ----------- | -------------- | -------------------- | ------------- |
| drwxr-x--- 1 |karencherono karencherono|      4096 Aug 30 08:18| .|
| drwxr-xr-x 1 ||root         root       |       4096 Aug 14 20:55 |.|
| -rw------- 1 karencherono karencherono |     6025 Aug 23 17:48 |.bash_history|
| -rw-r--r-- 1| karencherono karencherono |      220 Aug 14 20:55 |.bash_logout|
| -rw-r--r-- 1| karencherono karencherono|      4278 Aug 16 16:52 |.bashrc|
| drwxr-xr-x 1 |karencherono karencherono |     4096 Aug 16 16:53| .cache|
| drwxr-xr-x 1 |karencherono karencherono |     4096 Aug 16 16:09| .conda|
| -rw-r--r-- 1| karencherono karencherono  |      52 Aug 22 16:52 |.condarc|
| drwxr-xr-x 1| karencherono karencherono |     4096 Aug 22 19:37| .java|
| -rw------- 1 |karencherono karencherono |       20 Aug 30 08:18| .lesshst|
| drwxr-xr-x 1 |karencherono karencherono |     4096 Aug 15 11:46| .local|
| -rw-r--r-- 1 |karencherono karencherono |        0 Aug 29 16:11| .motd_shown|
| -rw-r--r-- 1 |karencherono karencherono |      807 Aug 14 20:55 |.profile|
| -rw-r--r-- 1| karencherono karencherono|         0 Aug 23 15:45 |.sudo_as_admin_successful|
| -rw-r--r-- 1| karencherono karencherono |      165 Aug 23 15:42| .wget-hsts|
| -rw-r--r-- 1 |karencherono karencherono |      323 Aug 16 15:21| 4sequences.fasta|
| drwxr-xr-x 1 |karencherono karencherono |     4096 Aug 15 16:10| BLUE-STATE-STATION|


> # Using * and ? wildcard in the same sentence.
>
>First i navigated to the directory alkanes then i used the command `ls ????ane.*` to list any file with four characters before *ane* and with any extension.
> 
>  (base) karencherono@DESKTOP-OE8D2M1:~/shell-lesson-data/exercise-data/alkanes$ ls ????ane.*

> methane.pdb  
> pentane.pdb  
> propane.pdb
>
> # Use the wc -m and -w to get the total number of charchers and words and save the output in the file lengthsF.txt(the one you had creatd above)
>
> `wc -m *.pdb`
> 
1158 cubane.pdb

 622 ethane.pdb
 
 422 methane.pdb
 
1828 octane.pdb

1226 pentane.pdb

 825 propane.pdb
 
6081 total

> `wc -w *.pdb`
> 
 156 cubane.pdb
 
  84 ethane.pdb
  
  57 methane.pdb
  
 246 octane.pdb
 
 165 pentane.pdb
 
 111 propane.pdb
 
 819 total

 > # Use the -r flag to sort you file in reverse order and then use the -c to check if the file is sorted
>
>  `sort -r lengthsF.txt`
> 
  |107| total|
  |----|------|
  |30 |octane.pdb|
  |21 |pentane.pdb|
  |20 |cubane.pdb|
  |15 |propane.pdb|
  |12 |ethane.pdb|
  |9 |methane.pdb|

  > # `sort -c lengthsF.txt`
> 
sort: lengthsF.txt:2: disorder:   12 ethane.pdb

> # Use the word count command on the .pdb files to count the lines, then pipe you output to the sort command based on the numerical order and then pipe this into the head command to give you the first 3 rows/records and save it in a file called my_sortedOut.txt
>
>  `wc -l *.pdb | sort -n | head -3`
> 
   9 methane.pdb
   
  12 ethane.pdb
  
  15 propane.pdb

  > # Using the `cut` command cut only the year in cat animals.csv file i.e
>  `cat animals.csv`
> 
2012-11-05,deer,5

2012-11-05,rabbit,22

2012-11-05,raccoon,7

2012-11-06,rabbit,19

2012-11-06,deer,2

2012-11-06,fox,4

2012-11-07,rabbit,16

2012-11-07,bear,1

> 
> `cut -d "-" -f 1 animals.csv`
> 
2012
2012

2012
2012

2012
2012

2012
2012

> # Can you try this same loop but implement the continue statement i.e
> #Start of for loop
> 
`for a in 1 2 3 4 5 6 7 8 9 10

do

        # if a is equal to 5 break the loop
        
        if [ $a == 5 ]
        
        then
        
                break
                
        fi
        
        # Print the value
        
        echo "Iteration no $a"
        
done`


>
>  `for a in 1 2 3 4 5 6 7 8 9 10
>
> do
>
>         # if a is equal to 5 break the loop
>
>         if [ $a == 5 ]
>
>         then
>
>         continue
>
>           fi
>
>         # Print the value
>
>         echo "Iteration no $a"
>
> done`
> 
Iteration no 1

Iteration no 2

Iteration no 3

Iteration no 4

Iteration no 6

Iteration no 7

Iteration no 8

Iteration no 9

Iteration no 10


> # Write a for loop that echoes numbers 0 to 9
>
>  `for a in {0..9}
> 
> do
> 
> echo "Iteration no $a"
> 
> done`
> 
Iteration no 0

Iteration no 1

Iteration no 2

Iteration no 3

Iteration no 4

Iteration no 5

Iteration no 6

Iteration no 7

Iteration no 8

Iteration no 9
