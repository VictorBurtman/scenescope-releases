# SceneScope

**Inspect 3D scenes, animation and simulation caches on Windows.**
SceneScope is a fast viewer for USD, Alembic, FBX/OBJ, STL and the cache formats used in
VFX and motion-graphics pipelines. It opens files read-only, shows what is really in
them, and never rewrites your sources.

*Visionneuse Windows pour scènes 3D, animations et caches de simulation. Les fichiers
sont ouverts en lecture seule. Version française plus bas.*

![SceneScope](assets/scenescope-gumroad-thumbnail-600-v1.png)

## Download

**Current version: 0.1.0-rc.26 (preview)** — free, no account, no telemetry.

- **Installer:** [SceneScope-Setup-rc26.exe](https://github.com/VictorBurtman/scenescope-releases/releases/download/v0.1.0-rc.26/SceneScope-Setup-rc26.exe) (680 MB)
- **Release page, checksums, notices and sources:** [v0.1.0-rc.26](https://github.com/VictorBurtman/scenescope-releases/releases/tag/v0.1.0-rc.26)
- **SHA-256:** `7b6b6745dc703c2539cc1ef657bc5ed86bbb7c0da9ffa7789bfa835d61ecbb4a`

Check it in PowerShell before running:

```powershell
Get-FileHash .\SceneScope-Setup-rc26.exe -Algorithm SHA256
```

### Install

1. Close SceneScope if it is running.
2. Run `SceneScope-Setup-rc26.exe`. It installs for the current user (no administrator
   rights) and includes everything it needs: Python, Qt, OpenUSD and MaterialX — nothing
   else to install.
3. An existing installation is updated in place; your preferences are kept and the
   previous version is retained for recovery.

The installer is **not code-signed** (Authenticode NotSigned), so Windows SmartScreen may
show a warning: choose *More info → Run anyway* after checking the SHA-256 above.

### Requirements

- Windows 11, 64-bit.
- A GPU and driver providing an OpenGL 4.5 compatibility context.
- About 8 GB of free disk space is prudent while installing (the installed application
  is ~2.6 GB); memory needs depend on your scenes.

Only an NVIDIA RTX 3080 Ti system has been qualified so far. Other GPUs, clean/offline
machines and network shares are still being validated — please report what you find.

## New in rc.26: signed in-app updates

Use **Help > Check for updates**. New profiles can enable daily checks of the
prerelease channel. Existing profiles can enable **Check for updates automatically**
in **Preferences > General**. Downloads and installation always require your choice.
Updates verify signed metadata, SHA-256 and inventories, reuse a verified matching
runtime, wait for normal window/worker closure, and preserve preferences with
startup confirmation and rollback recovery.

**From rc.15 or rc.25, install rc.26 manually once.** Those releases shipped without
the public update endpoint and key; a published installer alone cannot notify them.
After the bootstrap upgrade, genuine subsequent releases can be offered in the app.
Studio deployments retain their administrator-managed update policy.

## STL (introduced in rc.25)

Open ASCII and binary STL meshes through File > Open, drag/drop or the command line.
Source files are preserved. STL has no unit or up-axis metadata; coordinates are
kept unchanged, with Y-up and one meter per unit as preview defaults.

## What it does

- **Formats:** USD (`.usd .usda .usdc .usdz`), Alembic (`.abc`), FBX, OBJ, STL (ASCII/binary), MaterialX
  (`.mtlx`), OpenVDB, Houdini BGEO, XMesh, tyCache, PRT/PDC particles, Mantaflow UNI,
  Field3D and Bifrost caches. Support varies by exporter and source data.
- **Inspect:** scene hierarchy, composition (layers, variants, payloads), properties and
  array browsers, shading graphs, dependencies and diagnostics.
- **View:** Storm viewport with lighting and HDRI, material presets, display modes, cameras,
  grid, selection, hide/isolate, data overlays (numeric, color, direction), lens effects
  (depth of field, motion blur, bloom).
- **Time:** timeline with visible range, loop, RAM cache and FPS control.
- English and French interface.

## License and terms

SceneScope is **free for personal, educational and professional use**, including studio
and commercial work, without seat limits. A [Gumroad contribution](https://victorburtman.gumroad.com/l/qgcdqp)
is optional and gives the same application and rights. Read the full [terms](TERMS.md).

The original application code is proprietary. Bundled third-party software keeps its own
licenses. Notices and library-replacement instructions are included in the installer.
The unchanged notice archive, `source-delivery-index.json` and **corresponding source/recipe
archives** remain available on the [rc.21 release](https://github.com/VictorBurtman/scenescope-releases/releases/tag/v0.1.0-rc.21).

## Support

Contact **victorburtman@gmail.com** with the version, system information and steps to
reproduce. SceneScope is a preview: support, schedule and response time are not guaranteed.

---

## Français

**SceneScope** ouvre en lecture seule des scènes USD, Alembic, FBX/OBJ, STL (ASCII/binaire) et de nombreux
caches de simulation (VDB, BGEO, XMesh, tyCache, particules, Field3D, Bifrost) pour
inspecter leur contenu réel sans jamais modifier vos fichiers.

### Nouveauté rc.26 : mises à jour signées dans l'application

Utilisez **Aide > Rechercher les mises à jour**. Les nouveaux profils peuvent
activer une recherche quotidienne des préversions. Un profil existant peut
l'activer dans **Préférences > Général**. Le téléchargement et l'installation
nécessitent toujours votre choix. Les mises à jour vérifient la signature,
les empreintes et les inventaires, attendent la fermeture normale des fenêtres
et workers, conservent les préférences et prévoient un retour arrière.

**Depuis rc.15 ou rc.25, installez d'abord rc.26 manuellement.** Ces versions
ne contenaient ni adresse du service public ni clé de confiance. Les véritables
versions suivantes pourront ensuite être proposées dans l'application.
Les déploiements studio conservent leur politique de mise à jour administrée.

### STL (introduit dans rc.25)

Ouverture des maillages STL ASCII et binaires depuis Fichier > Ouvrir, par
glisser-déposer ou en ligne de commande. Les fichiers source sont préservés.
Le STL ne définit ni unité ni axe vertical : les coordonnées sont conservées,
avec Y vertical et un mètre par unité par défaut pour l’aperçu.

### Télécharger et installer

Version actuelle : **0.1.0-rc.26 (préversion)**, gratuite, sans compte ni télémétrie.

- **Installateur :** [SceneScope-Setup-rc26.exe](https://github.com/VictorBurtman/scenescope-releases/releases/download/v0.1.0-rc.26/SceneScope-Setup-rc26.exe) (680 Mo)
- **SHA-256 :** `7b6b6745dc703c2539cc1ef657bc5ed86bbb7c0da9ffa7789bfa835d61ecbb4a`

Fermez SceneScope s'il est ouvert, puis lancez l'installateur : il s'installe pour
l'utilisateur courant, sans droits administrateur, et contient tout le nécessaire. Une
installation existante est mise à jour sur place (préférences conservées, version
précédente gardée pour la récupération). Le programme n'est pas signé : Windows SmartScreen
peut afficher un avertissement (*Informations complémentaires → Exécuter quand même*)
après vérification de l'empreinte SHA-256.

**Prérequis :** Windows 11 64 bits, pilote graphique avec contexte OpenGL 4.5 en mode
compatibilité. Seule une machine NVIDIA RTX 3080 Ti a été qualifiée à ce jour.

### Licence

Usage gratuit, personnel comme professionnel (studio et projets commerciaux compris),
sans limite de postes ; la contribution Gumroad est facultative et ne change ni
l'application ni les droits. Voir les [conditions](TERMS.md). Le code original reste
propriétaire ; les composants tiers conservent leurs licences. Les notices et instructions
de remplacement des bibliothèques sont incluses dans l'installateur. Les archives de notices
et sources correspondantes inchangées restent disponibles sur la [release rc.21](https://github.com/VictorBurtman/scenescope-releases/releases/tag/v0.1.0-rc.21).

**Assistance :** victorburtman@gmail.com
