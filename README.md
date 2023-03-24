# SpanishAcquisition-install

Instructions on how to install Spanish Acquisition on a new Windows computer. All files required for install are in the repo. Tested on Windows 10. If anything is not working, do not hesitate to email stephenharrigan2@gmail.com for help.

## Installing Spanish Acquisition

1.  Install python 2.7.18

    Windows 64 bit installer in "python" folder

    Note: If python 3 is/will be installed on your machine, do not add to PATH as this will cause problems.

2.  Add Swig folder to path
    Follow instructions "Add to the PATH on Windows 10". No installation is necessary, just add the folder to path.

2. Install the Visual C++ Redistributable for the machine

    https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170

3.  Install wxPython 3.0.2.0
    Run wxPython3.0-win64-3.0.2.0-py27 installer

    Note: This is a python package, but will not appear in "pip list" since it is not (and cannot be) installed by pip

4.  Install all python packages from requirements.txt

    Note: The versions of all the packages are important

    TODO: Figure out what version of "quantities" works.

5. Install the SpanishAcquisitionIQC repo from Github

    link: https://github.com/mainCSG/SpanishAcquisitionIQC

6. Install the repo

    This can be done by running 
    ```
    C:Python27\python setup.py install
    ```
    from the folder where the repo is located


At this point, you should be able to run Spanish Acquition. You can try it out by running
```
C:Python27\python .\examples\acquisition.py
```
from the folder where the repo is located. 

## Installing Drivers

However, you will not be able to communicate with many pieces of equipement because there aren't any equipement drivers. Fortunately, this part is quite straightforward since driver support for Windows is good.

1. Install NI MAX

    https://knowledge.ni.com/KnowledgeArticleDetails?id=kA03q000000YGQwCAO&l=en-CA

2. Install drivers necessary for system

    Note: I recommend you install all of them since it's quite simple and you don't want to add a new instrument later with a different driver and not understand why it isn't communicating properly.

    1. For USB-GPIB adapter: https://knowledge.ni.com/KnowledgeArticleDetails?id=kA03q000000YGw4CAG&l=en-CA
    
    2. For USB controller: https://www.ni.com/en-ca/support/downloads/drivers/download.ni-845x-driver-software.html#460629

    Ethernet connections do not require a driver to by installed by NI MAX