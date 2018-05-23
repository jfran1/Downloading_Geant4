# Setting up/Downloading Geant4
How to download and setup Geant4 on linux system

## Update Unbuntu 
1. **sudo apt-get update** 
2. **sudo apt-get upgrade**
3. **sudo apt-get install build-essential**

## Install CMake
* **sudo apt-get install build-essential**
## Make Programs Folder
* **mkdir Programs**

## Make Geant$ folder in Programs
1. **cd Programs**
2. **mkdir Geant4**

## get geant4 tar file and unpack in Geant4 directory

1. **cd Geant4**
2. **wget http://geant4.cern.ch/support/source/geant4.10.04.p01.tar.gz**
3. **with tar -xvzf the geant4.10.04.p01.tar.gz**

## Make build directory

* **mkdir geant4_build**

## Donwload some dependencies
* **sudo apt-get install libx11-dev libxt-dev libxmu-dev libgl1-mesa-dev mesa-common-dev mesa-utils-extra libglapi-mesa libqt4-opengl libqt4-opengl-dev qt4-qmake libqt4-dev libxi-dev libxerces-c-dev libexpat1-dev **

## run cmake inside build folder
1. **cd geant4_build**
2. **cmake -DCMAKE_INSTALL_PREFIX=../geant4.10.04.p01_install -DBUILD_STATIC_LIBS=ON -DGEANT4_BUILD_MULTITHREADED=ON -DGEANT4_USE_OPENGL_X11=ON -DGEANT4_USE_QT=ON -DGEANT4_INSTALL_DATA=ON -DGEANT4_USE_GDML=ON ../geant4.10.04.p01**

## Once complete run make and install
1. **make -jN** (where N is an integer representing the number of cores one wants to use)

after 

2. **make install -jN**
