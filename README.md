# wyldTV releases

This repository publishes the signed **wyldTV** app for the TVs of family and friends (Android TV, Google TV, Fire TV). wyldTV is an IPTV player that brings no content: you add your own playlist.

Each [release](https://github.com/saschca/wyldTV-releases/releases) contains:

- `wyldtv-<version>.apk`: the app (also as `wyldtv.apk`, the same file under a fixed name for the first installation);
- `update.json`: what installed apps read to find out about a new version;
- `wyldtv-<version>-source.tar.gz`: the matching source code.

There is no source tree in this repository, and it does not take issues or pull requests.

## Install on a TV (first time)

1. On the TV, install the free **Downloader** app (by AFTVnews) from the TV's app store.
2. Allow Downloader to install apps: TV settings → *Apps* (Fire TV: *My Fire TV* → *Developer options*) → *Install unknown apps* → *Downloader* → on.
3. Open Downloader and enter this address, which always gives the newest version:

   `https://github.com/saschca/wyldTV-releases/releases/latest/download/wyldtv.apk`

4. Choose **Install**, then **Open**. Add your playlist in the app.

If the TV already has a wyldTV that was not installed from here, Android refuses the installation ("App not installed"). Uninstall the old one first (one time only; the playlist must then be entered again). After that, updates keep your setup.

## Updates

After the first installation, **updates arrive automatically**: the app checks for a new version about once a day and offers to install it. Your playlist, logins and settings stay.

## Source code and licence

wyldTV is free software under the **GNU General Public License version 3** (it is based on IPVIO Stream and includes the GPL-3.0 FFmpeg audio decoder). The complete corresponding source code of every version is attached to its release as `wyldtv-<version>-source.tar.gz`; the licence text is in the archive (`LICENSE`, `THIRD_PARTY_NOTICES.md`).

## For the maintainer

The **Release** workflow (Actions → Release → Run workflow) builds, signs and publishes a new version. It is a copy of `release/release.yml` from the private source repository, where it is reviewed; change it there first. The procedure is described in `docs/RELEASING.md` of the source repository.
