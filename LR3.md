# Lab Report 3: Researching ``find`` Command
## 1. ```find [path] -type [file type]```
This command outputs the files that are of the specificed file type (shown below) found from within the given path. This is useful in cases where you would want to find a lot of files, which you may have downloaded within a folder. Perhaps you can then find something from these files using a bash script. This allows the user to only tackle a certain type of files without running into problems if they try to edit or manipulate a file type that can't be manipulated just like a directory. (Credit to ```man``` command)

File Type Options:

             b       block special
             c       character special
             d       directory
             f       regular file
             l       symbolic link
             p       FIFO
             s       socket
             
### Example 1:
***
#### Input:
```
$ find technical/ -type d 
```
#### Output:
```
technical/
technical/911report
technical/biomed
technical/government
technical/government/About_LSC
technical/government/Alcohol_Problems
technical/government/Env_Prot_Agen
technical/government/Gen_Account_Office
technical/government/Media
technical/government/Post_Rate_Comm
technical/plos
```
* Here, only the paths shown are the ones in technical/ that are diretories. Thus, this only shows all folders inside the technical/ directory, as well as the folders inside folders. It will not show anything with .txt, .java, etc because they are files and not directories. 
* It is useful to look for directories in cases where you want to see how files are orgainized in a given space, for example here files are split among government files, 911 reports, Alcohol Problems, Meda, etc. You can then also see where to find specific files by narrowing down your search within directories.

### Example 2:
***
#### Input:
```
$ find technical/911report/ -type f
```
#### Output:
```
technical/911report/chapter-1.txt
technical/911report/chapter-10.txt
technical/911report/chapter-11.txt
technical/911report/chapter-12.txt
technical/911report/chapter-13.1.txt
technical/911report/chapter-13.2.txt
technical/911report/chapter-13.3.txt
technical/911report/chapter-13.4.txt
technical/911report/chapter-13.5.txt
technical/911report/chapter-2.txt
technical/911report/chapter-3.txt
technical/911report/chapter-5.txt
technical/911report/chapter-6.txt
technical/911report/chapter-7.txt
technical/911report/chapter-8.txt
technical/911report/chapter-9.txt
technical/911report/preface.txt
```
* Only paths to files in the technical/911report/ directory are shown here. Thus, this only shows all files inside the technical/911report/ directory, as well as the files inside folders. It will show anything that has .txt, .java, etc because they are files.
* Like stateed before this is useful if you are trying to run a bash script on a big load of files and need to isolate only the files with a directory. This can generalize file searches instead of searching for .java files, .txt files specifically. Here, you are specifically able to see the chapters in the 911report folder.

## 2. ```find [path] -maxdepth [n]```
This command outputs the files from at most n directory levels.(Credit to ```man``` command)
### Example 1:
***
#### Input:
```
$ find technical/ -maxdepth 1  
```
#### Output:
```
technical/
technical/911report
technical/biomed
technical/government
technical/plos
```
*

### Example 2:
***
#### Input:
```
$ find technical/ -maxdepth 2
```
#### Output:
```
technical/
technical/911report
technical/911report/chapter-1.txt
technical/911report/chapter-10.txt

...


technical/biomed
technical/biomed/1468-6708-3-1.txt
technical/biomed/1468-6708-3-10.txt
technical/biomed/1468-6708-3-3.txt
technical/biomed/1468-6708-3-4.txt
technical/biomed/1468-6708-3-7.txt


...


technical/plos
technical/plos/journal.pbio.0020001.txt
technical/plos/journal.pbio.0020010.txt
technical/plos/journal.pbio.0020012.txt

...

```

## 3. ```find [path] -size [n][ckMGTP]```
This command outputs the files with that file size amount rounded up, the size amount is the second descriptor, give below:
            
             c       bytes
             k       kilobytes (1024 bytes)
             M       megabytes (1024 kilobytes)
             G       gigabytes (1024 megabytes)
             T       terabytes (1024 gigabytes)
             P       petabytes (1024 terabytes)


(Credit to ```man``` command)

### Example 1:
***
#### Input:
```
$ find technical/ -size 1k
```
#### Output:
```
technical/plos/pmed.0020191.txt
technical/plos/pmed.0020226.txt
```

### Example 2:
***
#### Input:
```
$ find technical/ -size 2k
```
#### Output:
```
technical/government/Media/Campaign_Pays.txt
technical/government/Media/Court_Keeps_Judge_From.txt
technical/government/Media/Fire_Victims_Sue.txt
technical/government/Media/Helping_Hands.txt
technical/government/Media/It_Pays_to_Know.txt
technical/government/Media/Justice_requests.txt
technical/government/Media/Lawyer_Web_Survey.txt
technical/government/Media/Self-Help_Website.txt
technical/government/Media/Wilmington_lawyer.txt
technical/plos/pmed.0020028.txt
technical/plos/pmed.0020048.txt
technical/plos/pmed.0020082.txt
technical/plos/pmed.0020120.txt
technical/plos/pmed.0020157.txt
technical/plos/pmed.0020192.txt
```

## 4. ```find [path] -iname [pattern[]```
This command outputs the matched path but it is case insensitive.(Credit to ```man``` command)
### Example 1:
***
#### Input:
```
$ find technical/ -iname plos
```
#### Output:
```
technical/plos
```

### Example 2:
***
#### Input:
```
$ find technical/ -iname Plos
```
#### Output:
```
technical/plos
```

