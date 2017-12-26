Bootleggers ROM
========

To initialize your local repository, use this command:

	repo init -u https://github.com/BootleggersROM/manifest.git -b oreo

Then, be sure to add your device manifest in your local_manifests folder and finally, do:

	repo sync -f --force-sync --no-clone-bundle -jx
	(the x on jx it's the amount of cores you have)

Also, just in case something went wrong for our side, or from your manifest or whatever, just add a `-q` in your repo sync command to see less lines and get into the issue more easily.

When everything is done, be sure to shishufy your device (prepare it with the bootleg.mk file and bootleg_device product and stuff, that generic thing) and then when you're ready you can:

	. build/envsetup.sh
	brunch bootleg_device
	
	(where it says device, it's your device codename)

Also, a sidenote: This is explained on the updater-script but just to clarify: Unshishufied builds are UNOFFICIAL.


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
* Resurrection Remix (Inspiration)
* AOSiP
* CrDroid
* CypherOS

Help the GZOSP Guys
-------------------

They've done a really stable source but you can help them to get it better!
To do this, you will need an account setup with our gerrit server and a changeid hooks.
To add the changeid hook in a project, use the following commands:

	cd <project>
	scp -p -P 29418 <username>@review.gzospgzr.com:hooks/commit-msg ${gitdir}/hooks/

You can also install the hook globally in all local GZOSP projects

	repo forall -c 'gitdir=$(git rev-parse --git-dir); scp -p -P 29418 <username>@review.gzospgzr.com:hooks/commit-msg ${gitdir}/hooks/'

Go have a coffee while this runs

You can send patches by using these commands:

    cd <project>
    git add --all
    git commit
    git push ssh://<username>@review.gzospgzr.com:29418/GZOSP/<project> HEAD:refs/for/<branch>

This will commit your changes into a single commit.
Make sure your git has the changeid hooks added.
If you are going to make extra additions, just repeat steps, but instead of

	git commit

use

	git commit --amend

Gerrit will recognize it as a new patchset.

To view the status of your and others patches, visit [GZOSP Code Review](http://review.gzospgzr.com)
