# Bluetooth-Beacon-Scanning-Setup
Instructions to get set up scanning Bluetooth Beacons with a Raspberry Pi *(As of 9/2/19)*

## Getting Started

### Check That Your Bluetooth Is On
- (This is the icon in the top left of the screen)

### Get Your Pi Up To Date
```shell
$ sudo apt update
$ sudo apt upgrade -y
$ sudo apt dist-upgrade -y
```

### Gattlib, Maybe?
- *I strongly suspect that, at this point, you can just skip this next bit and go straight to the beacontools setup.*
- *The gattlib requirements were leftover from another tool we had planned to use, I believe, and ultimately were not used. If I have the time, I want to try this setup again without installing any of this blue section, but in case one or two of these tools do turn out to be necessary, I've included this for safety.*
- OscarAcena's dependencies for pygattlib:
```shell
$ sudo apt install pkg-config
$ sudo apt install libbluetooth-dev
$ sudo apt install libboost-python-dev
$ sudo apt install libboost-thread-dev
$ sudo apt install libbluetooth-dev
$ sudo apt install libglib2.0-dev
$ sudo apt install python-dev
```
- I also did:
```shell
$ sudo apt install libboost-dev
$ sudo apt install bluez
$ sudo apt install python-bluez
$ pip install pybluez
$ pip install pybluez[ble]
$ sudo apt install mercurial ((this didn't seem to help))
$ sudo pip install gattlib ((this is freezing for long long time))
$ pip install beacontools[scan]
$ sudo apt install python-dev libcap2-bin
```

### Beacontools
- We want to avoid using pip on Debian, so we'll install beacontools from source:
- Download the beacontools master zip
- cd into extracted dir
```shell
$ sudo python setup.py install
```

