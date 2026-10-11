# Origine du moteur PS3

Le lecteur et le déchiffrement du conteneur sont adaptés du projet PkgViewer fourni
par l’utilisateur, auteur indiqué dans ce projet : INF3CONxR7.

Projet de référence :
C:/Users/modzi/Desktop/Applications Visual Studio 2026/02_Projets_Exemples/WinForms/PkgViewer/PkgViewer

Fichiers de référence : PkgReader.cs, PkgHeader.cs, PkgContentReader.cs et PkgCrypto.cs.
L’interface, le moteur d’extraction et les dépendances de PkgViewer ne sont pas importés.

Adaptations : vérification des limites, utilisation du véritable décalage de chaque nom,
flux de lecture bornés et déchiffrés à la demande, addition directe du compteur,
contrôles d’annulation et libération des ressources.

Les champs et les indicateurs du format ont été recoupés avec les sources du
[lecteur RPCS3](https://github.com/RPCS3/rpcs3/blob/master/rpcs3/Crypto/unpkg.h).
Les sources RPCS3 ne sont pas incorporées dans cette application.
Le contrôle SHA-1 final suit la [description du format PKG](https://www.psdevwiki.com/ps3/PKG_files).

LibOrbisPkg reste utilisée comme bibliothèque distincte pour les PKG/PFS PS4 et
le format SFO commun aux deux plateformes. Sa licence figure dans Libraries/LibOrbisPkg.
