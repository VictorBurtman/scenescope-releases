# SceneScope third-party source preparation

Review draft, 2026-10-08. Local source assets are prepared for the dependencies
in the tested 0.1.0-dev.4 runtime. They are not yet downloadable release assets.
Original SceneScope application source remains proprietary and private.

The prepared set contains exact upstream sources for Qt 6.11.2, PySide/Shiboken
6.11.2, Graphite2 1.3.15, GLib 2.90.0, libiconv 1.18, gettext/libintl 0.22.5,
Cairo 1.18.6 and FreeType 2.14.3. Their package recipes, build scripts and patches
are included in a separate recipe ZIP, with a binary-to-source hash index.

Qt's archive matches the package recipe MD5 and the official SHA-256. PySide's
source comes from the exact package-recorded Git commit
`24627cd36e1593adf22eb1f2950e4248e7bcc1ec`; its archived tree has no submodules.
The remaining archive SHA-256 values match the exact package recipes. Available
mirrors are used only when the pinned content verifies, with TLS validation
enabled. Offline verification of all eight cached archives passes.

## Assets prepared locally

| Archive | SHA-256 |
|---|---|
| qt-everywhere-src-6.11.2.tar.xz | 6dcfbca271d76a6502741a2c0dc6fc98ef7dd0b7b4cfd0abcebb285a86a26f33 |
| pyside-setup-6.11.2-24627cd.tar.gz | b9ccbaba303eb6a471876cb21d7636bc7d24a360b6838d27cf4c8731e0982ecf |
| graphite2-1.3.15.tgz | c6bc8b4252724665297f7cad0c55897285c673f9b8e6db3522ace833593fe0b1 |
| glib-2.90.0.tar.xz | 17d15cac2af80a33271127408e0abc2748eb297c595c2a26409e81e14e7d1b8f |
| libiconv-1.18.tar.gz | 3b08f5f4f9b4eb82f151a7040bfd6fe6c6fb922efe4b1659c66ea933276965e8 |
| gettext-0.22.5.tar.xz | fe10c37353213d78a5b83d48af231e005c4da84db5ce88037d88355938259640 |
| cairo-1.18.6.tar.xz | 1c767308174337a74694da0f3ec069c271452163a1ef4540964c50c301f157d4 |
| freetype-2.14.3.tar.gz | e61b31ab26358b946e767ed7eb7f4bb2e507da1cfefeb7a8861ace7fd5c899a1 |

The recipe package also records the identities/hashes of the corresponding conda
binaries and each preserved recipe file. Follow the package's recorded Windows
build script, dependencies, variant configuration and patches after extracting
its upstream source. A successful rebuild of every library has not been performed.

The notice preparation ZIP contains 348 exact source notice/attribution files.
The Qt inspection covers the retained module families and records 17,808 source
license declarations and 93 attribution records. Seven attribution files require
manual reconciliation because their upstream JSON fails strict parsing; the
original files are preserved. These counts describe evidence, not a completed
license verdict for every shipped binary.

## Before publication

Complete the retained Qt tool/module and embedded-component review, including
the separately supplied Mesa/llvmpipe binary. Reconcile source/build information
and notices with the final runtime, then upload the corresponding source archives,
recipe ZIP and final notices beside the binary release. Fill in the verified
version-specific download links here and verify anonymous access. This document
does not substitute an email address or upstream homepage for source delivery.

Publisher/source enquiries: **Victor Burtman — victorburtman@gmail.com**.
