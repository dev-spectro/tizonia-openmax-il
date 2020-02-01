<a href="https://tizonia.org/">
    <img src="https://avatars2.githubusercontent.com/u/3161606?s=400&v=4" alt="Tizonia logo" title="The Tizonia Project" align="right" height="100" />
</a>

# The Tizonia Project

* A command-line streaming music client/server for Linux.
* Support for Spotify (Premium), Google Play Music (free and paid tiers), YouTube,
  SoundCloud, TuneIn Internet Radio, Plex servers and Chromecast devices.
* The first open-source implementation of [OpenMAX IL
  1.2](https://www.khronos.org/news/press/khronos-group-releases-openmax-il-1.2-provisional-specification).

---

<div align="center">
  <a href="https://travis-ci.org/tizonia/tizonia-openmax-il">
    <img src="https://travis-ci.org/tizonia/tizonia-openmax-il.png" />
  </a>

  <a href="https://scan.coverity.com/projects/594">
    <img src="https://scan.coverity.com/projects/594/badge.svg" />
  </a>

  <a href="https://codecov.io/gh/tizonia/tizonia-openmax-il">
    <img src="https://img.shields.io/codecov/c/github/tizonia/tizonia-openmax-il.svg" />
  </a>

  <a href="https://github.com/tizonia/tizonia-openmax-il/compare/v0.19.0...master">
    <img src="https://img.shields.io/github/commits-since/tizonia/tizonia-openmax-il/v0.19.0.svg" />
  </a>

</div>

<div align="center">

  <a href="https://www.codacy.com/app/tizonia/tizonia-openmax-il?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=tizonia/tizonia-openmax-il&amp;utm_campaign=Badge_Grade">
    <img src="https://api.codacy.com/project/badge/Grade/b002a7f1ba464093b48fb7c9620f8ae7" />
  </a>

  <a href="https://github.com/tizonia/tizonia-openmax-il/blob/master/COPYING.LESSER">
    <img src="https://img.shields.io/github/license/tizonia/tizonia-openmax-il.svg" />
  </a>

  <a href="https://bestpractices.coreinfrastructure.org/projects/1359">
    <img src="https://bestpractices.coreinfrastructure.org/projects/1359/badge" />
  </a>

</div>

<div align="center">

  <a href="https://gitter.im/tizonia/Lobby?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=body_badge">
    <img src="https://badges.gitter.im/tizonia/tizonia-openmax-il.svg" />
  </a>

  <a href="https://github.com/tizonia/tizonia-openmax-il/issues">
    <img src="https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat" />
  </a>

</div>


---


<div align="center">
  <img src="https://raw.githubusercontent.com/tizonia/tizonia-openmax-il/master/docs/animated-gifs/tizonia-usage-screencast.gif" />
</div>

<!-- [![](https://raw.githubusercontent.com/tizonia/tizonia-openmax-il/master/docs/animated-gifs/tizonia-usage-screencast2.gif)](https://raw.githubusercontent.com/tizonia/tizonia-openmax-il/master/docs/animated-gifs/tizonia-usage-screencast2.gif) -->

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->

- [News](#news)
- [Installation](#installation)
  - [Debian / Ubuntu / Raspbian](#debian--ubuntu--raspbian)
  - [Arch User Repository (AUR)](#arch-user-repository-aur)
  - [Snap Package](#snap-package)
  - [Docker Image](#docker-image)
  - [Configuration](#configuration)
  - [Upgrade (Debian / Ubuntu / Raspbian)](#upgrade-debian--ubuntu--raspbian)
- [Roadmap](#roadmap)
- [Resources](#resources)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# News

**Latest news**

- [2019-12-13] Tizonia
[v0.19.0](https://github.com/tizonia/tizonia-openmax-il/releases/tag/v0.19.0). Another
maintenance release with a good bunch of improvements and bug fixes: Dirble
removal (the service is sadly gone), Python 3 migration (please see the section
[Upgrade (Debian / Ubuntu / Raspbian)](#upgrade-debian--ubuntu--raspbian) to learn
how to install the new Python 3 dependencies!).

> NOTE: Please remember to also visit Tizonia's website at
> https://tizonia.org There is always some additional info on what is going on
> in the project and in the latest releases.

<details><summary><b>Show more</b></summary>

- [2019-03-13] Tizonia
[v0.18.0](https://github.com/tizonia/tizonia-openmax-il/releases/tag/v0.18.0). Various
improvements and bug fixes in Google Music and Spotify.

- [2019-01-17] Tizonia
[v0.17.0](https://github.com/tizonia/tizonia-openmax-il/releases/tag/v0.17.0). Fixed
Spotify login issues. A regression introduced in v0.16.0. This issue was
identified and fixed thanks to the great feedback provided by the users in
issue [#531](https://github.com/tizonia/tizonia-openmax-il/issues/531).

- [2018-12-03] Tizonia
[v0.16.0](https://github.com/tizonia/tizonia-openmax-il/releases/tag/v0.16.0). Improved
Spotify support with more options to dicover new music rather than just playing
the content that you know and love. Last but not least,
[docker-tizonia](https://hub.docker.com/r/tizonia/docker-tizonia/) has been
updated! (many thanks to [Josh5](https://github.com/Josh5)).

- [2018-06-15] Tizonia
[v0.15.0](https://github.com/tizonia/tizonia-openmax-il/releases/tag/v0.15.0). Reworked
Spotify support to overcome playlist search problems that arised in
libspotify. Now [spotipy](https://github.com/plamere/spotipy) is being used to
retrieve track, artist, album, and playlist metadata from Spotify.

- [2018-04-20] Tizonia
[v0.14.0](https://github.com/tizonia/tizonia-openmax-il/releases/tag/v0.14.0). Added
support for Google Play Music [stations for
non-subscribers](https://support.google.com/googleplaymusic/answer/6250894?hl=en)
and YouTube channels (uploads and playlists). Also added option to play the
user's entire Google Play Music library.

- [2017-12-28]
[Snap Package](#snap-package) and [Docker Image](#docker-image) available.

- [2017-08-26] [tizonia-all](https://aur.archlinux.org/packages/tizonia-all/) and [tizonia-all-git](https://aur.archlinux.org/packages/tizonia-all-git/) packages submitted to the [Arch User Repository](https://aur.archlinux.org/)

- [2017-05-04] [Summer of Code 2017: Add OpenMAX state tracker
in Mesa/Gallium that uses
Tizonia](https://summerofcode.withgoogle.com/projects/#4737166321123328) (X.Org
Foundation project, with Gurkirpal Singh and Julien Isorce).

</details>


# Installation

## Debian / Ubuntu / Raspbian

Debian packages for the latest release of Tizonia are available from
[Bintray](https://bintray.com/tizonia), with the following distro/arch
combinations:

<table>
    <thead>
        <tr>
            <th align="center">Ubuntu Xenial (16.04)</th>
            <th align="center">Ubuntu Bionic (18.04)</th>
            <th align="center">Debian Buster (10)</th>
            <th align="center">Debian Bullseye (11)</th>
            <th align="center">Raspbian Buster (10)</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td align="center">amd64</td>
            <td align="center">amd64, armhf</td>
            <td align="center">amd64, armhf</td>
            <td align="center">amd64</td>
            <td align="center">armhf</td>
        </tr>
    </tbody>
</table>

<!-- | [ ![](https://api.bintray.com/packages/tizonia/ubuntu/tizonia-xenial/images/download.svg) ](https://bintray.com/tizonia/ubuntu/tizonia-xenial/_latestVersion) | [ ![](https://api.bintray.com/packages/tizonia/ubuntu/tizonia-bionic/images/download.svg) ](https://bintray.com/tizonia/ubuntu/tizonia-bionic/_latestVersion) | [ ![](https://api.bintray.com/packages/tizonia/debian/tizonia-buster/images/download.svg) ](https://bintray.com/tizonia/debian/tizonia-buster/_latestVersion) | [ ![](https://api.bintray.com/packages/tizonia/raspbian/tizonia-buster/images/download.svg) ](https://bintray.com/tizonia/raspbian/tizonia-buster/_latestVersion) | [ ![](https://api.bintray.com/packages/tizonia/debian/tizonia-bullseye/images/download.svg) ](https://bintray.com/tizonia/debian/tizonia-bullseye/_latestVersion) | -->

> NOTE: Elementary OS, Linux Mint, Kali Linux are supported on releases based
> on Ubuntu 'Xenial' or 'Bionic', Debian 'Buster' or 'Bullseye'. To install
> Tizonia on other Debian or Ubuntu-based OSes, use the Snap package or have a
> look at [#631](https://github.com/tizonia/tizonia-openmax-il/issues/631).

Please note that the **recommended** way of installing Tizonia on a
Debian-compatible system is by running the following command:

```bash
$ curl -kL https://github.com/tizonia/tizonia-openmax-il/raw/master/tools/install.sh | bash
# Or its shortened version:
$ curl -kL https://goo.gl/Vu8qGR | bash
```

> NOTE: This script installs the
> [latest](https://github.com/tizonia/tizonia-openmax-il/releases/latest)
> release and all the dependencies. DISCLAIMER: trust no-one. Please have a
> look at the installation script before running it on your system!.


## Arch User Repository (AUR)

- [tizonia-all (for the latest released version)](https://aur.archlinux.org/packages/tizonia-all/)
- [tizonia-all-git (HEAD of master branch)](https://aur.archlinux.org/packages/tizonia-all-git/)

<details><summary><b>Show details</b></summary>

```bash
# Please note that if you are upgrading your existing
# Tizonia installation, you *need* to uninstall it before installing a new version.
# See GitHub issue https://github.com/tizonia/tizonia-openmax-il/issues/485

# For the latest stable release
$ git clone https://aur.archlinux.org/tizonia-all.git
$ cd tizonia-all
$ makepkg -si

# or for the bleeding edge
$ git clone https://aur.archlinux.org/tizonia-all-git.git
$ cd tizonia-all
$ makepkg -si

```

</details>


## Snap Package

A 'snap' package is now available to download from the 'Global' snap store
('stable' channel). For more details visit:

- Tizonia's landing page on [Snapcraft.io](https://snapcraft.io/tizonia)

<details><summary><b>Show details</b></summary>

To install, first visit [Install
Snapd](https://docs.snapcraft.io/core/install?_ga=2.41936226.1106178805.1514500852-128158267.1514500852)
and make sure that your Linux distro is supported. Follow the instructions
to get the 'snapd' service running on your system, and finally use this command
to install Tizonia:

```bash

$ sudo snap install tizonia

```

</details>


Tizonia's snapcraft.yaml file is hosted in its own repository:

- [tizonia-snap](https://github.com/tizonia/tizonia-snap/)


## Docker Image

Tizonia can also be run from a Docker container. A Docker image is available from the Docker hub:

- [docker-tizonia](https://hub.docker.com/r/tizonia/docker-tizonia/)

## Configuration

To use *Spotify*, *Google Play Music*, *SoundCloud* and *Plex* you need to
introduce your credentials in Tizonia's config file. No credentials needed to
stream from YouTube or TuneIn.

<details><summary><b>Show details</b></summary>

```bash
( On first use, Tizonia outputs its configuration file, if it is not there yet )

$ tizonia --help

( now edit $HOME/.config/tizonia/tizonia.conf )

( NOTE: If Tizonia was installed from the 'snap' package, use this path instead )
( $HOME/snap/tizonia/current/.config/tizonia/tizonia.conf )
```

> NOTE: see instructions inside this file for more information.

</details>


## Upgrade (Debian / Ubuntu / Raspbian)

To upgrade, simply re-run the installation script. This is the most convienent
way of upgrading the software and all its dependencies.

If you prefer to do it manually, it is a two-step process. Run 'apt-get' as
usual to upgrade the Debian packages, but also make sure that the various
Python dependencies are up-to-date.

<details><summary><b>Show details</b></summary>

```bash

# Step1: update Tizonia's Debian packages
$ sudo apt-get update && sudo apt-get upgrade

# Step2: update Tizonia's Python dependencies
# (Note that new versions of some of these Python dependencies are released often,
# so you should do this frequently, even if there isn't a new Tizonia release)

# For Tizonia v0.19.0 or newer: Python 3 dependencies
$ sudo -H pip3 install --upgrade gmusicapi soundcloud youtube-dl pafy pycountry titlecase pychromecast plexapi fuzzywuzzy eventlet python-Levenshtein && sudo -H pip3 install git+https://github.com/plamere/spotipy.git --upgrade

# For Tizonia v0.18.0 or older: Python 2 dependencies
$ sudo -H pip2 install --upgrade gmusicapi soundcloud youtube-dl pafy pycountry titlecase pychromecast plexapi fuzzywuzzy eventlet python-Levenshtein && sudo -H pip2 install git+https://github.com/plamere/spotipy.git --upgrade

```

</details>


# Roadmap

Roughly in priority order:

- REPL command-line interface.
- RPC interface / headless support ([#488](https://github.com/tizonia/tizonia-openmax-il/issues/488), [#509](https://github.com/tizonia/tizonia-openmax-il/issues/509), [#551](https://github.com/tizonia/tizonia-openmax-il/issues/551)).
- Pandora support ([#340](https://github.com/tizonia/tizonia-openmax-il/issues/340)).
- Airsonic/Subsonic support ([#496](https://github.com/tizonia/tizonia-openmax-il/issues/496)).
- Deezer support ([#498](https://github.com/tizonia/tizonia-openmax-il/issues/498))
- Tidal support ([#440](https://github.com/tizonia/tizonia-openmax-il/issues/440))
- OS X port ([#316](https://github.com/tizonia/tizonia-openmax-il/issues/316)).
- YouTube live streams ([#391](https://github.com/tizonia/tizonia-openmax-il/issues/391)).


# Resources

- See [PROJECT.md](PROJECT.md) to discover other facts about the project.
- See [CONTRIBUTING.md](CONTRIBUTING.md) to learn how to contribute to Tizonia.
- See [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) to keep Tizonia an open and welcoming environment.
- See [BUILDING.md](BUILDING.md) for instructions on how to build Tizonia from source (with the legacy Autotools build system).
- See [BUILDING_with_meson.md](BUILDING_with_meson.md) for instructions on how to build Tizonia from source (with the new Meson build system).
- See [docs.tizonia.org](https://docs.tizonia.org/) for the project's official documentation.
- The [Wiki](https://github.com/tizonia/tizonia-openmax-il/wiki) may also
contain some useful information (although in need of an update).
- See [CHANGELOG.md](CHANGELOG.md) for details on what has gone into each
release of the project.
- Tizonia OpenMAX IL is released under the [GNU Lesser General Public
License](COPYING.LESSER) version 3.

- Finally, please visit the project web site at https://tizonia.org
