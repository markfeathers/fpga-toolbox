# FPGA toolchains

This project helps run FPGA tools within a toolbox to provide a supported docker 
environment.

# Install and setup PATH
```
git clone https://github.com/markfeathers/fpga-toolbox.git
cd fpga-toolbox/
echo "export PATH=\$PATH:$(realpath bin)" >> ~/.bashrc
```

# Lattice Diamond 

Download these from:
* diamond_3_12-base-240-2-x86_64-linux.rpm
  * https://www.latticesemi.com/en/FileExplorer?media={C8EC1946-4A21-44B6-AECC-33901F04B4D5}&document_id=53111
* diamond_3_12-sp1-454-2-x86_64-linux.rpm
  * https://www.latticesemi.com/FileExplorer?media={1FBB81AC-5C3E-442D-94E3-5E97303D7AD3}&document_id=53370

Copy both to lattice-diamond-3.12/

To build the toolbox, run:
```
# Will take ~5-10 minutes
make lattice-diamond-3.12
```
Install your license file to ~/.license.dat. Even though the container runs with a different mac address, the licensing tools seem to load them from /sys/ which will use your host's mac address.

To launch the tool run "diamond"
