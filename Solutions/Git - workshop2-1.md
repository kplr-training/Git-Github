# GIT

## Objectif
L'objectif de cet atelier est d'approfondir vos compétences en travaillant avec les branches Git. 

Les branches sont utiles pour développer des fonctionnalités de manière isolée et collaborer efficacement sur un projet. Vous apprendrez à créer et à basculer entre les branches, à fusionner les modifications entre les branches, et à résoudre les éventuels conflits. 

## Instructions

### 1. Configuration initiale :

Ouvrez votre terminal.

Configurez votre nom d'utilisateur en utilisant la commande suivante :

```
$ git config --global user.name "Votre nom d'utilisateur"
```
     
La commande git config --global user.name "Votre nom d'utilisateur" vous permet de définir votre nom d'utilisateur. Remplacez "Votre nom d'utilisateur" par votre nom d'utilisateur réel. 

Configurez votre adresse e-mail en utilisant la commande suivante :

```
$ git config --global user.email "Votre adresse e-mail"
```

La commande git config --global user.email "Votre adresse e-mail" vous permet de définir votre adresse e-mail. Remplacez "Votre adresse e-mail" par votre adresse e-mail réelle.

Assurez-vous de remplacer les valeurs entre guillemets par vos propres informations. Une fois que vous avez exécuté ces commandes, votre nom d'utilisateur et votre adresse e-mail seront configurés globalement dans Git.

### 2. Vérifier que la configuration de votre nom d'utilisateur et de votre adresse e-mail a été effectuée avec succès. 

Vous pouvez utiliser la commande `git config --global --list` pour afficher la liste des paramètres de configuration globale de Git, y compris votre nom d'utilisateur et votre adresse e-mail.

Exécutez la commande suivante dans votre terminal :

```
$ git config --global --list
```

Cela affichera une liste des paramètres de configuration globale, y compris votre nom d'utilisateur et votre adresse e-mail, si vous les avez configurés correctement.

Assurez-vous de rechercher les lignes contenant **`user.name` et `user.email`** dans la sortie de la commande pour confirmer que vos informations de configuration sont correctement enregistrées.

![image](https://github.com/kplr-training/Git-Github/assets/123757632/2fe54518-acb9-4214-acac-8fcf51071f14)

### 3. Initialisation d'un nouveau dépôt :

Créez un nouveau dossier vide pour votre dépôt :

```
$ mkdir mon-depot
```

Cette commande crée un nouveau dossier (répertoire) portant le nom "mon-depot". Le terme "mkdir" est une abréviation de "make directory", qui signifie créer un répertoire. Une fois cette commande exécutée, un nouveau dossier vide portant le nom "mon-depot" est créé dans le répertoire actuel.

```
$ cd mon-depot
```

Cette commande permet de changer de répertoire (se déplacer vers un autre dossier). Le terme "cd" est une abréviation de "change directory". Lorsque vous exécutez cette commande, vous vous déplacez dans le dossier "mon-depot" qui vient d'être créé. Toutes les commandes ultérieures seront exécutées dans ce nouveau dossier.

### 4. Initialisez le dépôt Git en utilisant la commande suivante :

```
$ git init
```

La commande `git init` est utilisée pour initialiser un nouveau dépôt Git dans un répertoire existant. Lorsque vous exécutez cette commande, Git crée un sous-répertoire caché appelé ".git" dans le répertoire courant. Ce sous-répertoire contient toute la structure et les fichiers nécessaires pour suivre l'historique des modifications, gérer les branches, effectuer des commits, etc.

Le résultat de l'exécution de la commande `git init` est le suivant :

Git affiche un message indiquant que le dépôt est initialisé :
  ```
  Initialized empty Git repository in /chemin/vers/le/repertoire/.git/
  ```
Après l'initialisation du dépôt, vous pouvez commencer à ajouter des fichiers au suivi de Git, créer des commits et effectuer d'autres opérations liées à la gestion des versions avec Git.

![image](https://github.com/kplr-training/Git-Github/assets/123757632/fa6ddeba-35ae-4e7d-9eba-d4782b868ece)

### 5. Création d'un fichier Python

Créez un fichier Python vide dans le dossier :

```
$ touch gestion_eleves.py
```

### 6. Création de la nouvelle branche ajouter_eleve

Une branche est une ligne de développement isolée qui permet aux utilisateurs de travailler sur des fonctionnalités, des correctifs ou des expérimentations sans affecter la branche principale du projet, généralement appelée "branche principale" ou "branche maître" (par convention, "master" en anglais).

```
git branch ajouter_eleve
```
La commande "git branch ajouter_eleve" est utilisée pour créer une nouvelle branche dans un référentiel Git avec le nom "ajouter_eleve". 

### 7. Basculer vers la branche ajouter_eleve

La commande "git checkout ajouter_eleve" est utilisée pour basculer vers une branche spécifique dans un référentiel Git. Dans ce cas, la branche spécifique est "ajouter_eleve".

```
git checkout ajouter_eleve
```
Lorsque vous exécutez cette commande, Git met à jour votre répertoire de travail pour refléter l'état de la branche spécifiée. Cela signifie que les fichiers dans votre répertoire de travail seront modifiés pour correspondre à l'état de la branche "ajouter_eleve". Les modifications non validées dans votre branche actuelle peuvent être perdues si elles ne sont pas sauvegardées ou validées avant de passer à une autre branche.

![image](https://github.com/kplr-training/Git-Github/assets/123757632/24c4ffde-b190-4022-8549-6a743cf26dc9)

### 8. Ouvrez le fichier `gestion_eleves.py` et ajoutez la fonction pour ajouter un élève

```
def ajouter_élève():
    id_élève = input("Entrez l'identifiant de l'élève : ")
    nom_élève = input("Entrez le nom de l'élève : ")
    élèves[id_élève] = nom_élève
    print("Élève ajouté avec succès !")
```
La fonction ajouter_élève permet à l'utilisateur d'entrer l'identifiant et le nom d'un nouvel élève, puis ajoute ces informations au dictionnaire élèves.


### 9. Ajoutez le fichier `gestion_eleves.py` au suivi de Git en utilisant la commande suivante 

```
$ git add .
```

La commande `git add .` est utilisée pour ajouter le fichier `gestion_eleves.py` au suivi de Git. Cela signifie que Git commencera à suivre les modifications apportées à ce fichier et le prendra en compte lors des futurs commits.

### 10. Création d'un premier commit pour la fonction `ajouter_élève` 

Créez un commit pour enregistrer la fonction `ajouter_élève` 

```
$ git commit -m "Ajout de la fonction d'ajouter_élève"
```

La commande `git commit -m "Ajout de la fonction d'addition"` est utilisée pour créer un nouveau commit dans le dépôt Git. Un commit est une capture instantanée des modifications apportées aux fichiers suivis par Git.

Explication de la commande :

* `git commit` est la commande principale pour créer un commit.
* `-m "Ajout de la fonction d'addition"` est un paramètre qui permet de spécifier le message du commit. Le message doit être placé entre guillemets.

Résultat de l'exécution de la commande :

- Si le commit est créé avec succès, Git affiche des informations sur le commit, telles que l'identifiant unique du commit (SHA-1), l'auteur, la date et le message du commit.

- Par exemple :

```
[main f7fde4f] Ajout de la fonction d'addition
1 file changed, 10 insertions(+)
```
- Le commit est enregistré dans l'historique du dépôt Git, capturant ainsi les modifications apportées aux fichiers à ce stade.

Une fois le commit créé, les modifications apportées aux fichiers sont enregistrées de manière permanente dans le dépôt Git. 

![image](https://github.com/kplr-training/Git-Github/assets/123757632/c52a34ed-34c8-436b-a8a2-d499d77c7a40)

### 11. Afficher l'historique des commits et vérifier que votre commit a été enregistré avec succès

```
$ git log
```

La commande `git log` est utilisée pour afficher l'historique des commits dans le dépôt Git. Lorsque vous exécutez cette commande, Git affiche une liste des commits effectués, triés du plus récent au plus ancien.

Résultat de l'exécution de la commande :

- Chaque commit est affiché avec des informations telles que l'identifiant du commit (SHA-1), l'auteur, la date et le message du commit.
- Par exemple :
  ```
  commit f7fde4f82d5e8a7574680a8e138e41c05d1e3d6e
  Author: Votre nom <votre@email.com>
  Date:   Lun. Sept. 13 10:00:00 2023 +0200

      Ajout de la fonction d'addition

  commit 2cfd3b1e8949a7b894ca57182a3b14db6c0ee43f
  Author: Autre contributeur <autre@email.com>
  Date:   Lun. Sept. 12 15:30:00 2023 +0200

      Correction de bug dans la fonction de soustraction
  ```

- Chaque commit est identifié par son identifiant unique (SHA-1). Vous pouvez utiliser cet identifiant pour référencer spécifiquement un commit.

![image](https://github.com/kplr-training/Git-Github/assets/123757632/e41a8a1e-ce34-48ef-8d7b-e60a3f47695b)

### 12. Basculer vers la branche principale 

La commande "git checkout main" est utilisée pour basculer vers la branche principale (ou branche maître) dans un référentiel Git. La branche principale est généralement utilisée pour représenter l'état stable du projet.

```
git checkout main
```

Lorsque vous exécutez cette commande, Git met à jour votre répertoire de travail pour refléter l'état de la branche principale. Cela signifie que les fichiers dans votre répertoire de travail seront modifiés pour correspondre à l'état de la branche "main". 

![image](https://github.com/kplr-training/Git-Github/assets/123757632/f2bb6a1c-53fd-4878-aedc-5d3973750c15)

### 13. Fudionner la branche "ajouter_eleve" avec la branche "main"

La commande "git merge ajouter_eleve" fusionne la branche "ajouter_eleve" dans la branche actuelle. Plus précisément, elle incorpore les modifications de la branche "ajouter_eleve" dans la branche courante.

```
git merge ajouter_eleve
```

Lorsque vous exécutez cette commande, Git examine les modifications entre la branche actuelle et la branche "ajouter_eleve". Il essaie de fusionner automatiquement les modifications, en appliquant les changements de la branche "ajouter_eleve" sur la branche courante.

![image](https://github.com/kplr-training/Git-Github/assets/123757632/cbc15f8c-4b27-4a4f-a489-f53397ece1a8)

En résumé, la commande "git merge ajouter_eleve" fusionne les modifications de la branche "ajouter_eleve" dans la branche courante, incorporant ainsi les changements effectués dans la branche "ajouter_eleve" dans votre branche de travail actuelle.

**REMARQUE : La fonction ajouter_eleve se trouve maintenant dans le ficher "gestion_eleve" dans la branche principale "main"**

### 14. Création de la nouvelle branche modifier_eleve

```
git branch modifier_eleve
```
La commande "git branch modifier_eleve" est utilisée pour créer une nouvelle branche dans un référentiel Git avec le nom "modifier_eleve". 

### 15. Basculer vers la branche modifier_eleve

La commande "git checkout modifier_eleve" est utilisée pour basculer vers une branche spécifique dans un référentiel Git. Dans ce cas, la branche spécifique est "modifier_eleve".

```
git checkout modifier_eleve
```
![image](https://github.com/kplr-training/Git-Github/assets/123757632/2ce82b40-d957-46ef-bcec-508a28e53271)


### 16. Ouvrez le fichier `gestion_eleves.py` et ajoutez la fonction pour modifier un élève

```
def modifier_élève():
    id_élève = input("Entrez l'identifiant de l'élève à modifier : ")
    if id_élève in élèves:
        nouveau_nom = input("Entrez le nouveau nom de l'élève : ")
        élèves[id_élève] = nouveau_nom
        print("Élève mis à jour avec succès !")
    else:
        print("L'élève n'existe pas.")
```

La fonction modifier_élève permet à l'utilisateur d'entrer l'identifiant et le nom d'un nouvel élève, puis modifie ces informations au dictionnaire élèves.

### 17. Ajoutez le fichier `gestion_eleves.py` au suivi de Git en utilisant la commande suivante 

```
$ git add .
```

La commande `git add .` est utilisée pour ajouter le fichier `gestion_eleves.py` au suivi de Git. Cela signifie que Git commencera à suivre les modifications apportées à ce fichier et le prendra en compte lors des futurs commits.

### 18. Création d'un premier commit pour la fonction `modifier_élève` 

Créez un commit pour enregistrer la fonction `modifier_élève` 

```
$ git commit -m "Ajout de la fonction de modifier_élève"
```

La commande `git commit -m "Ajout de la fonction de modifier_élève"` est utilisée pour créer un nouveau commit dans le dépôt Git. Un commit est une capture instantanée des modifications apportées aux fichiers suivis par Git.

Explication de la commande :

* `git commit` est la commande principale pour créer un commit.
* `-m "Ajout de la fonction de modifier_élève"` est un paramètre qui permet de spécifier le message du commit. Le message doit être placé entre guillemets.

Résultat de l'exécution de la commande :

- Si le commit est créé avec succès, Git affiche des informations sur le commit, telles que l'identifiant unique du commit (SHA-1), l'auteur, la date et le message du commit.

- Par exemple :

```
[main f7fde4f] Ajout de la fonction d'addition
1 file changed, 10 insertions(+)
```
- Le commit est enregistré dans l'historique du dépôt Git, capturant ainsi les modifications apportées aux fichiers à ce stade.

Une fois le commit créé, les modifications apportées aux fichiers sont enregistrées de manière permanente dans le dépôt Git. 

![image](https://github.com/kplr-training/Git-Github/assets/123757632/fa5c28fb-2387-49c8-84a6-bb4831f002aa)

### 19. Afficher l'historique des commits et vérifier que votre commit a été enregistré avec succès

```
$ git log
```

La commande `git log` est utilisée pour afficher l'historique des commits dans le dépôt Git. Lorsque vous exécutez cette commande, Git affiche une liste des commits effectués, triés du plus récent au plus ancien.

Résultat de l'exécution de la commande :

- Chaque commit est affiché avec des informations telles que l'identifiant du commit (SHA-1), l'auteur, la date et le message du commit.
- Par exemple :
  ```
  commit f7fde4f82d5e8a7574680a8e138e41c05d1e3d6e
  Author: Votre nom <votre@email.com>
  Date:   Lun. Sept. 13 10:00:00 2023 +0200

      Ajout de la fonction d'addition

  commit 2cfd3b1e8949a7b894ca57182a3b14db6c0ee43f
  Author: Autre contributeur <autre@email.com>
  Date:   Lun. Sept. 12 15:30:00 2023 +0200

      Correction de bug dans la fonction de soustraction
  ```

- Chaque commit est identifié par son identifiant unique (SHA-1). Vous pouvez utiliser cet identifiant pour référencer spécifiquement un commit.

![image](https://github.com/kplr-training/Git-Github/assets/123757632/0d16bd78-a3ef-4d11-9432-7a86ddc50958)

### 20. Basculer vers la branche principale 

La commande "git checkout main" est utilisée pour basculer vers la branche principale (ou branche maître) dans un référentiel Git. La branche principale est généralement utilisée pour représenter l'état stable du projet.

```
git checkout main
```

Lorsque vous exécutez cette commande, Git met à jour votre répertoire de travail pour refléter l'état de la branche principale. Cela signifie que les fichiers dans votre répertoire de travail seront modifiés pour correspondre à l'état de la branche "main". 

![image](https://github.com/kplr-training/Git-Github/assets/123757632/f2bb6a1c-53fd-4878-aedc-5d3973750c15)

### 21. Fudionner la branche "modifier_eleve" avec la branche "main"

La commande "git merge modifier_eleve" fusionne la branche "modifier_eleve" dans la branche actuelle. Plus précisément, elle incorpore les modifications de la branche "modifier_eleve" dans la branche courante.

```
git merge modifier_eleve
```

Lorsque vous exécutez cette commande, Git examine les modifications entre la branche actuelle et la branche "modifer_eleve". Il essaie de fusionner automatiquement les modifications, en appliquant les changements de la branche "modifier_eleve" sur la branche courante.

![image](https://github.com/kplr-training/Git-Github/assets/123757632/97c509d8-37e3-48ac-b619-7cc5b226b3ce)

**REMARQUE : La fonction modifier_eleve se trouve maintenant dans le ficher "gestion_eleve" dans la branche principale "main"**


### 22. Création de la nouvelle branche supprimer_eleve

```
git branch supprimer_eleve
```
La commande "git branch modifier_eleve" est utilisée pour créer une nouvelle branche dans un référentiel Git avec le nom "modifier_eleve". 

### 23. Basculer vers la branche supprimer_eleve

La commande "git checkout supprimer_eleve" est utilisée pour basculer vers une branche spécifique dans un référentiel Git. Dans ce cas, la branche spécifique est "supprimer_eleve".

```
git checkout supprimer_eleve
```
![image](https://github.com/kplr-training/Git-Github/assets/123757632/3ac50e69-9423-416d-8dd4-21978552426e)


### 24. Ouvrez le fichier `gestion_eleves.py` et ajoutez la fonction pour supprimer un élève

```
def supprimer_élève():
    id_élève = input("Entrez l'identifiant de l'élève à supprimer : ")
    if id_élève in élèves:
        del élèves[id_élève]
        print("Élève supprimé avec succès !")
    else:
        print("L'élève n'existe pas.")
```

La fonction supprimer_élève permet à l'utilisateur d'entrer l'identifiant et le nom d'un nouvel élève, puis le supprimer.

### 25. Ajoutez le fichier `gestion_eleves.py` au suivi de Git en utilisant la commande suivante 

```
$ git add .
```

La commande `git add .` est utilisée pour ajouter le fichier `gestion_eleves.py` au suivi de Git. Cela signifie que Git commencera à suivre les modifications apportées à ce fichier et le prendra en compte lors des futurs commits.

### 26. Création d'un premier commit pour la fonction `supprimer_élève` 

Créez un commit pour enregistrer la fonction `supprimer_élève` 

```
$ git commit -m "Ajout de la fonction de supprimer_élève"
```

La commande `git commit -m "Ajout de la fonction de supprimer_élève"` est utilisée pour créer un nouveau commit dans le dépôt Git. Un commit est une capture instantanée des modifications apportées aux fichiers suivis par Git.

Explication de la commande :

* `git commit` est la commande principale pour créer un commit.
* `-m "Ajout de la fonction de supprimer_élève"` est un paramètre qui permet de spécifier le message du commit. Le message doit être placé entre guillemets.

Résultat de l'exécution de la commande :

- Si le commit est créé avec succès, Git affiche des informations sur le commit, telles que l'identifiant unique du commit (SHA-1), l'auteur, la date et le message du commit.

- Par exemple :

```
[main f7fde4f] Ajout de la fonction d'addition
1 file changed, 10 insertions(+)
```
- Le commit est enregistré dans l'historique du dépôt Git, capturant ainsi les modifications apportées aux fichiers à ce stade.

Une fois le commit créé, les modifications apportées aux fichiers sont enregistrées de manière permanente dans le dépôt Git. 

![image](https://github.com/kplr-training/Git-Github/assets/123757632/d405ffa7-778d-4020-bcc8-f0d8ba56ed4f)

### 27. Afficher l'historique des commits et vérifier que votre commit a été enregistré avec succès

```
$ git log
```

La commande `git log` est utilisée pour afficher l'historique des commits dans le dépôt Git. Lorsque vous exécutez cette commande, Git affiche une liste des commits effectués, triés du plus récent au plus ancien.

Résultat de l'exécution de la commande :

- Chaque commit est affiché avec des informations telles que l'identifiant du commit (SHA-1), l'auteur, la date et le message du commit.
- Par exemple :
  ```
  commit f7fde4f82d5e8a7574680a8e138e41c05d1e3d6e
  Author: Votre nom <votre@email.com>
  Date:   Lun. Sept. 13 10:00:00 2023 +0200

      Ajout de la fonction d'addition

  commit 2cfd3b1e8949a7b894ca57182a3b14db6c0ee43f
  Author: Autre contributeur <autre@email.com>
  Date:   Lun. Sept. 12 15:30:00 2023 +0200

      Correction de bug dans la fonction de soustraction
  ```

- Chaque commit est identifié par son identifiant unique (SHA-1). Vous pouvez utiliser cet identifiant pour référencer spécifiquement un commit.

### 28. Basculer vers la branche principale 

La commande "git checkout main" est utilisée pour basculer vers la branche principale (ou branche maître) dans un référentiel Git. La branche principale est généralement utilisée pour représenter l'état stable du projet.

```
git checkout main
```

Lorsque vous exécutez cette commande, Git met à jour votre répertoire de travail pour refléter l'état de la branche principale. Cela signifie que les fichiers dans votre répertoire de travail seront modifiés pour correspondre à l'état de la branche "main". 

![image](https://github.com/kplr-training/Git-Github/assets/123757632/fd071bba-8e5a-4ed3-a47b-b175d999aca5)

### 29. Fudionner la branche "supprimer_eleve" avec la branche "main"

La commande "git merge supprimer_eleve" fusionne la branche "supprimer_eleve" dans la branche actuelle. Plus précisément, elle incorpore les modifications de la branche "supprimer_eleve" dans la branche courante.

```
git merge supprimer_eleve
```

Lorsque vous exécutez cette commande, Git examine les modifications entre la branche actuelle et la branche "supprimer_eleve". Il essaie de fusionner automatiquement les modifications, en appliquant les changements de la branche "supprimer_eleve" sur la branche courante.

![image](https://github.com/kplr-training/Git-Github/assets/123757632/4412936d-aa0d-4a1b-a570-86a5576c06ad)

**REMARQUE : La fonction supprimer_eleve se trouve maintenant dans le ficher "gestion_eleve" dans la branche principale "main"**

### 30. Création de la nouvelle branche afficher_tous_les_eleves

```
git branch afficher_tous_les_eleves
```
La commande "git branch afficher_tous_les_eleves" est utilisée pour créer une nouvelle branche dans un référentiel Git avec le nom "modifier_eleve". 

### 31. Basculer vers la branche afficher_tous_les_eleves

La commande "git checkout afficher_tous_les_eleves" est utilisée pour basculer vers une branche spécifique dans un référentiel Git. Dans ce cas, la branche spécifique est "afficher_tous_les_eleves".

```
git checkout afficher_tous_les_eleves
```
![image](https://github.com/kplr-training/Git-Github/assets/123757632/33ded92f-7896-4cb5-ac62-a9b1d4787be3)


### 32. Ouvrez le fichier `gestion_eleves.py` et ajoutez la fonction pour afficher tous les eleves

```
élèves = {}
def afficher_tous_les_élèves():
    if élèves:
        print("Liste complète des élèves :")
        for id_élève, nom_élève in élèves.items():
            print(f"ID : {id_élève}, Nom : {nom_élève}")
    else:
        print("Aucun élève dans la liste.")
```

La fonction afficher_tous_les_élèves permet à l'utilisateur d'entrer l'identifiant et le nom d'un nouvel élève, puis le supprimer.

### 33. Ajoutez le fichier `gestion_eleves.py` au suivi de Git en utilisant la commande suivante 

```
$ git add .
```

La commande `git add .` est utilisée pour ajouter le fichier `gestion_eleves.py` au suivi de Git. Cela signifie que Git commencera à suivre les modifications apportées à ce fichier et le prendra en compte lors des futurs commits.

### 34. Création d'un premier commit pour la fonction `afficher_tous_les_élèves()` 

Créez un commit pour enregistrer la fonction `afficher_tous_les_élèves` 

```
$ git commit -m "Ajout de la fonction afficher_tous_les_élèves"
```

La commande `git commit -m "Ajout de la fonction afficher_tous_les_élèves"` est utilisée pour créer un nouveau commit dans le dépôt Git. Un commit est une capture instantanée des modifications apportées aux fichiers suivis par Git.

Explication de la commande :

* `git commit` est la commande principale pour créer un commit.
* `-m "Ajout de la fonction afficher_tous_les_élèves"` est un paramètre qui permet de spécifier le message du commit. Le message doit être placé entre guillemets.

Résultat de l'exécution de la commande :

- Si le commit est créé avec succès, Git affiche des informations sur le commit, telles que l'identifiant unique du commit (SHA-1), l'auteur, la date et le message du commit.

- Par exemple :

```
[main f7fde4f] Ajout de la fonction d'addition
1 file changed, 10 insertions(+)
```
- Le commit est enregistré dans l'historique du dépôt Git, capturant ainsi les modifications apportées aux fichiers à ce stade.

Une fois le commit créé, les modifications apportées aux fichiers sont enregistrées de manière permanente dans le dépôt Git. 

![image](https://github.com/kplr-training/Git-Github/assets/123757632/8385e429-7339-4b7a-baf7-2bef6cad8016)

### 35. Afficher l'historique des commits et vérifier que votre commit a été enregistré avec succès

```
$ git log
```

La commande `git log` est utilisée pour afficher l'historique des commits dans le dépôt Git. Lorsque vous exécutez cette commande, Git affiche une liste des commits effectués, triés du plus récent au plus ancien.

Résultat de l'exécution de la commande :

- Chaque commit est affiché avec des informations telles que l'identifiant du commit (SHA-1), l'auteur, la date et le message du commit.
- Par exemple :
  ```
  commit f7fde4f82d5e8a7574680a8e138e41c05d1e3d6e
  Author: Votre nom <votre@email.com>
  Date:   Lun. Sept. 13 10:00:00 2023 +0200

      Ajout de la fonction d'addition

  commit 2cfd3b1e8949a7b894ca57182a3b14db6c0ee43f
  Author: Autre contributeur <autre@email.com>
  Date:   Lun. Sept. 12 15:30:00 2023 +0200

      Correction de bug dans la fonction de soustraction
  ```

- Chaque commit est identifié par son identifiant unique (SHA-1). Vous pouvez utiliser cet identifiant pour référencer spécifiquement un commit.

### 36. Basculer vers la branche principale 

La commande "git checkout main" est utilisée pour basculer vers la branche principale (ou branche maître) dans un référentiel Git. La branche principale est généralement utilisée pour représenter l'état stable du projet.

```
git checkout main
```

Lorsque vous exécutez cette commande, Git met à jour votre répertoire de travail pour refléter l'état de la branche principale. Cela signifie que les fichiers dans votre répertoire de travail seront modifiés pour correspondre à l'état de la branche "main". 

![image](https://github.com/kplr-training/Git-Github/assets/123757632/890ee19a-bfae-40ba-a5bf-59d986058595)

### 37. Fudionner la branche "afficher_tous_les_eleves" avec la branche "main"

La commande "git merge afficher_tous_les_eleves" fusionne la branche "afficher_tous_les_eleves" dans la branche actuelle. Plus précisément, elle incorpore les modifications de la branche "afficher_tous_les_eleves" dans la branche courante.

```
git merge afficher_tous_les_eleves
```

Lorsque vous exécutez cette commande, Git examine les modifications entre la branche actuelle et la branche "afficher_tous_les_eleves". Il essaie de fusionner automatiquement les modifications, en appliquant les changements de la branche "afficher_tous_les_eleves" sur la branche courante.

![image](https://github.com/kplr-training/Git-Github/assets/123757632/532cd0f7-aa09-4caf-8868-58dc8bc10f53)

**REMARQUE : La fonction afficher_tous_les_élèves se trouve maintenant dans le ficher "gestion_eleve" dans la branche principale "main"**

### 38. Création de la nouvelle branche gestion_eleves

```
git branch gestion_eleves
```
La commande "git branch gestion_eleves" est utilisée pour créer une nouvelle branche dans un référentiel Git avec le nom "git branch gestion_eleves". 

### 39. Basculer vers la branche gestion_eleves

La commande "git checkout gestion_eleves" est utilisée pour basculer vers une branche spécifique dans un référentiel Git. Dans ce cas, la branche spécifique est "gestion_eleves".

```
git checkout gestion_eleves
```
![image](https://github.com/kplr-training/Git-Github/assets/123757632/d9213995-5cbb-4c1c-bfc5-68fb2985bf84)


### 40. Ouvrez le fichier `gestion_eleves.py` et ajoutez la fonction principale 

```
def gestion_eleves():
    print("Bienvenue dans la gestion des élèves !")
    while True:
        print("\nMenu :")
        print("1. Ajouter un élève")
        print("2. Modifier un élève")
        print("3. Supprimer un élève")
        print("4. Afficher la liste complète des élèves")
        print("5. Quitter")

        choix = input("Veuillez sélectionner une option (1-5) : ")

        if choix == "1":
            ajouter_élève()
        elif choix == "2":
            modifier_élève()
        elif choix == "3":
            supprimer_élève()
        elif choix == "4":
            afficher_tous_les_élèves()
        elif choix == "5":
            break
        else:
            print("Option invalide. Veuillez réessayer.")

if __name__ == "__main__":
    gestion_eleves()
```

La fonction gestion_eleves permet à l'utilisateur de selectionner une option afin d'executer les fonctions de gestion. 

### 41. Ajoutez le fichier `gestion_eleves.py` au suivi de Git en utilisant la commande suivante 

```
$ git add .
```

La commande `git add .` est utilisée pour ajouter le fichier `gestion_eleves.py` au suivi de Git. Cela signifie que Git commencera à suivre les modifications apportées à ce fichier et le prendra en compte lors des futurs commits.

### 42. Création un commit pour la fonction `gestion_eleves()` 

Créez un commit pour enregistrer la fonction `gestion_eleves()` 

```
$ git commit -m "Ajout de la fonction gestion_eleves()"
```

La commande `git commit -m "Ajout de la fonction gestion_eleves()"` est utilisée pour créer un nouveau commit dans le dépôt Git. Un commit est une capture instantanée des modifications apportées aux fichiers suivis par Git.

Explication de la commande :

* `git commit` est la commande principale pour créer un commit.
* `-m "Ajout de la fonction gestion_eleves()"` est un paramètre qui permet de spécifier le message du commit. Le message doit être placé entre guillemets.

Résultat de l'exécution de la commande :

- Si le commit est créé avec succès, Git affiche des informations sur le commit, telles que l'identifiant unique du commit (SHA-1), l'auteur, la date et le message du commit.

- Par exemple :

```
[main f7fde4f] Ajout de la fonction d'addition
1 file changed, 10 insertions(+)
```
- Le commit est enregistré dans l'historique du dépôt Git, capturant ainsi les modifications apportées aux fichiers à ce stade.

Une fois le commit créé, les modifications apportées aux fichiers sont enregistrées de manière permanente dans le dépôt Git. 

![image](https://github.com/kplr-training/Git-Github/assets/123757632/8d8ea649-b979-4f11-8006-65bea637079f)

### 43. Afficher l'historique des commits et vérifier que votre commit a été enregistré avec succès

```
$ git log
```

La commande `git log` est utilisée pour afficher l'historique des commits dans le dépôt Git. Lorsque vous exécutez cette commande, Git affiche une liste des commits effectués, triés du plus récent au plus ancien.

Résultat de l'exécution de la commande :

- Chaque commit est affiché avec des informations telles que l'identifiant du commit (SHA-1), l'auteur, la date et le message du commit.
- Par exemple :
  ```
  commit f7fde4f82d5e8a7574680a8e138e41c05d1e3d6e
  Author: Votre nom <votre@email.com>
  Date:   Lun. Sept. 13 10:00:00 2023 +0200

      Ajout de la fonction d'addition

  commit 2cfd3b1e8949a7b894ca57182a3b14db6c0ee43f
  Author: Autre contributeur <autre@email.com>
  Date:   Lun. Sept. 12 15:30:00 2023 +0200

      Correction de bug dans la fonction de soustraction
  ```

- Chaque commit est identifié par son identifiant unique (SHA-1). Vous pouvez utiliser cet identifiant pour référencer spécifiquement un commit.

### 44. Basculer vers la branche principale 

La commande "git checkout main" est utilisée pour basculer vers la branche principale (ou branche maître) dans un référentiel Git. La branche principale est généralement utilisée pour représenter l'état stable du projet.

```
git checkout main
```

Lorsque vous exécutez cette commande, Git met à jour votre répertoire de travail pour refléter l'état de la branche principale. Cela signifie que les fichiers dans votre répertoire de travail seront modifiés pour correspondre à l'état de la branche "main". 

![image](https://github.com/kplr-training/Git-Github/assets/123757632/5bcc91d3-e51b-49d6-9b69-e2a196796405)

### 45. Fudionner la branche "gestion_eleves" avec la branche "main"

La commande "git merge gestion_eleves" fusionne la branche "gestion_eleves" dans la branche actuelle. Plus précisément, elle incorpore les modifications de la branche "gestion_eleves" dans la branche courante.

```
git merge gestion_eleves
```

Lorsque vous exécutez cette commande, Git examine les modifications entre la branche actuelle et la branche "gestion_eleves". Il essaie de fusionner automatiquement les modifications, en appliquant les changements de la branche "gestion_eleves" sur la branche courante.

![image](https://github.com/kplr-training/Git-Github/assets/123757632/52dcb5ba-5e9e-4fd1-9080-cb1591cd8a61)

**REMARQUE : La fonction afficher_tous_les_élèves se trouve maintenant dans le ficher "gestion_eleve" dans la branche principale "main"**

### 46. Publier le dépôt sur [GitHub](https://github.com/) 

Créez un nouveau dépôt vide sur une plateforme de gestion de code telle que GitHub.

#### Associez le dépôt local à votre dépôt distant en utilisant la commande suivante (remplacez l'URL par celle de votre dépôt distant) 
     
```
git remote add origin <URL_du_depot distant>
```

La commande `git remote add origin <URL_du_depot_distant>` est utilisée pour associer un dépôt distant à votre dépôt Git local. L'argument `<URL_du_depot_distant>` doit être remplacé par l'URL du dépôt distant auquel vous souhaitez vous connecter. Cela peut être une URL HTTPS ou SSH, dépendant de votre configuration.

Explication de la commande :

- `git remote` est la commande pour gérer les dépôts distants.
- `add origin` est utilisé pour ajouter un nouveau dépôt distant avec le nom "origin". "origin" est souvent utilisé par convention pour désigner le dépôt distant principal.
- `<URL_du_depot_distant>` est l'URL du dépôt distant que vous souhaitez associer à votre dépôt local. Par exemple, si vous utilisez GitHub, l'URL peut ressembler à `https://github.com/votre-utilisateur/votre-depot.git`.

Résultat de l'exécution de la commande :

- Si la commande est exécutée avec succès, elle n'affiche généralement aucun message.
- L'URL du dépôt distant est enregistrée sous le nom "origin" dans votre dépôt local. Cela vous permet de référencer facilement le dépôt distant lors de l'exécution de commandes telles que `git push` ou `git pull`.


#### Poussez votre dépôt local vers le dépôt distant :

```
git push -u origin master
```

La commande `git push -u origin master` est utilisée pour pousser les commits de la branche "master" vers le dépôt distant associé à l'alias "origin". L'option `-u` est utilisée pour configurer la branche locale "master" pour qu'elle suive la branche distante "master" sur le dépôt distant "origin".

Explication de la commande :

- `git push` est la commande pour pousser les commits vers un dépôt distant.
- `-u` est une option qui permet de configurer la branche locale pour qu'elle suive la branche distante.
- `origin` est l'alias donné au dépôt distant au moment de l'association avec `git remote add origin <URL_du_depot_distant>`.
- `master` est le nom de la branche locale que vous souhaitez pousser vers le dépôt distant.

Résultat de l'exécution de la commande :

- Si la commande est exécutée avec succès et qu'il n'y a pas de problèmes de connectivité ou d'autorisations, Git pousse les commits de la branche locale "master" vers la branche distante "master" sur le dépôt distant "origin".
- Git affiche des informations sur les commits poussés, ainsi que des statistiques sur les modifications ajoutées ou supprimées.
- Par exemple :
  ```
  Enumerating objects: 5, done.
  Counting objects: 100% (5/5), done.
  Delta compression using up to 4 threads
  Compressing objects: 100% (3/3), done.
  Writing objects: 100% (3/3), 300 bytes | 300.00 KiB/s, done.
  Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
  To <URL_du_depot_distant>
     f7fde4f..2cfd3b1  master -> master
  ```
 

### 47. Vérification du dépot et des commits sur [GitHub](https://github.com/) 

![image](https://github.com/kplr-training/Git-Github/assets/123757632/9e250760-c8bf-4b88-94d4-ee43a4ca5a11)

Pour vérifier les commits dans un dépôt GitHub, vous pouvez suivre les étapes suivantes :

1. Dans l'onglet du dépôt, vous trouverez plusieurs onglets différents tels que "Code", "Issues", "Pull requests", etc. Cliquez sur l'onglet "Commits" pour afficher la liste des commits.

2. La page des commits affiche les commits dans l'ordre chronologique, du plus récent au plus ancien. Chaque commit est accompagné d'un message de commit, de l'auteur du commit, de l'heure et de la date du commit, ainsi que des statistiques sur les modifications ajoutées ou supprimées.

![image](https://github.com/kplr-training/Git-Github/assets/123757632/1d53380f-373b-4a35-8427-e0f291bf926b)

En utilisant l'interface GitHub, vous pouvez facilement visualiser l'historique des commits, examiner les modifications apportées aux fichiers et les commentaires associés à chaque commit. Cela vous permet de suivre l'évolution du dépôt et de comprendre les changements qui ont été effectués au fil du temps.

Cela conclut l'atelier d'initialisation Git avec l'ajout et le commit de chaque fonction de la calculatrice séparément. 


