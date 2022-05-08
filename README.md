# install-python3.8-on-ubuntu

# Installing Python 3.8 on Ubuntu with Apt 
Installing Python 3.8 on Ubuntu with apt is a relatively straightforward process and takes only a few minutes:

1. Run the following commands as root or user with sudo access to update the packages list and install the prerequisites:
```sh
sudo apt update
sudo apt install software-properties-common
```

2. Add the deadsnakes PPA to your system’s sources list:
```sh
sudo add-apt-repository ppa:deadsnakes/ppa
```

When prompted press Enter to continue:
```sh
Output
Press [ENTER] to continue or Ctrl-c to cancel adding it.
```

3. Once the repository is enabled, install Python 3.8 with:
```sh
sudo apt install python3.8
```

4. Verify that the installation was successfully by typing:
```sh
python3.8 --version
```

```sh
Output
Python 3.8.0
```

# Installing Python 3.8 on Ubuntu from Source
In this section, we’ll explain how to compile Python 3.8 from the source.

1. Update the packages list and install the packages necessary to build Python:
```sh 
sudo apt update
sudo apt install build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libreadline-dev libffi-dev libsqlite3-dev wget libbz2-dev
```

2. Download the latest release’s source code from the Python download page using wget :
```sh 
wget https://www.python.org/ftp/python/3.8.0/Python-3.8.0.tgz
```

3. When the download finishes, extract the gzipped archive :
```sh 
tar -xf Python-3.8.0.tgz
```

4. Switch to the Python source directory and execute the configure script which performs a number of checks to make sure all of the dependencies on your system are present:
```sh 
cd Python-3.8.0
./configure --enable-optimizations
```
The --enable-optimizations option optimizes the Python binary by running multiple tests. This makes the build process slower.

5. Start the Python 3.8 build process:
```sh 
make -j 8
```
For faster build time, modify the -j to correspond to the number of cores in your processor. You can find the number by typing nproc.

6. When the build process is complete, install the Python binaries by typing:
```sh
sudo make altinstall
```
Do not use the standard make install as it will overwrite the default system python3 binary.


7. That’s it. Python 3.8 has been installed and ready to be used. Verify it by typing:
```sh
python3.8 --version
```


