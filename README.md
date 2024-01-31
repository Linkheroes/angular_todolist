# {E} - Angular ToDo List

## Step 1 : Requierements

### Installer NodeJS on Fedora

```bash
sudo dnf install -y gcc-c++ make
sudo curl -sL https://rpm.nodesource.com/setup_20.x | sudo bash - 
sudo dnf install nodejs
node -v
```

### Installer NodeJS on Arch

```bash
sudo pacman -S nodejs
node -v
```

### Installer NodeJS on Unbutu

```bash
cd ~
curl -sL https://deb.nodesource.com/setup_20.x -o /tmp/nodesource_setup.sh
sudo bash /tmp/nodesource_setup.sh
sudo apt install nodejs
node -v
```

### Installer NodeJS sur Windows ou MacOS

Download the LTS version on this [link](https://nodejs.org/en)

### Installer Angular CLI

```bash
sudo npm install -g @angular/cli
ng --version
```

## Step 2 : Créer le projet

Pour créer un nouveau projet, nous allons utiliser la commande suivante :

```bash
ng new my_todolist
cd my_todolist
```

## Step 3 : Compréhension de l'architecture du projet

Angular est un framework web en TypeScript, chaque page/component sont composé de la façon suivante :

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

Il est l'heure de créer nos premiers composants. Pour cela, nous allons utiliser la commande suivante :

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

Après avoir créer vos composants, il faut maintenant créer le tableau qui va acceuillir vos todo dans un nouveau fichier qu'on appellera "utils.ts" à la racine du dossier src/app.
Pour faire ça vous pouvez utiliser le code suivant :

```TypeScript
export interface ToDo {
  ...
}
```

## Step 7 : Associer les composants

Maintenant que nous avons nos Composant et notre interface, il faut les associer afin de créer la todo et de l'afficher.

Vous pouvez utiliser le code suivant sur une balise html pour répliquer votre component "todo" dans votre "app.component.html".

Il faudra importer dans le "app.component.ts" "CommonModule".

```TypeScript
*ngFor="..."
```

## Step 8 : Laisser parler votre imagination

Vous avez finis la base du workshop maintenant rendez votre todo list unique
