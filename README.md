<p align="center"><img src="imgs/logo.png" 
alt="GeCo3" width="300" height="260" border="0" /></p>
<b>Compress and analyze genomic sequences</b>. As a compression tool, GeCo3 is able to provide additional compression gains over several top specific tools, while as an analysis tool, GeCo3 is able to determine absolute measures, namely for many distance computations, and local measures, such as the information content contained in each element, providing a way to quantify and locate specific genomic events. 
GeCo3 can afford:
<ul>
<li>reference-free compression</li>
<li>referential compression</li>
<ul>
<li>relative compression</li>
<li>conditional compression</li>
</ul>
</ul>

## INSTALLATION ##

Cmake is needed for installation (http://www.cmake.org/). You can download it directly from http://www.cmake.org/cmake/resources/software.html or use an appropriate packet manager. In the following instructions we show the procedure to install, compile and run GeCo3:

### STEP 1

Download, install and resolve conflicts.

#### Linux 
<pre>
#sudo apt-get install cmake git
git clone https://github.com/pratas/geco3.git
cd geco3/src/
cmake .
make
</pre>

Alternatively, you can install (without cmake and only for linux) using

<pre>
wget https://github.com/pratas/GeCo3/archive/master.zip
unzip master.zip
cd GeCo3-master/src/
mv Makefile.linux Makefile
make
</pre>

#### OS X
Install brew:
<pre>
ruby -e "$(curl -fsSL https://raw.github.com/Homebrew/homebrew/go/install)"
</pre>
only if you do not have it. After type:
<pre>
brew install cmake
brew install wget
brew install gcc48
wget https://github.com/pratas/GeCo3/archive/master.zip
unzip master.zip
cd GeCo3-master/src/
cmake .
make
</pre>
With some versions you might need to create a link to cc or gcc (after the *brew install gcc48* command), namely
<pre>
sudo mv /usr/bin/gcc /usr/bin/gcc-old   # gcc backup
sudo mv /usr/bin/cc /usr/bin/cc-old     # cc backup
sudo ln -s /usr/bin/gcc-4.8 /usr/bin/gcc
sudo ln -s /usr/bin/gcc-4.8 /usr/bin/cc
</pre>
In some versions, the gcc48 is installed over /usr/local/bin, therefore you might need to substitute the last two commands by the following two:
<pre>
sudo ln -s /usr/local/bin/gcc-4.8 /usr/bin/gcc
sudo ln -s /usr/local/bin/gcc-4.8 /usr/bin/cc
</pre>

#### Windows

In windows use cygwin (https://www.cygwin.com/) and make sure that it is included in the installation: cmake, make, zcat, unzip, wget, tr, grep (and any dependencies). If you install the complete cygwin packet then all these will be installed. After, all steps will be the same as in Linux.

## EXECUTION

### Run GeCo3

Run GeCo3 using (lazy) level 5:

<pre>
./GeCo3 -v -l 5 File.seq
</pre>

## PARAMETERS

To see the possible options type
<pre>
./GeCo3
</pre>
or
<pre>
./GeCo3 -h
</pre>

If you are not interested in setting the template for each model, then use the levels mode. To see the possible levels type:
<pre>
./GeCo3 -s
</pre>

## CITATION ##

On using this software/method please cite:

D. Pratas, A. J. Pinho, P. J. S. G. Ferreira. Efficient compression of genomic sequences. Proc. of the Data Compression Conference, DCC-2016, Snowbird, UT, p. 231-240, March 2016.

## NEW FEATURES IN VERSION 3 ##

1. ...

## ISSUES ##

For any issue let us know at [issues link](https://github.com/pratas/GeCo3/issues).

## LICENSE ##

GPL v3.

For more information:
<pre>http://www.gnu.org/licenses/gpl-3.0.html</pre>

                                                    

