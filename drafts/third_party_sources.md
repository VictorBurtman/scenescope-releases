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

The revised Qt/PySide notice ZIP contains 364 exact source legal/attribution
files and its hash/attribution index. The engineering scan covers all ten recipe
families, including qtimageformats, with 17,861 source license declarations and
95 attribution files describing 116 components. All seven previously failing
files are parsed according to Qt's newline convention; their original bytes and
all duplicate descriptive/version fields remain available. Two Shiboken PSF
license references are explicitly included. These counts describe the evidence,
not an assertion that all source components are linked into Windows binaries.

Mesa's separately precompiled `opengl32sw.dll` now matches the recipe-pinned Qt
archive byte-for-byte. Its embedded LLVM version is 3.6.2. Official upstream
version archives are also prepared for notice provenance:

| Archive | SHA-256 |
|---|---|
| mesa-12.0.0-rc2.tar.xz | 4fea2e873e8baf92cefa58695d4e719bcddb279c601077f0e7fafaed1259fbc0 |
| llvm-3.6.2.src.tar.xz | f60dc158bfda6822de167e87275848969f0558b3134892ff54fced87e4667b94 |

Mesa/LLVM are permissive components; their notice ZIP preserves the original
licenses and selected file headers. These upstream archives are not a claim of
a reproduced complete Qt Mesa build or an additional LGPL source obligation.
Microsoft SDK installation media used for the supplier-byte comparison are
private review evidence and are not part of the source-delivery assets.

## Additional source preparation after dev.6

The unchanged runtime identity also appears in dev.6. The systematic follow-up
prepares exact certificate/Python tool sources for MPL/vendored scope beyond
package metadata; these are local assets, not yet public links.

| Archive | SHA-256 |
|---|---|
| certifi-2026.7.22.tar.gz | 741e2c3b351ddf169a738da9f2c048608ff7f2c5cc02f1ebc6b118bb090d5d55 |
| certifi-2026.6.17.tar.gz | 024c88eeec92ca068db80f02b8b07c9cef7b9fe261d1d535abfd5abd6f6af432 |
| setuptools-84.0.0.tar.gz | f4695c21257f0d9b537ec2692c941d02ee143b7cc1276941349a546573b2ef73 |
| pip-26.2.1.tar.gz | f6ad667e89a1fe78046c8f13232b247200f5258d7828f3f7883d660878e0813f |

All hashes match PyPI. The conda certificate/setuptools/pip recipe pins also
match. Three delivered certificate PEM files and seven setuptools MPL-covered
schema/notice/Python files match their source members exactly. MPL-covered
editable files are already delivered in the runtime; their notices and rights
must be kept with the final distribution.

A complete `SceneScope-runtime-rt-2192364560b51c5afc8f7221-recipes.zip` is now
prepared for all 104 conda packages: 1,159 original recipe/build/patch files plus
index/instructions, SHA-256
`9742885f974588de7c3c434854107f952145333f09188d3ef092ae9546a63965`.
It supplements the earlier eight-component recipe package; it is not all
upstream sources or proof of every historical native build.

Rust standard-library notices additionally match the source commit observed in
cryptography's binary, Rust 1.93.0. The official std/compiler archive hashes and
original standard-library attribution catalogue are preserved in
`rust-stdlib-supplements-provenance.json`. Rust tooling itself is not shipped.
The verifier wheels match PyPI and 130 Python/stub/header files match their
sdists. A verified cryptography publish attestation identifies its upstream
publisher; it is not SLSA build provenance. Public source delivery remains open.

## Before publication

Reconcile the reviewed Qt/Mesa set, remaining native/resource scope, source/build
information and notices with the final runtime, then upload the corresponding source archives,
recipe ZIP and final notices beside the binary release. Fill in the verified
version-specific download links here and verify anonymous access. This document
does not substitute an email address or upstream homepage for source delivery.

Publisher/source enquiries: **Victor Burtman — victorburtman@gmail.com**.
