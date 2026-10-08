# SceneScope third-party notices and library replacement

Final prepared notice index, 2026-10-08, based on **0.1.0-dev.6** with runtime
**rt-2192364560b51c5afc8f7221**. The local dependency engineering assessment is
complete with the final supplements. Those additions require a new installer;
existing dev.6 and the public source-delivery gate remain unchanged.
The final release must carry the full applicable license texts, attributions,
corresponding sources and verified instructions for its actual payload.

Publisher and source enquiries: **Victor Burtman — victorburtman@gmail.com**.
SceneScope's application terms apply to its original code. Third-party licenses
govern the components below and take precedence for those components.

## Principal components

| Component | Observed version | License / notice location in the candidate |
|---|---|---|
| Qt / PySide / Shiboken | 6.11.2 | SceneScope uses the LGPLv3 Widgets/OpenGL stack. Independent Designer/QmlCompiler/tooling components retain GPLv3/Qt exception terms; embedded components have additional terms. Readable full-source notices and attributions are prepared under `notices/qt-pyside/`, alongside the original conda notices and full Qt/PySide sources/recipes. |
| OpenUSD, usdview and Storm | 26.08 | Upstream TOST-1.0 and embedded third-party terms; preserve the complete upstream license and applicable NOTICE. `notices/conda/openusd-*/`. |
| MaterialX | 1.39.5 | Complete upstream license and embedded third-party notices. `notices/conda/materialx-*/`. |
| Python | 3.11.16 | Python/PSF and bundled-library terms. `notices/conda/python-*/`. |
| PyOpenGL | 3.1.10 | BSD-style terms. `notices/conda/pyopengl-*/`. |
| oneTBB / OpenSubdiv | 2022.3.0 / 3.7.0 | Complete licenses and third-party notices in their conda notice folders. |
| NumPy / Intel MKL | 2.4.6 / 2025.3.1 | NumPy BSD terms and Intel/other applicable notices in their conda notice folders. |
| Alembic / Imath / Boost / adapted AbcOpenGL | 1.8.12 / 3.2.2 / 1.91 / upstream adaptation | Full applicable upstream notices and modification provenance. `notices/alembic/`. |
| ufbx | 0.23.0 | MIT option; copyright and permission notice with upstream source/provenance. `notices/ufbx/`. |
| Cryptography / cffi / pycparser | 46.0.5 / 2.1.1 / 3.0 | Installed metadata/license files within the runtime and readable copies under `notices/verifier/`. Cryptography embeds OpenSSL 3.5.5; its Apache-2.0 text is in `license_supplements/OpenSSL-3.5.5-LICENSE.txt`. `Verifier-46.0.5-NOTICES.txt`/ZIP preserve 80 source/crate/libffi notices, including all 36 checksum-verified Cargo.lock registry packages. Final embedded source/binary correspondence remains part of the wider review. |
| Theme tokens | pyside6-fluent-ui adaptation / Microsoft Fluent UI | MIT notices are in `FLUENT_LICENSE.txt` and `FLUENT_THIRD_PARTY_NOTICES.md`, and accompany the resource files. No upstream font or widget implementation is shipped. |
| FreeType | 2.14.3 | Proposed FTL option, subject to the source's per-file exceptions. Exact upstream license supplements are prepared separately. |
| GLib / libiconv / libintl / Graphite2 / Cairo | See release inventory | LGPL or alternative licenses depend on the component and file; full texts and source arrangements must accompany the final selection. |
| Microsoft VC runtime / UCRT | 14.51.36247 / package 10.0.26100.0, DLLs 10.0.26100.4654 | All 116 inventoried copies match permitted supplier x64 runtime files byte-for-byte. Community individual-development and SDK terms apply, with recipient protections in the application terms. Original vendor documents are in `notices/license_supplements/`. |
| Mesa llvmpipe / embedded LLVM | 12.0.0-rc2 / 3.6.2 | Mesa DLL matches the exact Qt precompiled archive. Mesa MIT/Khronos/Boost and LLVM 3.6.2 NCSA/embedded terms are prepared under `notices/mesa-llvm/` and the license supplements. |
| Nuitka / NSIS | 4.2.2 / bundled installer tool | Compiler/runtime and installer notices in `notices/nuitka/` and `notices/NSIS-LICENSE.txt`. |

This index is not exhaustive. The candidate records 104 conda packages, plus the
native bridges, verifier packages and resources. Its `notices/` directory and
runtime metadata provide the fuller inventory; the final release must reconcile
them with the files actually distributed.

The FreeType option requires the appropriate credit:
"This software is based in part on the work of the FreeType Team."
SQLite 3.53.4 includes an upstream public-domain dedication in its header.
The prepared FreeType, SQLite and libintl supplements have hash provenance in
`license_supplements/provenance.json`; they are included in the new dev.6 notice set.

## Revised Qt/Mesa/Microsoft notice set

The Qt Windows recipe selects ten families, including qtimageformats. The
preparation now contains 364 original Qt/PySide legal/attribution files and 95
attribution files describing 116 components. All seven files that failed strict
JSON parsing are recovered using the Qt-style newline convention. Original bytes
and duplicate descriptive/version fields are preserved; license/copyright fields
are unique. Shiboken's two referenced Python-3.7 PSF texts are also included.
The collection conservatively retains source-only and other-platform attributions;
not every collected component is linked into Windows libraries.

`license_supplements/Qt-PySide-6.11.2-notices.zip` and
`license_supplements/Mesa-12.0.0-rc2-LLVM-3.6.2-notices.zip` contain exact texts
and per-file hash indices. The candidate stager validates every member before
exposing readable copies in `notices/qt-pyside/` and `notices/mesa-llvm/`.
`license_supplements/qt-ms-supplements-provenance.json` records their identities
and the supplier comparisons. These additions are included in the dev.6 notice set;
existing dev.4 files remain unchanged.

A native isolated scene test observes the app's loaded Qt DLLs/plugins and normal
closure. It loads no Designer, DesignerComponents or QmlCompiler tooling library;
static import/delay-import inspection agrees for the app's module set. This
observed scene path does not establish behavior for arbitrary external plugins.
The retained independent tools keep their own licenses and source rights.

## Additional preparation after dev.6

The existing dev.6 installer remains unchanged. The following supplements are
prepared for the next version and are not yet included in that installer:

- `Runtime-extra-NOTICES.txt` and its original-byte ZIP retain 104 delivered
  runtime notices, 43 additional source legal documents and nine complete
  FreeType exception files. This includes NumPy, pip/setuptools vendored code,
  Python, font and other library attributions.
- The conda certificate bundle (certifi 2026.7.22) and pip's separate certifi
  2026.6.17 data carry MPL-2.0 rights despite the package's ISC label. Original
  PEM data matches both exact source archives. Setuptools includes MPL-2.0
  schemas/validate-pyproject code and BSD fastjsonschema notices despite MIT
  package metadata; editable sources and full notices remain in the runtime.
- `Rust-1.93.0-stdlib-NOTICES.txt` and its ZIP preserve six standard-library,
  compiler-builtins/libm and root Rust documents. The cryptography binary embeds
  the matching Rust source commit. The catalogue includes conservative
  platform-specific attributions; it does not establish a historical rebuild.

The final native/runtime ZIP preserves 15,406 unique original legal documents
and exact comment blocks, with a complete source/hash/offset index. Nine
`Native-runtime-NOTICES-*.txt` parts provide readable offline text. This includes
the complete IJG README, Adobe Gain Map, LLVM support/ITT, MinGW, generated
launcher/PSF and Nuitka supplier credits. Conservative catalogue inclusion does
not assert that every platform/source-only component is linked on Windows.
Graphite2's exact LICENSE offers MIT; that library option is selected alongside
the preserved alternatives. All 13 Ubuntu fonts match Canonical's 0.83 source.

Third-party source, modification and redistribution rights continue to take
precedence over original application terms. Hash/source indices are in the
matching supplement provenance files and the complete supplement manifest.
Embedded/native classification is recorded in the final 104-package matrix;
new-installer integration and public delivery remain pending.

## LGPL libraries and corresponding source

The candidate uses external Qt DLLs and PySide/Shiboken extensions alongside
the compiled original application. LGPL-covered components retain the rights
granted by their licenses, including modification and replacement. The final
distribution must include the applicable LGPL and GPL texts, notices and an
appropriate corresponding-source provision. Qt's
[official LGPL obligations](https://www.qt.io/development/open-source-lgpl-obligations)
describe these requirements.

**Source delivery status:** eight verified source archives, their package recipes,
build scripts and patches are now prepared locally. See the
[source preparation index](third_party_sources.md). Local native/resource
reconciliation is complete; final public release links remain open and these
assets are not published.
Before publication, reconcile the sources/build information with the final
payload, attach the required archives and record their verified public links.
An upstream homepage or an email address alone is not source delivery.

## Library replacement procedure to validate

This procedure describes the current folder layout. On 2026-10-08, an isolated
dev.4 copy successfully starts with a modified QtCore DLL and closes normally.
The modification changes the diagnostic string returned by `QLibraryInfo::build()`;
the changed return value executes, and the application process loads that exact
modified DLL. This demonstrates replacement under the existing ABI, rather than
a rebuild of Qt or compatibility with arbitrary future library versions.

1. Close all SceneScope windows and make a copy of the complete installation in
   a directory you can write to. Work on that copy and keep the original backup.
2. Read `active.json` in the copy. Its `runtime` value identifies
   `runtimes/<runtime>/materialx-runtime/`; dev.4 uses the identity above.
3. Supply compatible Windows x64 replacement libraries at the existing runtime
   paths. Qt DLLs occur in `Library/bin/` and `Library/lib/qt6/bin/`; plugins occur
   under `Library/lib/qt6/plugins/`. PySide and Shiboken files occur under
   `Lib/site-packages/`. Keep a consistent, ABI-compatible Qt/PySide/Shiboken set,
   matching the application's Python 3.11 ABI and required modules.
4. Launch the copied `SceneScope.exe`. The current launcher selects these
   external runtime paths; inherited Qt/DCC environment overrides are cleared.
   It does not enforce each DLL's original checksum during ordinary startup.
   Retain the active pair identity to exercise that same application's layout.
5. Original integrity verification will report modified libraries. Official repair
   or update operations may restore the official runtime. Keep your modified copy
   separate and preserve the supplied license texts and notices.

The test needs no signing key from the publisher. The release's final layout and
libraries must retain that capability. Replacement libraries can affect
functionality, so report the modified runtime when seeking assistance.
