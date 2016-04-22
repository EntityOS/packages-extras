### Calamares-entityos
--------
## Graphical installer for EntityOS ##
### Dependencies

Main:
* Compiler with C++11 support: GCC >= 4.9.0 or Clang >= 3.5.1
* CMake >= 2.8.12
* Qt >= 5.3
* yaml-cpp >= 0.5.1
* Python >= 3.3
* Boost.Python >= 1.55.0
* dmidecode

Modules:
* welcome:
 * NetworkManager
 * UPower
* partition:
 * extra-cmake-modules
 * KF5: KCoreAddons, KConfig, KI18n, KIconThemes, KIO, KService
 * KPMcore >= 2.1
 * sgdisk
* bootloader:
 * systemd-boot or GRUB
 * sgdisk
* unpackfs:
 * squashfs-tools
 * rsync

### Building
Clone Calamares from GitHub and `cd` into the calamares directory, then:
```
$ git submodule init
$ git submodule update
$ mkdir build
$ cd build
$ cmake -DCMAKE_BUILD_TYPE=Debug ..
$ make
```