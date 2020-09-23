<div align="center">

## About the "Compressing Files thru VB\(w/WinZip\)"


</div>

### Description

this is actually not a code but this is just a list of parameters to use WinZip in VB.. I hope this will help those who are interested in my previous posting namely: "Compressing Files thru VB(w/WinZip)"
 
### More Info
 
you have read my previous posting.. the "Compressing Files thru VB(w/WinZip)"


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Jaeger](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/jaeger.md)
**Level**          |Unknown
**User Rating**    |3.5 (28 globes from 8 users)
**Compatibility**  |VB 5\.0, VB 6\.0
**Category**       |[VB function enhancement](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/vb-function-enhancement__1-25.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/jaeger-about-the-compressing-files-thru-vb-w-winzip__1-4696/archive/master.zip)





### Source Code

```
Adding files:
The command format is:
winzip[32].exe [-min] action [options] filename[.zip] files
where:
-min specifies that WinZip should run minimized. If -min is specified,
it must be the first command line parameter.
action
-a for add, -f for freshen, -u for update, and -m for move. These
actions correspond to the actions described in the section titled
"Adding files to an Archive" in the online manual.
options
-r and -p correspond to the "Recurse Directories" and "Save Extra
Directory Info" checkboxes in the Add and Drop dialog boxes. -ex, -en,
-ef, -es, and -e0 options determine the compression method: eXtra,
Normal, Fast, Super fast, and no compression. The default is "Normal".
-s allows specification of a password. The password can be enclosed
in quotes, for example, -s"Secret Password". Note that passwords are
case-sensitive.
-hs option allows hidden and system files to be included.
filename.zip
Specifies the name of the ZIP involved. Be sure to use the full
filename (including the directory).
files
Is a list of one or more files, or the @ character followed by the
filename containing a list of files to add, one filename per line.
Wildcards (e.g. *.bak) are allowed.
Extracting Files:
The command format is:
winzip[32].exe -e [options] filename[.zip] directory
where:
-e Is required.
options
-o and -j stand for "Overwrite existing files without prompting" and
"Junk pathnames", respectively. Unless -j is specified, directory
information is used.
-s allows specification of a password. The password can be enclosed
in quotes, for example, -s"Secret Password". Note that passwords are
case-sensitive.
filename.zip
Specifies the name of the ZIP involved. Be sure to specify the full
filename (including the directory).
directory
Is the name of the directory to which the files are extracted. If the
directory does not exist it is created.
Notes:
* VERY IMPORTANT: Always specify complete filenames, including the full
path name and drive letter, for all file IDs.
* To run WinZip in a minimized inactive icon use the "-min" option.
When specified this option must be the first option.
* Only operations involving the built-in zip and unzip are supported.
* Enclose long filenames on the command line in quotes.
* NO leading or trailing blanks, or blank lines for readability, are
allowed in list ("@") files.
* The action and each option on the command line must be separated
from the others by at least one space.
* WinZip can be used to compress files with cc:Mail . Change the
compress= line in the [cc:Mail] section of the appropriate WMAIL.INI
files to specify the full path for WinZip followed by "-a %1 @%2".
For example, if WinZip is installed in your c:\winzip directory,
specify
compress=c:\winzip\winzip.exe -a %1 @%2
```

