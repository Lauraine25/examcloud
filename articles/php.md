# Introduction à PHP : Un Guide Complet pour Débutants

PHP (Hypertext Preprocessor) est un langage de programmation côté serveur largement utilisé pour le développement web. Il permet de créer des sites dynamiques et interactifs, et s'intègre facilement avec des bases de données comme MySQL.

## Pourquoi choisir PHP ?

PHP est un langage très populaire, voici pourquoi :

- **Facile à apprendre** : Syntaxe simple et intuitive.
- **Compatible avec plusieurs bases de données** : MySQL, PostgreSQL, SQLite, etc.
- **Communauté active** : Beaucoup de documentation et de forums d'entraide.
- **Gratuit et open-source** : Disponible sur toutes les plateformes.
- **Excellente intégration avec HTML et CSS**.

## Installation de PHP

Avant de commencer, il faut installer PHP sur votre machine. Voici comment faire :

### Sous Windows (avec XAMPP) :
1. Téléchargez [XAMPP](https://www.apachefriends.org/fr/index.html).
2. Installez-le et démarrez **Apache** et **MySQL**.
3. Placez vos fichiers PHP dans le dossier `htdocs`.

### Sous Linux :
```sh
sudo apt update
sudo apt install php
```

### Vérification de l'installation :

Pour vérifier que PHP est bien installé, ouvrez un terminal et tapez :
```sh
php -v
```

## Écrire son premier script PHP

Créez un fichier `index.php` et insérez le code suivant :

```php
<?php
  echo "Hello, World!";
?>
```

Puis ouvrez ce fichier dans un navigateur via `http://localhost/index.php`.

## Concepts de base en PHP

### 1. Les Variables

En PHP, les variables commencent par un `$` et ne nécessitent pas de déclaration explicite de type.

```php
<?php
$name = "Alice";
$age = 25;
echo "Nom: $name, Age: $age";
?>
```

### 2. Structures de contrôle

#### Condition IF
```php
<?php
$age = 18;
if ($age >= 18) {
    echo "Vous êtes majeur.";
} else {
    echo "Vous êtes mineur.";
}
?>
```

#### Boucle FOR
```php
<?php
for ($i = 1; $i <= 5; $i++) {
    echo "Compteur: $i <br>";
}
?>
```

### 3. Fonctions en PHP

```php
<?php
function saluer($nom) {
    return "Bonjour, $nom !";
}

echo saluer("Alice");
?>
```

### 4. Formulaires et Méthodes GET/POST

```php
<form method="POST" action="traitement.php">
    Nom: <input type="text" name="nom">
    <input type="submit" value="Envoyer">
</form>
```

Dans `traitement.php` :
```php
<?php
if ($_SERVER["REQUEST_METHOD"] == "POST") {
    $nom = htmlspecialchars($_POST["nom"]);
    echo "Bonjour, $nom !";
}
?>
```

## Aller plus loin

- **Connexion à une base de données MySQL avec PDO**
- **Gestion des sessions et cookies**
- **Utilisation d'un framework comme Laravel**

PHP reste un langage puissant et incontournable pour le développement web. Bonne programmation ! 🎉
