# LibOrbisPkg

Bibliothèque de maxton, issue du dossier LibOrbisPkg-0.2 fourni par l’utilisateur.
Code original : https://github.com/maxton/LibOrbisPkg
Licence : GNU LGPL version 3. Voir LICENSE.txt et COPYING-GPL-3.0.txt.

La bibliothèque est compilée dans une DLL distincte. Ses sources restent dans ce dossier.

Adaptations locales pour PkgEditorRework, le 10 octobre 2026 :
- projet SDK ciblant .NET 10 et conservation de l’espace de noms original ;
- remplacement de AesManaged par Aes.Create et du RSA brut DecryptValue par une exponentiation modulaire ;
- lectures exactes des flux et respect de la fin de flux par StreamWrapper ;
- libération des contextes AES utilisés par XTS ;
- contrôles de cohérence et limites des structures PFS, PFSC et SFO ;
- lecture du param.sfo dans un flux borné à son entrée ;
- longueur UTF-8 correcte pour les chaînes spéciales SFO.

L’application elle-même utilise ces API à travers Resources/Packages.
Le dossier original fourni n’a pas été modifié.
