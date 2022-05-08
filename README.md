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

