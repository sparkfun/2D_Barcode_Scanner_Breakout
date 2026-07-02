# SparkFun DE2290 Python Package Setup

The SparkFun DE2290 Python package helps streamline sending commands and receiving barcode data from the 2D Barcode Scanner Breakout. Install the `sparkfun-de2290d` Python package hosted by PyPi through a command interface or if you prefer to manually download and build the libraries from the [GitHub Repository](https://github.com/sparkfun/DE2290D_Py), 

## Installation

The Raspberry Pi OS should automatically install any necessary drivers for the 2D Barcode Scanner when it is connected and operating in USB-COM Mode. Find the USB-COM barcode on page 23 in the [Scan Settings Manual](/ref/DY%20SCAN%202D%20barcode%20scanner%20DE2290D.%20DE2290H%20setting%20manual.pdf) (the DE22900 defaults to USB-Keyboard mode) or scan it below:

<figure>
[![USB-COM Mode barcode from the Scan Settingss Manual](/img/USBCOM-Barcode.png)]
</figure>

### PyPi Installation

The DE2290 Py repository is hosted on PyPi as the `sparkfun-de22902` package. On systems that support PyPi, install the package via `pip3` (use `pip` for Python 2) using the following commands:

For **all users** (The user must have **[sudo](https://en.wikipedia.org/wiki/Sudo)** privileges):

``` bash
    sudo pip3 install sparkfun-DE2290
```

For the **current user**:

``` bash
    pip3 install sparkfun-DE2290
```
### Local Installation

Make sure to install the `setuptools` package on the system.

Direct installation at the command line (use `python` for Python 2):

``` bash
    python3 setup.py install
```    
Use the following command to build a package for use with `pip3`:

``` bash
    python3 steup.py sdist
```

A package file is built and placed in a subdirectory called dist. Install the package file using `pip3`.

``` bash
    cd dist
    pip3 install sparkfun_DE2290-<version>.tar.gz
```
### DE2290 Python Package Operation

For a full overview of how to use this package along with all the functions included with the DE2290 Py package, take a look at the [source code](https://github.com/sparkfun/DE2290D_Py/blob/main/de2290D_barcode_scanner.py).

### Upgrading the Python Package

If needed, the DE2290 Python package can be upgraded using the following commands:

For **all users**:

``` bash
    sudo pip3 install --upgrade sparkfun-DE2290
```

For the **current user**:

``` bash
    pip3 install --upgrade sparkfun-DE2290
```