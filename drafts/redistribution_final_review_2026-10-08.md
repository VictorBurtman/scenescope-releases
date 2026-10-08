# Completed embedded-dependency engineering review

Date: 2026-10-08. The local licence, notice and source assessment is complete for
the dependencies in immutable **SceneScope 0.1.0-dev.6**, runtime
`rt-2192364560b51c5afc8f7221`. This conclusion uses the prepared supplements;
those additions are not inside the existing dev.6 installer. Publication still
requires a new installer with these documents and actual public source delivery.
The owner explicitly defers acceptance on another PC. That test is separate
from the dependency review and does not prevent its completion.

The [104-package decision matrix](redistribution_dependency_matrix_2026-10-08.json)
records binary/source identities, selected terms, exceptions, original notice
hashes and a decision for every package. The
[final source lock](redistribution_source_lock_final_2026-10-08.json) records 81
source declarations, including separately pinned archives for one project and
conservative source-only/platform inputs. These counts describe review coverage,
not 81 libraries loaded by SceneScope.

## Closed questions

- All **42,946** indexed runtime files pass the existing fingerprint audit.
  All **42,658** available installed-package hashes match; 5,278 omitted paths
  are explained by bytecode/PDB/cache staging filters. The 114 cached original
  notice copies match. Empty TBB-devel metadata is resolved by actual notices;
  metadata-only packages and SQLite/FreeType exceptions have explicit decisions.
- All six generated pip/pip3/wheel files are now reconciled. The three 74,752-byte
  EXEs match the complete byte array in Mamba 2.9.0 commit
  `2676ec2050f7dd5b8a524287526f50a8a4fb9652`, SHA-256
  `28b001bb9a72ae7a24242bfab248d767a1ac5dec981c672a3944f7a072375e9a`.
  The three Python scripts exactly match its entry-point template and recorded
  shebang. The supplier identifies the CPython/conda-build launcher source.
  Vinay Sajip/PSF, conda-build and Mamba credits are retained, with conservative
  MinGW/GCC runtime texts. This is exact supplier-byte/template reconciliation;
  it does not establish a historical compiler rebuild.
- Native upstream sources are verified against actual recorded recipe hashes
  or Git revisions. OpenUSD 26.08's **TOST-1.0** text controls over Apache package
  metadata, as does OpenSubdiv's actual TOST text. Full NOTICE/THIRD-PARTY files
  and embedded utility, image, XML, font and hash-code attributions are retained.
  MaterialX's exact Git revision, OIIO/OCIO, OpenEXR/OpenVDB, Embree, LLVM,
  compression/image/font libraries and their patch inputs are covered.
- Graphite2's exact 1.3.15 LICENSE expressly offers **MIT**, despite older
  COPYING/metadata; that option is selected for the library. FreeType selects
  FTL and retains its nine complete exceptions and credit. Cairo selects the
  LGPL branch; GLib/libiconv/libintl retain matching library source and patches.
  GPL CI/test/gettext tools and XZ scripts are distinguished from the actual
  shipped libraries/helpers. Qt's prior 70-target matrix and full source apply
  to its independent GPL tooling and the application's LGPL stack. The DBus
  alternate AFL-2.1 text is already in the Qt supplement.
- The complete IJG **README.ijg** is now retained in addition to libjpeg-turbo's
  general LICENSE.md. libultrahdr's original **Adobe Gain Map NOTICE** and
  image_io/modp_b64 notices are retained. LLVM support/BLAKE3/regex/ITT and
  MinGW runtime/winpthreads notices are accounted for separately.
- All 13 unmodified Ubuntu font files match Canonical's 0.83 source tar.
  The recipe ZIP endpoint is unavailable; the alternative upstream archive is
  explicitly labelled and separately hashed, rather than assigned the ZIP's
  checksum. Other fonts retain OFL/Bitstream/DejaVu terms and reserved names.
- Intel MKL remains in unmodified binary form with its complete October 2022
  Simplified Software License and third-party text. Its bundled grant permits
  use/redistribution with notice, no-modification/reverse-engineering and
  non-endorsement conditions. The general Intel developer-tools EULA is not
  substituted for those package-specific terms. All Microsoft runtime copies
  retain the separately established permitted-file and publisher entitlement
  evidence and recipient protections.
- Previous verifier evidence closes its package/embedded scope: 148 original
  wheel members and 130 comparable source members match; cryptography's publish
  attestation verifies and altered bytes fail. Exact Cargo.lock crates, Windows
  libffi comments, OpenSSL 3.5.5 and identified Rust 1.93.0 standard-library
  attributions are retained. This is not a historical wheel rebuild attestation.
- Alembic/Imath/Boost.Python, modified AbcView, ufbx/VDB bridges, original assets,
  reproduced HDRIs/MaterialX presets and MIT theme tokens retain the prior exact
  native/resource evidence. Nuitka supplier runtime comments are supplemented
  without copying generated SceneScope C. The installer selects **NSIS zlib**
  and nsExec, with the original NSIS licence; NSIS LZMA is not selected.

## Prepared final notices

`license_supplements/Native-runtime-rt-2192364560b51c5afc8f7221-notices.zip`
preserves **15,406** unique original legal documents/comment blocks with source
archive/file hashes and exact byte offsets for extracts. The collection is
conservative and does not assert every source file is linked into Windows.
Tests, documentation toolchains and unrelated LLVM tools are excluded from
runtime attribution selection; the complete source catalogue remains local.
Deduplication preserves exact bytes. Standard Apache/Boost SPDX references are
covered by their complete terms; embedded permissive copyright/permission blocks
remain supplied. The collection adds to, rather than replaces, the existing
Qt/Mesa/runtime/verifier/Rust bundles.

The ZIP has **12,345,076 bytes**, SHA-256
`0d8c60e4f2de86797a10c9ac0f582264a9f3aaca4bb6b280e576d604ec9a77fa`;
its 23,779,837 expanded bytes stay below the stager's 32 MiB limit. Nine readable
UTF-8 parts each stay below the offline reader's 2 MiB document limit. Native
catalogues remain archived to avoid adding thousands of loose installation files.
All originals are still accessible in the ZIP and matching indexed sources.
`native-runtime-supplements-provenance.json` pins every asset.

The stager now verifies the complete supplement manifest, rejects missing,
altered, unregistered or linked assets, and verifies every ZIP member before
copying prepared notices. Existing Qt/Mesa readable extraction is retained;
new archived catalogues use their bounded readable text parts. Historical dev.6
bytes, hashes, identities and release flags remain unchanged.

Validation passes: seven notice-staging checks (including archived member
tampering and missing/extra assets), three payload-audit regressions, all 44
supplement files copied byte-for-byte, and all nine new documents fully readable
in both English and French interfaces (**18** reader checks). Every indexed ZIP
member and all 81 source archives are verified. A final independent runtime
fingerprint audit passes again, and the dev.6 installer SHA-256 remains unchanged.
Hashes are generated after Git newline normalization of maintained JSON/Markdown;
original vendor text/ZIP bytes are preserved by their existing attributes.
Evidence: `final-validation.json`, `generated-launcher-reconciliation.json`,
`source-catalogue.json` and `final-payload-audit/` under the final review directory.
These targeted checks do not replace dev.6's historical 450-test compiled build
or the future new-installer/external-PC acceptance.

## What remains before publication

1. Build a new application version/installer carrying all final terms, notices,
   source instructions and hashes; repeat affected compiled and installed reader/
   ownership/integrity checks. The old dev.6 installer is not the final notice set.
2. Deliver the matching LGPL/GPL/MPL sources and recipe/build/patch inputs as
   actual release assets with verified anonymous URLs alongside the binaries.
   Local archives or upstream homepages alone do not fulfil this delivery gate.
3. Receive the owner's later clean-PC/offline/other-GPU acceptance and settle the
   production signing/update trust policy. Preference testing remains deferred.
4. Publish GitHub/Gumroad last and verify anonymous downloads and checksums.

There is no remaining unidentified dependency supplier or licence-text question
in this local assessment. These delivery/acceptance steps remain open; the
assessment is not an assertion that dev.6 is already distributable, a historical
rebuild of every vendor binary, or a change to the proprietary application's
licence. Source and preparation repositories remain private.

Evidence: `build/distribution/dependency-final-review-2026-10-08/`, plus the
earlier payload/Qt/Microsoft/native/verifier review directories. Primary source
texts include [Mamba's launcher supplier](https://github.com/mamba-org/mamba/blob/2.9.0/libmamba/data/conda_exe.hpp),
[OpenUSD terms](https://github.com/PixarAnimationStudios/OpenUSD/blob/v26.08/LICENSE.txt),
[OpenSubdiv terms](https://github.com/PixarAnimationStudios/OpenSubdiv/blob/v3_7_0/LICENSE.txt),
[Intel's identification of the controlling bundled terms](https://www.intel.com/content/www/us/en/developer/articles/license/end-user-license-agreement.html)
and [NSIS licence/component exceptions](https://nsis.sourceforge.io/Docs/AppendixI.html).
