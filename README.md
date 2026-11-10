# Dextop Linux images

Prebuilt Debian images for [Dextop](https://github.com/NarYuki/Dextop)'s Linux feature.
Dextop downloads them on its own. Each image is arm64 and holds the base system, Mesa, Vulkan
drivers and the desktop. Language, fonts, input methods and applications are installed afterwards.

`manifest.json`, served from this repository's GitHub Pages, tells Dextop which image to use.
It is signed and Dextop verifies the signature and the image's SHA-256.

## Licenses and source

Images are made of Debian packages, DD-Turnip and the Materia-Manjaro-Dark IceWM theme
(GPL-3.0), each under its own license. Inside an image,
see `/usr/share/doc/<package>/copyright` and `/usr/share/doc/dextop-image/`.

Each release includes `*-sources.tar`: the complete corresponding source of that image, with
the scripts used to build it. To request the source another way, open an issue here.

## Current image

`20261110-1` includes GnuPG, gpg-agent, GPGSM and GTK pinentry in the base system.
The image is built on a Galaxy; Xvfb, llvmpipe, Turnip, GPG and Secret Service were tested there.
The release includes checksums, the installed package list and verification results.

The base build scripts are in `build/`. The source release also contains the exact finalization,
source refresh and validation scripts used for that release. Use a separate build directory;
never run them against a user's container. Signing requires the existing private key, which is
not part of this repository or any release.

Steam and other applications are installed later by Dextop. APK-side compatibility fixes require
an updated app; replacing a base image does not update existing user containers or the APK.
