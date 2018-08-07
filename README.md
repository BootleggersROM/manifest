Bootleggers ROM | Pastafrola (Android Pie) sources
========

To initialize your local repository, use this command:

	repo init -u https://github.com/BootleggersROM/manifest.git -b pasta

Then, be sure to add your device manifest in your local_manifests folder and finally, do:

	repo sync -f --force-sync --no-clone-bundle -jx
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

Look, my device doesn't have flash, so i couldn't add and test the flash-required gestures and features. The same happens with Fingerprint stuff, so if you want to add tweaks, features or help me to optimize the ROM, you can make pull request and help me out, will be really appreciated.


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
* The Memedo Testers team