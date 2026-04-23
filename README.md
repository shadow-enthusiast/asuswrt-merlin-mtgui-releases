# asuswrt-merlin-mtgui — Release Mirror

Public mirror of release artifacts for **asuswrt-merlin-mtgui** — a Web UI
addon for [Asuswrt-Merlin](https://www.asuswrt-merlin.net/) routers that
installs and manages [mtg](https://github.com/9seconds/mtg), a lightweight
MTProto proxy for Telegram.

> Source code is in a private repository.
> This repo exists only so routers can fetch the install tarball without
> authentication.

## Install on ASUS Merlin

Run this on your router over SSH:

```sh
wget -O /tmp/asuswrt-merlin-mtgui.tar.gz \
  https://github.com/shadow-enthusiast/asuswrt-merlin-mtgui-releases/releases/latest/download/asuswrt-merlin-mtgui.tar.gz && \
  mkdir -p /jffs/addons && \
  tar -xzf /tmp/asuswrt-merlin-mtgui.tar.gz -C /jffs/addons && \
  sh /jffs/addons/mtgui/install.sh
```

After install:

- Open the **MTGUI** tab in the router Web UI (under VPN/Addons).
- Edit the config, set/generate a secret, save, then press **Restart**.
- Share the generated `tg://proxy` link or QR from the **Access** page.

## Supported routers

Any Asuswrt-Merlin device (384.15+ / 3006.102.1+) with Entware where mtg's
architecture matches:

- `aarch64` — RT-AX86U, RT-AX88U, GT-AX6000, GT-AX11000, RT-BE88U, …
- `armv7` — RT-AC86U, RT-AC68U
- `mipsle` / `mips` — best-effort for legacy devices

## Uninstall

```sh
/jffs/scripts/mtgui uninstall
rm -rf /jffs/addons/mtgui
```

## Releases

- Tagged releases (`vX.Y.Z`) are promoted to Latest.
- `vX.Y.Z-rc*` / `-beta*` / `-alpha*` tags are published as pre-releases.

## License

MIT — see the tarball for the full LICENSE file.
