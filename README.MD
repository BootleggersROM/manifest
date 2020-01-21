Bootleggers ROM | Queue (Android 10) sources
========

[![SF Downloads Badge](https://img.shields.io/sourceforge/dm/bootleggersrom.svg?color=e52c5f&label=Shishufied%20downloads&style=for-the-badge&labelColor=121217&logo=sourceforge)](https://sourceforge.net/projects/bootleggersrom/files/builds)
[![TG chat](https://img.shields.io/badge/Support-Telegram-%23e52c5f.svg?style=for-the-badge&logo=telegram&&labelColor=121217)](https://t.me/keepthebootleg)

To initialize your local repository, use this command:

	repo init -u https://github.com/BootleggersROM/manifest.git -b queso

Then, be sure to add your device manifest in your local_manifests folder and finally, do:

	repo sync --current-branch --force-sync --no-clone-bundle --no-tags --optimized-fetch --prune -jx
	(the x on jx it's the amount of cores you have)

Also, just in case something went wrong for our side, or from your manifest or whatever, just add a `-q` in your repo sync command to see less lines and get into the issue more easily.

When everything is done, be sure to shishufy your device (prepare it with the bootleg.mk file and bootleg_device product and stuff, that generic thing) and then when you're ready you can:

	source build/envsetup.sh
	lunch bootleg_device-userdebug
	mka bacon -jxxxxx
	
	(where it says device, it's your device codename. And you can use mka bacon ~~or mka bootleg~~, it's all up to you.)


Also, as another sidenote: This is explained on the updater-script but just to clarify: Unshishufied builds are UNOFFICIAL.


Help from other devices
-----------------------

If you got some commits missing for us, let us know on our telegram chat. Everything else, it's up to you at the time of building.


Thanks section
--------------
Here's my thanks to people who made this possible:

* Shishu (For being there)
* Ground Zero ROMs Team
* AOSPExtended
* ABC ROMs
* NitrogenOS
* AICP
* DirtyUnicorns
* Lukas Koller (Camera Roll dev)
* fxckingdeathwish (for the amazing photos for wallpaper/headers)
* OmniROM
* CyanogenMod/LineageOS
* PixelExperience
* PureNexus
* merothh
* Resurrection Remix
* AOSiP
* CrDroid
* CypherOS
* PureKat
* theimpulson
* MatiHalperin
* Project Xtended
* Pixeldust Project
* AquariOS
* Alejandro Ponce (Quetzal/Calypso dev)
* PixysOS 
* ArrowOS
* BlissROMs
* The Memedo Testers team