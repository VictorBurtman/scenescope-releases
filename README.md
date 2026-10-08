# SceneScope — préparation de la distribution

Ce dépôt est privé pendant la préparation. Il accueillera la documentation
publique et les téléchargements de SceneScope. Le code de l'application reste
dans un autre dépôt privé ; aucun historique de développement n'est importé ici.

## Brouillons à relire

- [Présentation GitHub](drafts/github_README.md)
- [Page Gumroad en français et en anglais](drafts/gumroad_copy.md)
- [Notes de préversion](drafts/github_release.md)
- [Conditions d'utilisation](drafts/application_terms.md)
- [Notices tierces et remplacement des bibliothèques](drafts/third_party_notices.md)
- [Préparation des sources tierces](drafts/third_party_sources.md)
- [Suppléments de licences vérifiés](drafts/license_supplements/README.md)

Compte Gumroad : https://victorburtman.gumroad.com/

Page SceneScope créée par Victor : https://victorburtman.gumroad.com/l/qgcdqp

Les champs entre doubles accolades attendent les derniers choix de publication.
Aucun téléchargement public n'est disponible dans ce dépôt à ce stade.
Les derniers essais Windows, les conditions et notices de redistribution,
ainsi que les choix de signature et de mise à jour restent à finaliser.

Choix confirmés le 8 octobre 2026 : usage gratuit personnel et professionnel,
y compris en studio, sans limite de postes. Éditeur : Victor Burtman.
Assistance : victorburtman@gmail.com. Les contributions Gumroad restent facultatives.

Les conditions et notices sont des brouillons à relire. La fourniture des sources
des dépendances, les derniers contrôles de redistribution et la validation du
prochain paquet restent à terminer avant publication.

Suite du 8 octobre : huit archives sources exactes et leurs recettes/correctifs
sont préparés et vérifiés hors ligne. Un essai de SceneScope avec un DLL QtCore
réellement modifié réussit dans une copie isolée. Le NOTICE OpenUSD et les textes
complets Graphite2/Qt sont préparés. La revue finale des fichiers et la livraison
publique des sources restent à terminer ; aucun binaire n'est publié ici.

Revue Qt/Mesa/Microsoft du 8 octobre : les 70 bibliothèques Qt principales sont
rapprochées de leurs cibles source ; 364 fichiers de notices Qt/PySide sont
préparés et les sept problèmes de format d'attribution sont résolus. Le DLL Mesa
correspond au précompilé Qt, avec les notices LLVM 3.6.2. Les 116 copies Microsoft
recensées correspondent désormais aux fichiers redistribuables du fournisseur.
Les conditions incluent les protections Microsoft en préservant les droits LGPL.
Les nouveaux bundles de notices restent des documents pour le prochain build.
Aucun installateur, média SDK Microsoft ou code original SceneScope n'est publié.

Préparation dev.5 : les conditions et les notices disposent d'un lecteur hors
ligne EN/FR, avec information LGPL visible et page d'accord dans l'installateur.
Les nouveaux compléments du vérificateur conservent OpenSSL 3.5.5 et 80 notices
sources/Rust/libffi ; les 36 archives du Cargo.lock officiel sont vérifiées.
Les archives binaires et la revue globale restent locales en cours de validation.
Le dépôt de code original et ce dépôt de préparation restent privés. Aucun
installateur ni média SDK Microsoft n'est téléchargé ici ou publié.


Préparation dev.6 validée localement : correction de la copie et de la lecture
des notices dans les chemins Windows longs. Les 450 tests passent sur le code
source et sur le module compilé. Installation neuve, mise à niveau depuis dev.4,
démarrage natif et notices hors ligne EN/FR passent dans des dossiers de test
isolés ; les 547 notices sont copiées et inventoriées pour la désinstallation.
Ces essais ne remplacent pas les tests sur un autre PC/GPU. La revue globale,
les liens publics des sources et les décisions de signature restent ouverts.
Aucun binaire n'est publié et les deux dépôts restent privés.


Revue systématique du runtime dev.6 : 42 946 fichiers vérifiés, 104 paquets
Conda rapprochés des empreintes et 148 fichiers du vérificateur identiques à
leurs wheels PyPI. Signature de publication cryptography vérifiée. Les nouveaux
compléments couvrent 162 documents originaux, les exceptions MPL certificats/
setuptools, FreeType et la bibliothèque standard Rust 1.93.0. Quatre sources
exactes et 1 159 fichiers de recettes sont préparés localement. Ces compléments
ne sont pas dans l'installateur dev.6 existant ; intégration sous une nouvelle
version et revue restante précèdent la publication. Aucun binaire ni archive
de sources n'est publié ici. Les deux dépôts restent privés.


Revue locale des dépendances embarquées terminée : 104 paquets évalués,
six lanceurs rapprochés exactement de leur fournisseur, 81 déclarations de
sources vérifiées. Le complément natif conserve 15 406 documents/blocs de
notices originaux avec leurs empreintes ; neuf parties lisibles passent les
lecteurs français et anglais. Le manifeste vérifie tous les compléments et
les membres des ZIP avant intégration. Le bilan et la matrice sont dans drafts.

Ces ajouts exigent un nouvel installateur ; dev.6 existant est inchangé.
La livraison publique des sources requises reste à faire. L'essai sur un autre
PC est différé par l'éditeur, indépendamment de la revue des dépendances.
Les deux dépôts restent privés, sans release ni binaire publié. Gumroad inchangé.
