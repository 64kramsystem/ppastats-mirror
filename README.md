# ppastats-mirror

Mirror of the [`ppastats` project](https://wpitchoune.net/ppastats), with patch required for compilation, and instructions for building.

I've prepared a PPA for the current Ubuntu LTS versions: https://launchpad.net/~saveriomiroddi/+archive/ubuntu/ppastats.

## Preparing a PPA via PPA Packaging tools

Prepareing the PPA packages using [PPA Packaging tools](https://github.com/saveriomiroddi/ppa_packaging), is trivial:

```sh
export PPA_PAK_VERSION='<fill>'
export PPA_PAK_PPA_ADDRESS='<fill>'
export PPA_PAK_EMAIL='<fill>'

export PPA_PAK_PACKAGE_NAME='ppastats'
export PPA_PAK_COPYRIGHT=gpl2
export PPA_PAK_DESCRIPTION='Command line tool which produces HTML report for viewing download statistics of an Ubuntu PPA'
export PPA_PAK_HOMEPAGE='https://wpitchoune.net/ppastats'
export PPA_PAK_SECTION='utils'

export PPA_PAK_BUILD_DEPS='pkg-config,libcurl-dev,libjson-c-dev'

git clone https://github.com/saveriomiroddi/ppastats-mirror.git

prepare_ppa_package ppastats-mirror
```
