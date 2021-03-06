# RFdroid-scanparam

[![Build Status](https://travis-ci.org/bertrandmartel/rfdroid-scanparam.svg?branch=master)](https://travis-ci.org/bertrandmartel/rfdroid-scanparam)
[![License](http://badge.kloud51.com/pypi/l/html2text.svg)](LICENSE.md)

Modification of <a href="https://github.com/bertrandmartel/RFdroid">RFdroid application</a> to be used with a patched version of AOSP `frameworks/base` & `packages/apps/Bluetooth`. 

* This patch is working for API 21+ (tested on branch `android-5.1.1_r30`)
* The patch include addition of the following API : 

in `BluetoothAdapter.java` : 
```
public boolean startLeScan(final UUID[] serviceUuids, int scanIntervalMillis, int scanWindow, 
							final LeScanCallback callback) 
```

It can start a BLE scan with a specified scan interval and scan window

Patches can be found <a href="https://github.com/bertrandmartel/rfdroid-scanparam/blob/master/patch">here</a>

![screenshot](screen/screenshot.gif)

## Build

### Get code source

```
git clone git@github.com:bertrandmartel/rfdroid-ble-scanparam.git
cd rfdroid-ble-scanparam
```

### Build Android App

```
./gradlew clean build
```

## External projects

* BLE AD frame parser : https://github.com/TakahikoKawasaki/nv-bluetooth

* DiscreteSeekbar : https://github.com/AnderWeb/discreteSeekBar

* MPAndroidChart : https://github.com/PhilJay/MPAndroidChart

## License

```
Copyright (C) 2016  Bertrand Martel

This program is free software; you can redistribute it and/or
modify it under the terms of the GNU General Public License
as published by the Free Software Foundation; either version 3
of the License, or (at your option) any later version.

Foobar is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with Foobar.  If not, see <http://www.gnu.org/licenses/>.
```
