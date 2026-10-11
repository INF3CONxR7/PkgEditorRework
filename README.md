# Pkg Editor Rework

Visionneuse et éditeur de paquets **PKG PS3 et PS4** pour Windows. Ouvrez un PKG pour voir ses informations, parcourir ses fichiers, les extraire, modifier son `PARAM.SFO`, vérifier ses empreintes, et, côté PS4, exporter un projet GP4 ou construire un nouveau PKG.

**[Télécharger la dernière version](https://github.com/INF3CONxR7/PkgEditorRework/releases/latest)** · [English](#english)

## Configuration requise

- Un PC sous Windows 64 bits (x64). Rien d'autre à installer : le runtime .NET est inclus dans l'exécutable.
- Aucune console n'est nécessaire : tout se fait sur les fichiers `.pkg`.
- Facultatif : l'application Discord ouverte sur le PC, pour l'activité Discord.

## Fonctionnalités

**Ouverture**

- PKG PS3 et PS4 par **Fichier > Ouvrir…**, **Ctrl+O** ou glisser-déposer ; le format est reconnu automatiquement (badge PS3 / PS4).
- Jusqu'à **trois PKG ouverts** en même temps, chacun dans son onglet.
- Fiche du paquet : titre, icône, identifiant du contenu (copiable), type, taille, version du PKG et de l'application.

**Contenu**

- Arborescence et liste des vrais fichiers du paquet, recherche dans le dossier, vue en liste ou en grille.
- Aperçu au double-clic : textes, images, et aperçu hexadécimal des autres fichiers.
- Extraction d'un fichier ou d'un dossier entier (clic droit ou menu **Paquet**).
- En-têtes détaillés, copiables : en-tête du PKG, et pour la PS4 les images PFS externe et interne.

**PS4**

- Lecture des images PFS et de leurs fichiers.
- **Déverrouillage** d'un contenu chiffré avec le code d'accès (32 caractères), la clé EKPFS (64 caractères hexadécimaux) ou les deux clés XTS.
- Vérification des empreintes et des signatures prises en charge.
- **Extraction complète et export d'un projet GP4**, puis **construction d'un nouveau PKG** depuis ce projet (**Fichier > Construire un PKG PS4 depuis un GP4…**).

**PS3**

- Conteneurs de développement et de distribution, déchiffrés à la lecture.
- Table des fichiers, en-tête et **vérification de l'empreinte SHA-1** finale du paquet.

**PARAM.SFO (PS3 et PS4)**

- Affichage et modification des valeurs, enregistrées dans une **copie** : le PKG d'origine n'est jamais modifié.
- Ouverture directe d'un fichier `.sfo` (**Fichier > Ouvrir un fichier SFO…**).

**Aide**

- **Activité Discord** : affiche le paquet ouvert sur votre profil Discord, avec un petit logo PKG PS4 ou PKG PS3. Activée par défaut, désactivable dans **Aide > Afficher mon activité sur Discord**.
- **Mises à jour** et **À propos** (version installée).

Raccourcis : **Ctrl+O** ouvrir · **Ctrl+W** fermer le paquet · **Ctrl+F** rechercher · **Ctrl+Tab** paquet suivant.

## Installation

1. Ouvrez la [dernière version](https://github.com/INF3CONxR7/PkgEditorRework/releases/latest) et téléchargez **`PkgEditorRework-win-x64.zip`**. Le fichier `.zip.sig` sert au programme de mise à jour : inutile de le télécharger.
2. Extrayez l'archive à l'endroit de votre choix, par exemple dans Documents ou sur le Bureau : vous obtenez le dossier **`PkgEditorRework-win-x64`**. Gardez ensemble tous les fichiers qu'il contient : `Pkg Editor Rework.exe`, `Pkg Editor Rework Update.exe` (le programme de mise à jour), `LibOrbisPkg.dll` et les fichiers de licence.
3. Lancez **`Pkg Editor Rework.exe`** depuis ce dossier.

> **Windows SmartScreen** : l'exécutable n'est pas signé Authenticode, Windows peut donc afficher « Windows a protégé votre ordinateur ». Cliquez sur **Informations complémentaires**, puis sur **Exécuter quand même**.

## Utilisation

1. Ouvrez un ou plusieurs PKG (**Ctrl+O** ou glisser-déposer sur la fenêtre).
2. Parcourez le contenu dans l'arborescence ; double-cliquez sur un fichier pour l'afficher.
3. Clic droit sur un fichier ou un dossier > **Extraire l'élément…** pour l'enregistrer sur le PC.
4. Menu **Paquet** : déverrouillage, paramètres SFO, export GP4 et vérification.

Bon à savoir : les PKG sont ouverts en **lecture seule**. Les modifications (SFO, reconstruction) produisent toujours de nouveaux fichiers.

## Limites

- Les codes et clés des PKG officiels ne sont pas fournis : sans eux, un contenu PFS chiffré reste fermé, mais ses informations restent consultables.
- Les PKG construits sont des PKG de développement : ils ne portent pas de signature officielle.
- Les conteneurs PSP / PS Vita et les paquets découpés incomplets ne sont pas pris en charge.
- Les fichiers SELF, EDAT et SDAT d'un PKG PS3 sont affichés et extraits tels quels.

## Mises à jour

Au démarrage, l'application vérifie sur GitHub si une nouvelle version est publiée. Si c'est le cas, **« Mise à jour X.Y.Z disponible »** apparaît à droite de la barre de menus : un clic, et l'application se ferme, installe la mise à jour, puis se relance. Vous pouvez aussi utiliser **Aide > Rechercher les mises à jour…**. Chaque version est **signée** : une version dont la signature est absente ou invalide est refusée. Aucun droit d'administrateur n'est demandé, sauf si l'application est installée dans un dossier protégé comme `C:\Program Files`.

`Pkg Editor Rework Update.exe` peut aussi être lancé seul : il cherche la dernière version et l'installe si elle est plus récente.

## Désinstallation

Supprimez le dossier de l'application. Le choix de l'activité Discord et le journal des mises à jour sont dans `%LocalAppData%\PkgEditorRework`.

## Licences

L'application utilise **[LibOrbisPkg](https://github.com/maxton/LibOrbisPkg)** de maxton, sous licence **GNU LGPL v3**, adaptée à .NET 10 et livrée en DLL distincte (`LibOrbisPkg.dll`). Ses licences (`LICENSE.txt`, `COPYING-GPL-3.0.txt`) et ses mentions (`NOTICE.md`) accompagnent l'exécutable.

## Support

- Discord : [discord.gg/TbFYvqsh5z](https://discord.gg/TbFYvqsh5z)
- Soutenir le projet : [ko-fi.com/INF3C7ONxR7](https://ko-fi.com/INF3C7ONxR7)

Développé par **INF3C7ONxR7**.

---

## English

**Pkg Editor Rework** is a **PS3 and PS4 PKG** viewer and editor for Windows. Open a PKG to see its details, browse and extract its files, edit its `PARAM.SFO`, check its hashes and, for PS4, export a GP4 project or build a new PKG. The interface is in French.

**Requirements**: Windows 64-bit (x64) PC, no .NET install needed · no console needed · optional: Discord app running for the Discord activity.

**Features**: open up to three PS3/PS4 PKGs in tabs (menu, Ctrl+O or drag and drop) · package card (title, icon, content ID, type, size, versions) · file tree, search, list/grid view, preview (text, images, hex) and extraction · detailed headers · PS4: PFS images, unlocking with passcode, EKPFS or XTS keys, hash and signature checks, full extraction with GP4 project export and building a new PKG from a GP4 · PS3: retail and debug containers, SHA-1 check · PARAM.SFO viewing and editing, saved as a copy · Discord activity with a PS4 or PS3 PKG badge (on by default, can be turned off).

**Install**: download **`PkgEditorRework-win-x64.zip`** from the [latest release](https://github.com/INF3CONxR7/PkgEditorRework/releases/latest) (not the `.sig` file, which is used by the updater), extract it wherever you like to get the **`PkgEditorRework-win-x64`** folder, keep all its files together and run **`Pkg Editor Rework.exe`**. The executable is not Authenticode-signed, so Windows SmartScreen may show "Windows protected your PC": click **More info**, then **Run anyway**.

**Limits**: keys for official PKGs are not included; built PKGs are debug PKGs without official signatures; PSP / PS Vita containers are not supported.

**Updates**: the app checks GitHub at startup; when a new version is out, click **"Mise à jour X.Y.Z disponible"** in the menu bar (or **Aide > Rechercher les mises à jour…**). Every release is signed; unsigned or tampered releases are refused.

**Licenses**: uses [LibOrbisPkg](https://github.com/maxton/LibOrbisPkg) by maxton (GNU LGPL v3), shipped as a separate DLL with its license files.

**Support**: [Discord](https://discord.gg/TbFYvqsh5z) · [Ko-fi](https://ko-fi.com/INF3C7ONxR7) · Developed by **INF3C7ONxR7**.
