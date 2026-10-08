<!-- Private review draft. Resolve placeholders and public license/notice files before use. -->
# SceneScope

Inspect 3D scenes and simulation caches in a Windows desktop viewer.

SceneScope brings scene hierarchy, properties, animation and viewport diagnostics
into one application. It previews supported USD, Alembic, FBX, OBJ, XMesh,
Houdini BGEO, OpenVDB and observed tyCache layouts, with MaterialX look development.
Support varies by format and exporter; this preview does not reproduce every
feature of the originating application.

## Download

[Download the Windows preview]({{RELEASE_URL}})

Choose the complete `SceneScope-Setup-{{VERSION}}.exe` installer. The separate
application ZIP requires its matching runtime; use the complete installer for
personal installation. The full studio ZIP is intended for managed deployment.

Downloads and use are free for personal and professional purposes, including
commercial studio work, with no seat limit. [Support development on Gumroad](https://victorburtman.gumroad.com/l/qgcdqp) if you wish;
contributions are optional and deliver the same application.

## Explore your scene

- Browse hierarchy, inspect properties and step through animation samples.
- Inspect surfaces using Normal, Velocity and Object ID visualization.
- Color eligible geometry from source attributes and inspect supported volume fields.
- Preview supported materials, lighting and camera effects.

Available data and controls depend on the scene format. Velocity visualization
uses source data when available. A displayed Object ID color does not guarantee
a unique ID; picking reports the object's identity separately.

## Installation and updates

System requirements: {{CONFIRMED_WINDOWS_GPU_REQUIREMENTS}}

Download and run the complete installer, then open SceneScope through its Start
Menu shortcut. Installed scene inspection works offline. Internet access is
needed for downloads and optional online version checks. Studio deployments
follow their administrator's update policy.

For a manual update, close SceneScope and run the new installer at the same
destination. Keep a backup of important preferences and follow that release's
instructions. Integrated automatic installation of updates is not available in
this preview.

## Preview limitations and feedback

This is a development preview. Supported exporter/layout combinations and memory
limits apply. XMesh source materials and authored shading normals are not
reconstructed; its channel association must remain constant across a sequence.
Broader exporter fidelity and very-large-scene streaming remain ongoing work.

Report reproducible problems to [victorburtman@gmail.com](mailto:victorburtman@gmail.com) with the SceneScope
version, Windows/GPU information, file format and steps. Share only scenes and
screenshots you are permitted to disclose; exclude confidential studio data.

## License and notices

Published by **Victor Burtman**. SceneScope's original application code is
proprietary. See the [application terms](application_terms.md) for the applicable
terms. Third-party components retain their own licenses; see the
[third-party notices](third_party_notices.md) and corresponding-source information.

<!-- Preparation links point to review drafts. Finalize the terms, source
delivery and matching packaged notices before using this README publicly. -->

This repository contains release documentation and binaries. Original application
source is maintained separately in a private repository.
