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
