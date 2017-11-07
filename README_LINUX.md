

## USING HSP2 on Linux and MacOS:
 
The major Python distributions (such as Enthought's Canopy and Anaconda) include version for Windows, Linux, and MacOS.  To use Linux, just download the 64-bit Linux distribution and if necessary use the package manager with your distribution to load the libraries such as pandas, numpy,  matplotlib, numba, etc.   For MacOS (and Linux to a lesser extent), you MUST use a distribution rather than going to the various Github sites and doing your own downloads to avoid messing up your operating system!
 
HDF5 files:   HDF was designed to run on many hardware architectures with significant internal differences (such as big endian vs. Little endian)  and many operating systems.  An HDF5 file can be moved without any changes between any machines supporting a reasonably modern version of HDF5.  For example a watershed model HDF5 file can be created on a Windows computer, moved to a Linux computer to execute, and then moved to a Mac computer to analyze the results without any "conversions".  So the HDF5 files in the tutorials will work in Linux.
 
Jupyter Notebooks: The Jupyter team works to maintain parity with most modern browsers (particularly Chrome, Firefox and IE/Edge). So any Notebook should be able to be opened on any computer in any major browsers.  In reality, since the browsers evolve independently, at any given time some browsers might have "quirks" that are a pain.  In general Chrome and Firefox are the most dependable on most operating systems.
 
The essential HSP2 core in the RESPEC HSPsquared Github site consists of the directories:
HSP2
HSP2 notebooks
HSP2 tools.
These core codes should work in both Python 2 and Python 3 on any machine without modification.
 
ALL the remaining directories are WINDOWS only to support the Tim Cera wdtoolbox, tstoolbox, and hspfbintoolbox. These are used to read legacy files into the HDF5 file.  In my early development I found some issues with these codes on Windows.
'Bugs' reported to Tim and acknowledged to be errors - but not fixed during my development cycle.
Failure to run.  Tim apparently developed these tools in a Linux  development environment and didn't test the Windows versions.  The Python distribution tools he used assumed that a  Fortran compiler was available on the Windows machine. Sometimes, he did release a precompiled file - but it still assumed that certain compiler DLLs were available at runtime.  So things always worked on my POD/RESPEC machine which had a full Microsoft development system and failed when Jason tried to use HSP2. So I made a collection of files with a bug patch and the missing DLLs together with a compatible release from Tim Cera.
I will be checking in the next few days to determine if these problems still exist.  If they now work, I will remove all of these files from the HSPsquared distribution.

## Python Packages (pip install):

* numpy
* pandas
* matplotlib
* numba
* ipython
* h5py
* networkx
* tables
* wdmtoolbox (also installed baker, tstoolbox)
* hspftoolbox

## Optional:

* HDF5 binary utilities from hdfgroup.org
