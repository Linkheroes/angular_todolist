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

## Step 3 : Lancer l'environnement de développement

Pour lancer le site, nous allons utiliser la commande suivante :

```bash
npm run start
```

## Step 4 : Créer de nouveaux composants

Il est l'heure de créer nos premiers composants. Pour cela, nous allons utiliser la commande suivante :

```bash
ng generate component todo
```

## Step 5 : Créer une interface

Après avoir créer vos composants, il faut maintenant créer le tableau qui va acceuillir vos todo.
Pour faire ça vous pouvez utiliser le code suivant :

```TypeScript
export interface ToDo {
  ...
}
```

## Step 6 : Associer les composants

Maintenant que nous avons nos Composant et notre interface, il faut les associer afin de créer la todo et de l'afficher.

## Step 7 : Laisser parler votre imagination

Vous avez finis la base du workshop maintenant rendez votre todo list unique
