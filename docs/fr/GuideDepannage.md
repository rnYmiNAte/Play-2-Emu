# Guide de Dépannage Play2 Emu

---

## Problème Fréquent : Jeux Lents ou Ralentis
- **Symptômes** : Images saccadées, taux d'images inférieur à 25/29,97 ips
- **Solutions** :
  1. Ajustez les paramètres de rendu :
     - Passez au moteur de rendu OpenGL (moins exigeant que Vulkan/Metal)
     - Désactivez les options de filtrage des textures
  2. Fermez toutes les applications en arrière-plan
  3. Pour les jeux PAL : Vérifiez que le taux d'images est réglé sur 25 ips

---

## Problème : Fichier BIOS Non Détecté
- **Solutions** :
  1. Vérifiez que le fichier porte un nom valide (`ps2_bios.bin`, `scph10000.bin`, etc.)
  2. Placez-le dans le répertoire :
     - Android : `/Stockage Interne/Play2Emu/bios/`
     - iOS : Importez-le via le sélecteur de fichiers de l'application
  3. Assurez-vous que le fichier n'est pas corrompu
