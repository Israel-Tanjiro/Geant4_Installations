# Geant4_Installations
The following instructions are to install Geant4 10.7.4 in Ubuntu 22.04.3 LTS
We need some prerequisites and suggested packages to compile Geant4.
```bash
sudo apt install build-essential ninja-build pkg-config
libxerces-c-dev libexpat1-dev cmake git  wget zip unzip curl
openssl ca-certificates qtbase5-dev libqt5opengl5-dev libx11-dev libxmu-dev libgl1-mesa-glx qt3d5-dev libxcb-xkb-dev
```
```bash
sudo apt-get install build-essential libssl-dev
sudo apt install cmake-curses-gui
```
Now, donwload the geant4 source [version](https://geant4.web.cern.ch/download/10.7.4.html) 
untar using
tar xzvf geant4.10.7.4.tar.gz
go to the directory where geant4 is unpacked
cd geant4.10.7.4 
create the build directory 
mkdir build
go to the build directory
cd build
```bash
ccmake ..
```
you will see an figure like this.

press c to generate, If everthing is ok. Turn on the following options:
Select the directory where you want to install geant4, remember this path, you will need to install G4CMP
presee g, this is to configure, if you do not have errors.

```bash
make -j4
```




