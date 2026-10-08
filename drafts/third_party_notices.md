# SceneScope third-party notices and library replacement

Review draft, 2026-10-08, based on local **0.1.0-dev.4** and runtime
**rt-2192364560b51c5afc8f7221**. This is an index for preparing the next release,
not a declaration that the current package's redistribution review is complete.
The final release must carry the full applicable license texts, attributions,
corresponding sources and verified instructions for its actual payload.

Publisher and source enquiries: **Victor Burtman — victorburtman@gmail.com**.
SceneScope's application terms apply to its original code. Third-party licenses
govern the components below and take precedence for those components.

## Principal components

| Component | Observed version | License / notice location in the candidate |
|---|---|---|
| Qt / PySide / Shiboken | 6.11.2 | Qt and PySide package records declare LGPLv3. Review every shipped module, plugin, tool and embedded third-party component; the package label does not cover every file. `notices/conda/qt6-main-*/` and `notices/conda/pyside6-*/`. |
| OpenUSD, usdview and Storm | 26.08 | Upstream TOST-1.0 and embedded third-party terms; preserve the complete upstream license and applicable NOTICE. `notices/conda/openusd-*/`. |
| MaterialX | 1.39.5 | Complete upstream license and embedded third-party notices. `notices/conda/materialx-*/`. |
| Python | 3.11.16 | Python/PSF and bundled-library terms. `notices/conda/python-*/`. |
| PyOpenGL | 3.1.10 | BSD-style terms. `notices/conda/pyopengl-*/`. |
| oneTBB / OpenSubdiv | 2022.3.0 / 3.7.0 | Complete licenses and third-party notices in their conda notice folders. |
| NumPy / Intel MKL | 2.4.6 / 2025.3.1 | NumPy BSD terms and Intel/other applicable notices in their conda notice folders. |
| Alembic / Imath / Boost / adapted AbcOpenGL | 1.8.12 / 3.2.2 / 1.91 / upstream adaptation | Full applicable upstream notices and modification provenance. `notices/alembic/`. |
| ufbx | 0.23.0 | MIT option; copyright and permission notice with upstream source/provenance. `notices/ufbx/`. |
| Cryptography / cffi / pycparser | 46.0.5 / 2.1.1 / 3.0 | Installed distribution metadata and license files within the runtime. |
| FreeType | 2.14.3 | Proposed FTL option, subject to the source's per-file exceptions. Exact upstream license supplements are prepared separately. |
| GLib / libiconv / libintl / Graphite2 / Cairo | See release inventory | LGPL or alternative licenses depend on the component and file; full texts and source arrangements must accompany the final selection. |
| Microsoft VC runtime / UCRT | 14.51.36247 / 10.0.26100.0 | Microsoft terms; redistribution entitlement and the permitted file list require separate verification. |
| Nuitka / NSIS | 4.2.2 / bundled installer tool | Compiler/runtime and installer notices in `notices/nuitka/` and `notices/NSIS-LICENSE.txt`. |

This index is not exhaustive. The candidate records 104 conda packages, plus the
native bridges, verifier packages and resources. Its `notices/` directory and
runtime metadata provide the fuller inventory; the final release must reconcile
them with the files actually distributed.

The FreeType option requires the appropriate credit:
"This software is based in part on the work of the FreeType Team."
SQLite 3.53.4 includes an upstream public-domain dedication in its header.
The prepared FreeType, SQLite and libintl supplements have hash provenance in
`license_supplements/provenance.json`; they are not yet inside dev.4.

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
[source preparation index](third_party_sources.md). The final per-file/embedded
review and public release links remain open; these assets are not published.
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
