# {E} - Angular ToDo List

## Step 1 : Requierements

### Installer NodeJS sur Fedora

```bash
sudo dnf install -y gcc-c++ make
sudo curl -sL https://rpm.nodesource.com/setup_20.x | sudo bash - 
sudo dnf install nodejs
node -v
```

### Installer NodeJS sur Arch

```bash
sudo pacman -S nodejs
node -v
```

### Installer NodeJS sur Unbutu

```bash
cd ~
curl -sL https://deb.nodesource.com/setup_20.x -o /tmp/nodesource_setup.sh
sudo bash /tmp/nodesource_setup.sh
sudo apt install nodejs
node -v
```

### Installer NodeJS sur Windows ou MacOS

Télécharger la dernière version dite LTS sur le lien suivant [nodejs.org](https://nodejs.org/en)

### Installer Angular CLI

```bash
sudo npm install -g @angular/cli
ng version
```

## Step 2 : Créer le projet

Pour créer un nouveau projet, nous allons utiliser la commande suivante :

```bash
ng new my_todolist
cd my_todolist
```

## Step 3 : Compréhension de l'architecture du projet

Angular est un framework web en TypeScript, chaque page/component sont composés de la façon suivante :

```
- app.component.html --> pour la partie visuel du site en html
- app.component.css/scss --> pour la partie visuel du site en css/scss
- app.component.ts --> Pour écrire toutes vos fonctions
- app.component.spec.ts --> pour effectuer des tests
```

## Step 4 : Lancer l'environnement de développement

Pour lancer le site, nous allons utiliser la commande suivante :

```bash
npm run start
```

## Step 5 : Créer de nouveaux composants

Il est l'heure de créer nos premiers composant. Pour cela, nous allons utiliser la commande suivante :

```bash
ng generate component todo
```

Pour appeler votre component dans votre front il suffit de l'appeler de la façon suivante:

```html
<app-todo></app-todo>
```

Vous pouvez passer des input à votre component en ajoutant ce code dans votre component.ts

```TypeScript
@Input() name: string = ""
```

## Step 6 : Créer une interface

Après avoir créé vos composants, il faut maintenant créer le tableau qui va acceuillir vos todo dans un nouveau fichier qu'on appellera "utils.ts" à la racine du dossier src/app.
Pour faire ça vous pouvez utiliser le code suivant :

```TypeScript
export interface ToDo {
  ...
}
```

Une interface est un équivalent au strucutre en C mais ça ne fonctionne pas tout à fait pareil.

Il suffira de déclarer la liste comme suit dans le fichier ``app.component.ts`` :

```TypeScript
todoList: ToDo[] = [];
```

## Step 7 : Associer les composants

Maintenant que nous avons nos composants et notre interface, il faut les associer afin de créer la todo et de l'afficher.

Vous pouvez utiliser le code suivant sur une balise html pour répliquer votre component "todo" dans votre "app.component.html".

```TypeScript
*ngFor="..."
```
Le *ngFor à besoin pour fonctionner d'un import nommé "CommonModule" qui devra être importé dans le fichier "app.component.ts".

## Step 8 : Ajouter dans la liste

Pour ce faire, il faudra créer une fonction assignable à un élement hmtl / component avec la propriété ``(click)=""``.

Vous pouvez utiliser le code suivant afin d'ajouter un élement à la liste:

```TypeScript
let test: ToDo {
...
}

this.todoList.push(test);
```

## Step 9 : Laissez parler votre imagination

Vous avez finis la base du workshop! Maintenant rendez votre todo list unique en ajoutant des fonctions pour les modifier, supprimer, classifier par type/importance.
