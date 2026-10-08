<!-- Private draft: choose the final version, resolve fields, recheck the final payload. -->
# SceneScope {{VERSION}} — Windows preview

Explore 3D scenes, animation and simulation caches in SceneScope for Windows.
This is a development preview; format and exporter limitations apply.

## Download and install

For personal installation, download **`SceneScope-Setup-{{VERSION}}.exe`**,
run it and open SceneScope from the Start Menu. Check
{{CONFIRMED_WINDOWS_GPU_REQUIREMENTS}} before installing.

The complete installer includes its runtime. The application component ZIP alone
is insufficient for installation. The studio ZIP is for managed deployments.
SHA-256 files accompany the downloadable assets.

Downloads and personal/professional studio use are free, with no seat limit.
[Optional contributions](https://victorburtman.gumroad.com/l/qgcdqp) support development
and deliver the same application.

## Included in this preview

- Normal, Velocity and Object ID surface visualization.
- Direct geometry coloring from eligible source attributes and supported volume-field coloring.
- XMesh UV/Velocity and supported generic channels, with explicit missing samples.
- XMesh cache and USD-payload admission limits; unsupported channel association
  transitions produce a frame/channel error and retain the open scene.

Support varies by format and source data. XMesh source materials and authored
shading normals are not reconstructed. Broader exporter fidelity and streaming
of very large sequences remain ongoing work.

## Updates, terms and feedback

For a manual update, close SceneScope and install the new version at the same
destination. Integrated automatic update installation is not available in this preview.

Publisher: Victor Burtman
Application terms: https://github.com/VictorBurtman/scenescope-releases/blob/main/drafts/application_terms.md
Third-party notices and corresponding-source information: https://github.com/VictorBurtman/scenescope-releases/blob/main/drafts/third_party_notices.md
Windows executable signing status: {{FINAL_AUTHENTICODE_STATUS}}
Feedback: victorburtman@gmail.com

## Validation

{{FINAL_PUBLIC_VALIDATION_SUMMARY}}

<!-- Internal baseline only: dev.4 passed 438 source/compiled tests and 18 compiled
checks, isolated fresh/upgrade installation, native launch/shutdown and installed
XMesh. Final external-machine acceptance and redistribution review remain open.
Replace this comment and the validation field with evidence for the final public
payload. Do not copy the private engineering ledger or private asset paths. -->

<!-- Terms/notice links currently point to private review drafts. Complete them,
package the matching documents and verify public access at publication. -->
