# asuswrt-merlin-mtgui — Releases

Public release mirror for [asuswrt-merlin-mtgui](https://github.com/shadow-enthusiast/asuswrt-merlin-mtgui).

Source code lives in a private repository. This repo exists only to host public release artifacts so the installer one-liner works from any router without authentication.

## Install on ASUS Merlin

```sh
wget -O /tmp/asuswrt-merlin-mtgui.tar.gz \
  https://github.com/shadow-enthusiast/asuswrt-merlin-mtgui-releases/releases/latest/download/asuswrt-merlin-mtgui.tar.gz && \
  tar -xzf /tmp/asuswrt-merlin-mtgui.tar.gz -C /jffs/addons && \
  sh /jffs/addons/mtgui/install.sh
```

## License

MIT
