Uncompress zip files using p7zip
============================

We received a file from a collaborator in a zip format with a password. When I tried various approaches to unzipping it, I received the error "skipping: [filename]  need PK compat. v5.1 (can do v2.1 [or whatever, less than 5.1])

I was able to unzip the file with the following approach 

download from here to my osx laptop
-----------------------------------
    https://sourceforge.net/projects/p7zip/

uncompress
-----------------------------------
    p7zip_16.02_src_all.tar.bz2

make program
-----------------------------------
    cd ~/downloads/p7zip_16.02

    make

    make install

confirm install and check usage
-----------------------------------
    ~/downloads/p7zip_16.02/bin/7za

    
```
7-Zip (a) [64] 16.02 : Copyright (c) 1999-2016 Igor Pavlov : 2016-05-21

p7zip Version 16.02 (locale=en_US.UTF-8,Utf16=on,HugeFiles=on,64 bits,8 CPUs x64)



Usage: 7za <command> [<switches>...] <archive_name> [<file_names>...]

       [<@listfiles...>]



<Commands>

  a : Add files to archive

  b : Benchmark

  d : Delete files from archive

  e : Extract files from archive (without using directory names)

  h : Calculate hash values for files

  i : Show information about supported formats

  l : List contents of archive

  rn : Rename files in archive

  t : Test integrity of archive

  u : Update files to archive

  x : eXtract files with full paths
  ```

unzip archive
-----------------------------------
    ~/downloads/p7zip_16.02/bin/7za x [fileName].zip


    
```
7-Zip (a) [64] 16.02 : Copyright (c) 1999-2016 Igor Pavlov : 2016-05-21

p7zip Version 16.02 (locale=en_US.UTF-8,Utf16=on,HugeFiles=on,64 bits,8 CPUs x64)



Scanning the drive for archives:

1 file, 15617801 bytes (15 MiB)



Extracting archive: [fileName].zip

--

Path = [fileName].zip

Type = zip

Physical Size = 15617801



    

Enter password (will not be echoed):

Everything is Ok                                                              



Folders: 34

Files: 65

Size:       86842179

Compressed: 15617801
```
