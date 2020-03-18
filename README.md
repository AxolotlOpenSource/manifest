![axolotl](https://i.imgur.com/1eP0RSm.png)

Getting Started Axolotl Open Source
---------------
You must be running a 64-bit Linux distribution and must have installed some packages to build
Axolotl Open Source. Google recommends using [Ubuntu](http://www.ubuntu.com/download/desktop) for
this and provides instructions for setting up the system (with Ubuntu-specific commands) on
[the Android Open Source Project website](https://source.android.com/source/initializing.html#setting-up-a-linux-build-environment).

To initialize your local repository using the XPerience CAF trees, use a command like this:

      $ mkdir ax
      $ cd ax
      $ repo init -u https://github.com/AxolotlOpenSource/manifest -b ax-Q
    
Then to sync up:

      repo sync -j<number_of_threads>
OR:

      repo sync --no-tags --no-clone-bundle --force-sync -c

--------

## Building Axolotl Open Source for your device

### Build Environment

- Tested and Working on any version of Ubuntu - 15.10 & 16.04 16.10 (64-bit)
- Any other distribution based of the Ubuntu Distro such as Lubuntu, Xubuntu and etc.
- A Terminal window
- A Good specs of hardware like 8 GB of RAM and an Intel I3 dual core (Minimum)
- A storage unit of any kind (minimum 100 GB). It would be better to use SSD because is more fast during the compliation process
- Some dependencies that should be installed

### [Dependencies for Linux](https://github.com/TheXPerienceProject/Manifest/wiki/Dependencies-for-Linux) or [Dependencies for Mac](https://github.com/TheXPerienceProject/Manifest/wiki/Dependencies-for-Mac)

### Building Axolotl Open Source ROM for your device
- Preparing Required Binaries and Device Drivers
- Set CCache for Faster Building (Optional)
- Build phase

### Set CCache
 
      $ sudo apt-get install ccache
      $ export USE_CCACHE=1
      $ export CCACHE_DIR=~/.ccache
      $ ccache -M 50G

Congratulations,the sources are initialized! 
	  
#### To build Axolotl Open Source ROM

The bundled builder tool `./rom-build.sh` handles all the building steps for the specified device
automatically. As the device value, you just feed it with the device codename (for example,
'Addison' for the Redmi Note 7).

      # Automatic script
      $ ./rom-build.sh codename
      # Example
      $ ./rom-build.sh lavender

#### OR
      
      # Manually
      $ . build/envsetup.sh
      $ lunch codename-userdebug #only if we support your device if not clone manually and do
      $ lunch xpe_codename-userdebug or breakfast codename
      $ make bacon -j$(nproc --all)

#### Credits to:

      * Android Open Source Project.
      * Cyanogenmod Team.
      * LineageOS
      * CodeAurora Forum
      * ParanoidAndroid (AOSPA)
      * The XPerience Project
      * And too much other's devs They do a lot for the community

      # bibliography:
      * http://tryge.com/2013/06/15/build-android-from-source-macosx/
      * https://source.android.com/source/initializing.html

## Copyright (C) 2018 The XPerience Project
## Copyright (C) 2020 Axolotl Open Source

Axolotl Logo is a mark of Axolotl Open Source

