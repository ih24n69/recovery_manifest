#Setting up a minimal tree for building TWRP
##Android 4.4 branch

[![Join the chat at https://gitter.im/marduk191/recovery_manifest](https://badges.gitter.im/marduk191/recovery_manifest.svg)](https://gitter.im/marduk191/recovery_manifest?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
This repo is ~2.6GB
###To initialize the main repository:

````
repo init -u https://github.com/ih24n69/recovery_manifest.git -b android-4.4
````
Then add anyrecovery/device trees/kernels you need to a file (one XML for each device) and add them to the .repo/local_manifests folder of your initialized repo folder.

Once added:
````
repo sync
````
Done

To build recovery:
````
. build/envsetup.sh
lunch (devicename)
make installclean
time make recoveryimage
````


Devices tested:

````
Pantech Burst p9070 (presto)
HTC Desire 610 (a3ul)
````
