# Démarrage de l’alpha

Si le jeu de base nécessite le patch Intel, voici sa page originale : [Intel HD graphics Bypass package de Bren712](https://www.nexusmods.com/fallout3/mods/17209). Suivre les instructions de son auteur et vérifier le fonctionnement du jeu sans VR. Ce patch n’est pas obligatoire sur tous les PC, ni inclus dans l’alpha. Conserver votre `d3d9.dll` s’il fonctionne déjà ; le lanceur VR le préserve.

Extraire tout le ZIP, connecter le Quest au PC via Virtual Desktop ou SteamVR, réveiller les deux manettes, puis double-cliquer **THEwill_Fallout3_VR.exe**. Steam doit être connecté et le jeu de base doit déjà fonctionner. Le lanceur démarre directement Fallout3.exe, sans la fenêtre Start/Settings, et active la VR automatiquement.

Le dossier Steam est détecté ; s’il ne l’est pas, une sélection de dossier apparaît. Le runtime est sélectionné automatiquement sans modifier les réglages OpenXR globaux. Si les deux sont installés, SteamVR déjà lancé a priorité, puis le runtime enregistré. Le lanceur essaie l’autre runtime disponible si le casque n’est pas prêt. Il ne peut pas établir à votre place la connexion du casque dans l’application de streaming.

Dans `settings.json`, `Profile` accepte `Normal`, `HD` ou `UHD` ; `Runtime` accepte `Auto`, `VirtualDesktop` ou `SteamVR`. HD est le profil par défaut. La rotation physique n’est pas plafonnée dans ce lanceur.

Quitter le jeu normalement permet de restaurer les DLL précédentes et les trois réglages d’affichage temporaires. Après un arrêt brutal, relancer le lanceur avec le jeu fermé. Les sauvegardes de restauration et journaux se trouvent dans `%LOCALAPPDATA%\Fallout3VR`. Un conflit de DLL est signalé au lieu d’écraser un autre mod. Le patch Intel et vos sauvegardes de partie ne sont pas modifiés.

Cette alpha reconnaît uniquement l’exécutable Steam 1.7.0.4 précis documenté dans README.md. Les autres versions sont refusées. Aucun fichier du jeu n’est fourni. La calibration personnelle du développeur et les poses extraites du jeu ne sont pas incluses.

Limites : rendu alterné entre les yeux, reflets d’eau simplifiés, modèles de mains/armes reconnus seulement, prise à deux mains et mêlée partielles. La version 0.70 du lanceur et le recentrage ont été testés sur la configuration de développement. Une seconde machine reste à valider. Problèmes connus : Pip-Boy parfois décalé au poignet gauche ; crashs intermittents au lancement signalés, sans résolution complète confirmée. Consulter README.md et CONTROLS.md pour les détails.

Pour les retours, ouvrir [un ticket GitHub](https://github.com/THEwill2002/Fallout3VR/issues/new/choose) : **Bug report** pour un problème, **Alpha feedback** pour un résultat de test ou une suggestion. Vous pouvez écrire en français. Indiquer la version du mod, le casque, la carte graphique, le runtime et le profil utilisé. Un ticket par bug ; rechercher les tickets existants avant d’en créer un. Ne pas publier les captures F8 brutes ni les fichiers du jeu.

Pour choisir sans modifier settings.json : double-cliquer Launch-HD.cmd (moins exigeant) ou Launch-UHD.cmd (plus net). L’exécutable accepte aussi --hd et --uhd.
