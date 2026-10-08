# License supplements for the next release

Prepared 2026-10-08. These files supplement gaps in the immutable dev.4 notice
collection; they have not been inserted into its installer or runtime.

- FreeType 2.14.3: unchanged `FTL.TXT` and `LICENSE.TXT` from the exact upstream
  source archive referenced by the installed libfreetype6 build recipe.
  Proposed option: FTL, preserving the credit and per-file exceptions.
- gettext 0.22.5: unchanged `gettext-runtime/intl/COPYING.LIB` (LGPLv2.1) from
  the exact archive referenced by the installed libintl recipe. The candidate
  currently collected only `COPYING` (GPLv3) for that package.
- SQLite 3.53.4: the copyright-disclaimer/blessing comment from the shipped
  `Library/include/sqlite3.h`, closed as a standalone comment. This is an excerpt,
  not a newly selected license. See [SQLite's copyright statement](https://sqlite.org/copyright.html).

`provenance.json` records source URLs, source/member hashes and sizes. Both
downloaded source archives were SHA-256 verified against their cached package
recipes before selecting the texts. Archives and collection evidence remain in
the ignored build area; no SceneScope original source is in this supplement.

The missing-notice entries `libfreetype` and `vc` own zero shipped files in the
inspected runtime. They need inventory classification, rather than inventing
a license for a nonexistent binary. The actual FreeType DLL and Microsoft
runtime files remain subject to their applicable terms. These supplements do
not complete the full redistribution or corresponding-source review.

The subsequent source collection adds the unchanged full Graphite2 1.3.15 LICENSE
and Qt 6.11.2 GPLv3/LGPLv3/Qt GPL exception texts. See
`source-supplements-provenance.json`. Graphite's full text includes multiple
license choices and exceptions; its original COPYING notice is retained and a
per-file selection is still to be reconciled.

`vendor-supplements-provenance.json` records the missing OpenUSD 26.08 NOTICE
and the official Microsoft Visual C++ V14 2026 end-user contract. The latter is
kept as its original authoritative DOCX plus a paragraph-text extraction for
convenience. Its presence is not the publisher's redistribution grant: that
review additionally uses Community terms, redistributable file lists and SDK
terms. The OpenUSD LICENSE matches upstream byte-for-byte; MaterialX's exact
source license matches the collected text after newline decoding.

## Qt/Mesa/Microsoft continuation

The exact Qt/PySide notice ZIP contains 364 original files plus its hash and
attribution index; the Mesa/LLVM ZIP contains 14 upstream licensing/header files
plus its index. The new-candidate stager verifies both complete bundles and all
members, then extracts readable notices under `notices/qt-pyside/` and
`notices/mesa-llvm/`. Conservatively included source-only/platform-only material
is labeled; the collection is not a claim that every component is linked.

The 12.0.0-rc2 Mesa DLL matches Qt's recipe-pinned precompiled archive. LLVM's
embedded diagnostic identifies 3.6.2, whose original NCSA release license is
supplied separately too. The Mesa default MIT license is extracted from its
upstream licensing HTML; the original HTML, Khronos/C11 headers and LLVM embedded
notice files remain in the corresponding ZIP. No complete rebuilt Mesa DLL is
claimed. The SDK RTF is the original installed Microsoft license; its separately
labeled plain-text extraction is for convenient reading.

`qt-ms-supplements-provenance.json` pins all new files, source versions and exact
supplier-byte evidence. All 24 VC/OpenMP and 92 UCRT copies match their permitted
release x64 supplier files; Community/SDK publisher requirements remain applicable.
Installation media used for this comparison are not redistributed here.

## Verifier OpenSSL supplement, 2026-10-08

`OpenSSL-3.5.5-LICENSE.txt` is the original Apache-2.0 text from the OpenSSL
`openssl-3.5.5` tag. The installed cryptography 46.0.5 wheel reports
`OpenSSL 3.5.5 27 Jan 2026`. Its hash and URL are in
`verifier-supplements-provenance.json`. This addition does not close the remaining
Rust/libffi embedded-component review. The wheel's own licenses are retained
within the runtime and also copied into the central `notices/verifier/` folder.

`Verifier-46.0.5-notices.zip` contains 80 original legal files or labeled exact
legal-comment extracts, plus its hash/source index: five package license files,
68 files from all 36 checksum-verified Cargo.lock registry packages and seven
libffi legal header extracts from cffi's Windows x86/x64 source subset.
`Verifier-46.0.5-NOTICES.txt` is the readable UTF-8 concatenation. Both hashes
are pinned by `verifier-supplements-provenance.json`. Build-only/other-platform
crates are conservatively retained; this is not a historical wheel rebuild or
a claim that every crate is linked into the Windows binary.
