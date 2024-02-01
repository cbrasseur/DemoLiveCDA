# Commandes git (utilisation très basique solo)
- Cloner le repo distant (github) 
``` git clone https://github.com/{lien_repo} .``` Le . à la fin permet de copier le contenu directement dans le dossier courant (de l'exécution de la commande)
- Connaître le status des fichiers de son repo local
``` git status ```
- Ajouter des fichiers à commiter 
```git add {filename}```
```git add .``` Ajoute tous les fichiers
```git add -p``` Ouvre les modifications une à une et propose de les ajouter ou non
- Créer un commit (une nouvelle version de notre code)
```git commit -m "{EmojiCommit} {MessageCommit}``` Pour ouvrir l'interface avec les émojis sur windows, faire windows + ;
- Envoyer les sources sur le répo distant
```git push origin main```
- Afficher les logs (différents commits du repo)
```git lg``` (Commande en alias à prendre dans la partie ci-dessous)

# Gestion des logs et des commits
- Ouvrir ses config git
```git config --global -e```
- Si ça ouvre vim ou autre, vous pouvez changer l'editeur par défaut avec (Si vous avez la variable d'environnement pour vs code) : 
```git config --global core.editor "code"```
- (Si vous n'avez pas la variable d'environnement pour vscode)
```git config --global core.editor "C:/{CheminVersVSCode.exe}```
- Ajouter cet alias tout en bas du fichier : 
```
[alias]
	lg = log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit
```
Sauvegarder, puis fermer le fichier
- 