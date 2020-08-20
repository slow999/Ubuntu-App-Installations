# How to install Python 3.7 by using source file in Ubuntu


The motivation of this tutorial is that I got a few import error when I tried to run a Django project. I have to install the missing apt packages and recompile Python 3.7 since I install it through raw source file.
```
UserWarning: Could not import the lzma module. Your installed Python is incomplete
ImportError: No module named bz2
```

## What is source file?
1. At the bottom of Python 3.7.7 official page, there are three types of operating systems. They are source release, Mac OS X and Windows. Source file in Ubuntu is what we would consider .exe in Windows.
https://www.python.org/downloads/release/python-377/

2. Download source release "Gzipped source tarball".

3. Unzip file. We should get a "Python-3.7.7" folder.


## Installation
1.Start terminal and cd into the "Python-3.7.7" folder.

2.Run command below. The package would check a bunch of env and collect preps info. Let it finish.
```shell script
./configure
```

3.Run command below. The installation process will start compiling file and check maybe. Let it finish.
```shell script
make
```

4.Run command below. The installation process will start testing the compiled file for each package it needs. Keep an eye on the package you care the most. In my case, it would be bz2 and lzma. Both passed test.
```shell script
make test
```

5.Run command below.That will actually install Python executables in <strong>/user/local/bin</strong>, data files in <strong>/user/local/share/</strong>, etc.
```shell script
sudo make install
``` 

Done!

## Note
* The time I installed Python 3.7.7, system already has Python 3.7.2. In the end, it overwrites the old one rather than keep separate copy. The reason may be they both belong to version 3.7. In addition, all the virtual environments I created the time I was still using 3.7.2 are still working.
