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
This command outputs the files from at most n directory levels. This is useful to get a grasp of how big a certain directory is, which can then give you grasp of how much data you are dealing with, perhaps in a larger scale project. This can substitute the `-type d` command if you are trying just go into the folder at a certain depth.(Credit to ```man``` command)
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
* Here, the output is only the directories in the technical/ folder. The output does not give us any normal files since none exist in the first depth of the technical/ directory. The `-maxdepth 1` command is useful as it allows the user to specify how deep in the directory they'll want to search. This will output the folders 911report, biomed, government, and plos.

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
* Here, the output shows all files and folders that satify the depth of 2 within the technical/ directory. This time, it also includes files since some files are found within the 1 depth of folders. More folders (and .txt files) are shown within this `-maxdepth 2` command making it helpful for the user, searching for additional paths. This command outputs .txt files in the 911report, biomed, and plos folder.

## 3. ```find [path] -size [n][ckMGTP]```
This command outputs the files with that file size amount rounded up, the size amount is the second descriptor, give below:
            
             c       bytes
             k       kilobytes (1024 bytes)
             M       megabytes (1024 kilobytes)
             G       gigabytes (1024 megabytes)
             T       terabytes (1024 gigabytes)
             P       petabytes (1024 terabytes)


This is handy in cases where you are trying to find large files within a project that you may need to export. This may also allow to find smaller files that may or may not have anything in them, meaning they are not useful and are just taking up space which may be valuable in the long run of the project.(Credit to ```man``` command)

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
* Here, the output only shows files that are just 1 kilobyte. These files can then be said to not be large enough to matter and may thus not be contributing to a project as much as other files. It may be possible to delete these files in the plos/ directory which are the pmed files.

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
* Here, the output only gives files that are 2 kilobytes big which are within the government/ and plos/ directories, these files may be crucial in providing key data in cases such as Court cases, media outlet information and health information.

## 4. ```find [path] -iname [pattern]```
This command outputs the matched path but it is case insensitive. This can be used in cases where you are trying to find a specific name of a file which ignores the capitalization. This will enable a user to find more files without being too specific are what they are trying to find. Perhaps a user is trying to find all of the files that match a certain name while not wanting to worry about the casing. (Credit to ```man``` command)
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
* Here the output only shows files with plos in the name. It does not care about capitals. This is useful if trying to find all files with the same name that may have a different capital letter within the word.

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
* Here is the same seach with with Plos with a capital P. In this case, the same output is given since this is case insensitive. Although the difference is very slight, it is still present. It could be hard to tell at first, but that is what's interesting about the command.
