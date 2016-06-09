MallowRom Github
===================

Build Environment
--------------------
- Official build environment as per Google and AOSP [Android source page](http://source.android.com/source/index.html)
- XDA user guides [Ubuntu 14.04 Trusty LTS](http://forum.xda-developers.com/showthread.php?t=2639611) , 
[Ubuntu 14.10 Utopic](http://forum.xda-developers.com/chef-central/android/howto-setup-ubuntu-14-10-utopic-unicorn-t2862442) , 
[Arch Linux](https://wiki.archlinux.org/index.php/android#Building_Android)

Initialize Source
--------------------
(Assuming you have a valid build environment setup)
- mkdir mallow (or whatever you want to name the source folder)
- cd ~/mallow
- repo init -u https://github.com/MallowRom/manifest.git -b mm

Sync Source
--------------------
- repo sync -jx -f (x being however many cpu jobs, you can also use -c to sync only the current branch specified by repo init)

Build Source
--------------------
- . build/envsetup.sh

Choose Device
--------------------
- lunch mallow_shamu-user

Clean Builds
--------------------
- cd ~/mallow
- repo sync -jx -f (x being however many cpu jobs, may also use -c as above)
- lunch and pick the right device (refer to above for choosing right device to build)
- make clean
- mka mallow
﻿
