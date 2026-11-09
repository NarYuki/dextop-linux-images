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
