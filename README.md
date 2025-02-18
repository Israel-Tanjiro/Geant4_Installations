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
Now, donwload the geant4 source [version](https://geant4.web.cern.ch/download/10.7.4.html) . Using, after downloading the package
tar xzvf geant4.10.7.4.tar.gz
go to the directory where geant4 is unpacked
```
cd geant4.10.7.4
```
create the build directory 
```
mkdir build
```
go to the build directory
```
cd build
```
```bash
ccmake ..
```
you will see an figure like this.

![Workflow Diagram](Gean4_installation.png)


press c to generate, If everthing is ok.
Turn on the following options:
```
GEANT4_BUILD_MULTITHREAD  ON
GEANT4_INSTALL_DATA       ON
GEANT4_USE_OPENGL_X11     ON
GEANT4_USE_QT             ON
GEANT4_USE_RAYTRACER_X11  ON
GEANT4_USE_SYSTEM_EXPAT   ON
```


Select the directory where you want to install geant4, remember this path, you will need to install G4CMP
presee g, this is to configure, if you do not have any errors.

```bash
make -j4
```
After some minutes type
```bash
make install
```
Now checking that Geant4 was installed correctly
go to the path where you installed Geant4. Source the geant4 variables, this usually is in the following path /your_path/share/Gean4-10.7.4/geant4make/
```bash
source geant_env.sh
```
Go to the examples folder, and to the directory basic and B1 example.
Create the build directory
```bash
mkdir build
```
go to the build directory 
```bash
cd build
```
type 
```bash
cmake ..
```
later 
```bash
make
```
if you do not have error run the program 
```bash
./exampleB1
```
You will see something like this 
![Workflow Diagram](B1_example.png)











