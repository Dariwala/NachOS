# NachOS
NachOS with new file system
- support file I/O system call 
```
int Create(char *name, int size);
OpenFileId Open(char *name);
int Read(char *buf, int size, OpenFileId id);
int Write(char *buf, int size, OpenFileId id);
int Close(OpenFileId id);
```
- support larger file size(Support up to 64MB single file)
- support subdirectory
- support recursive operations on directories
```
>nachos -lr <directory_to_be_listed>
```
Recursively list the file/directory in a directory. The Directory will always exist.
```
>nachos -rr <file/directory_to_be_removed>
```
Remove the file or recursively remove the directory.    
     
     
--------------
     

Building Instructions:
 * got to the directory build.<host>, where <host> is your working OS
 * do a "make depend" to build depenencies (DO IT!)
 * do a "make" to build NachOS

Usage:
see "nachos -u" for all command line options

Building and starting user-level programs in NachOS:
 * use Mips cross-compiler to build and link coff-binaries
 * use coff2noff to translate the binaries to the NachOS-format
 * start binary with nachos -x <path_to_file/file>
