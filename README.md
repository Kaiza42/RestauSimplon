# BreafCommande - Gestion de Commandes et Clients

## Description du Projet
BreafCommande est une application conçue pour gérer les commandes d'articles de menu et les informations des clients. Ce projet combine une interface utilisateur interactive et une base de données robuste pour fournir une solution complète de gestion de commandes pour un restaurant.

---

## Fonctionnalités Principales

1. **Gestion des Clients** :
   - Ajout, modification et suppression des informations des clients.
   - Suivi des coordonnées des clients (nom, prénom, téléphone, adresse).

2. **Gestion des Articles du Menu** :
   - Création et organisation des articles dans des catégories.
   - Définition des prix et suivi des articles.

3. **Gestion des Commands** :
   - Création de commandes associées à des clients.
   - Ajout d'articles à une commande avec des quantités spécifiques.
   - Calcul automatique du total des commandes.

4. **Interface Utilisateur** :
   - Interface web utilisant HTML, CSS, et JavaScript pour la gestion des données.
   - Affichage des informations des clients, articles et commandes en temps réel.

5. **Base de Données** :
   - Base de données relationnelle utilisant SQLite pour le stockage des données.
   - Relations bien définies entre les entités (clients, commandes, articles, catégories).

---

## Structure du Projet

BreafComande est une application Web .NET 9 conçue pour gérer les commandes de restaurants. Ce projet utilise Entity Framework Core avec une base de données SQLite et comprend une feuille de style CSS simple pour styliser les pages Web.

### Dependencies

- Microsoft.EntityFrameworkCore
- Microsoft.EntityFrameworkCore.Sqlite
- Microsoft.EntityFrameworkCore.Tools
- Microsoft.AspNetCore.Diagnostics.EntityFrameworkCore
- Microsoft.AspNetCore.OpenApi
- Swashbuckle.AspNetCore
- Swashbuckle.AspNetCore.Annotations

### Backend :
- **Langage** : C# (.NET 9.0)
- **Base de données** : SQLite
- **Dossier Principal** : `BreafCommande`
  - `ClassFolder` : Contient les classes principales (Clients, Commande, ArticleDuMenu, etc.).
  - `Data` : Contient les contextes de base de données (AppDbContext).
  - `Program.cs` : Point d'entrée principal de l'application.





### Frontend :
- **Technologies** : HTML, CSS, JavaScript
- **Dossier** : `wwwroot`
  - `index.html` : Page principale.
  - `style.css` : Feuille de style pour la mise en page.
  - `script.js` : Logique interactive pour l'interface utilisateur.

---

### Fichiers et répertoires importants

- **wwwroot/CSS/StyleSheet.css** : contient les styles CSS pour l'application Web.
- **wwwroot/HTML/index.html** : le fichier HTML principal de l'application Web.
- **ClassFolder/ClientsDbContextFactory.cs** : classe Factory pour la création du contexte `ClientsDB`.
- **ClassFolder/Commande.cs** : représente l'entité `Commande`.
- **ClassFolder/CommandesDTO.cs** : objet de transfert de données pour `Commande`.
- **ClassFolder/Commande_Articles.cs** : représente l'entité `Commande_Articles`.
- **ClassFolder/Commande_ArticlesDTO.cs** : objet de transfert de données pour `Commande_Articles`.
- **ClassFolder/ClientsDTO.cs** : Objet de transfert de données pour `Clients`.
- **ClassFolder/ClientsDB.cs** : DbContext pour la gestion de `Clients`.
- **Data/AppDbContext.cs** : DbContext principal de l'application.
- **Program.cs** : Point d'entrée principal de l'application.
- **BreafComande.csproj** : Fichier de projet contenant les dépendances et les configurations de build.

### Routes

L'application expose plusieurs routes pour la gestion des clients, des catégories, des articles et des commandes. Voici les principales routes :

- **Clients**
- `GET /api/clients` : Récupérer une liste de clients.
- `GET /api/clients/{id}` : Récupérer un client spécifique par ID.
- `POST /api/clients` : Créer un nouveau client.
- `PUT /api/clients/{id}`: Mettre à jour un client existant.
- `DELETE /api/clients/{id}`: Supprimer un client.

- **Catégories**
- `GET /api/categories`: Récupérer une liste de catégories.
- `GET /api/categories/{id}`: Récupérer une catégorie spécifique par ID.
- `POST /api/categories`: Créer une nouvelle catégorie.
- `PUT /api/categories/{id}`: Mettre à jour une catégorie existante.
- `DELETE /api/categories/{id}`: Supprimer une catégorie.

- **Articles**
- `GET /api/articles`: Récupérer une liste d'articles.
- `GET /api/articles/{id}`: Récupérer un article spécifique par ID.
- `POST /api/articles`: Créer un nouvel article.
- `PUT /api/articles/{id}`: Mettre à jour un article existant.
- `DELETE /api/articles/{id}`: Supprimer un article.

- **Commandes (Orders)**
- `GET /api/commandes`: Récupérer une liste de commandes.
- `GET /api/commandes/{id}`: Récupérer une commande spécifique par ID.
- `POST /api/commandes`: Créer une nouvelle commande.
- `PUT /api/commandes/{id}`: Mettre à jour une commande existante.
- `DELETE /api/commandes/{id}`: Supprimer une commande.

### Utilisation

Pour utiliser des fichiers statiques, supprimez le commentaire de la ligne suivante dans `Program.cs` :

### Installation et Exécution

### Prérequis :
1. Visual Studio 2022 ou une version ultérieure.
2. SDK .NET 6 installé.
3. Navigateur moderne (Chrome, Firefox, Edge, etc.).

### Étapes :

1. **Cloner le Projet** :
   ```bash
   git clone <URL-du-dépôt>
   cd BreafCommande
   ```

2. **Configurer le Backend** :
   - Ouvrez le projet dans Visual Studio.
   - Restaurez les dépendances avec la commande :
     ```bash
     dotnet restore
     ```
   - Appliquez les migrations pour initialiser la base de données :
     ```bash
     dotnet ef database update
     ```

3. **Exécuter le Serveur** :
   - Lancez le projet avec :
     ```bash
     dotnet run
     ```
   - L'API sera disponible sur `http://localhost:5000` par défaut.

4. **Configurer le Frontend** :
   - Accédez au dossier `wwwroot` et ouvrez `index.html` dans votre navigateur.
   - Vérifiez les interactions entre le backend et l'interface.

---

## Utilisation

### Interface Web :
1. **Clients** :
   - Ajoutez de nouveaux clients avec leurs informations personnelles.
   - Mettez à jour ou supprimez des entrées.

2. **Articles du Menu** :
   - Ajoutez de nouveaux articles et organisez-les par catégorie.
   - Modifiez ou supprimez des articles existants.

3. **Commandes** :
   - Créez des commandes pour les clients.
   - Ajoutez ou modifiez les articles dans une commande.
   - Affichez les totaux et les détails de chaque commande.

---

## Contribution

1. **Forkez le projet** :
   ```bash
   git fork <URL-du-dépôt>
   ```

2. **Créez une branche pour vos modifications** :
   ```bash
   git checkout -b feature/nouvelle-fonctionnalité
   ```

3. **Soumettez une Pull Request** :
   - Décrivez les modifications apportées.

---

## Licence

Ce projet est sous licence MIT. Voir le fichier `LICENSE` pour plus d'informations.

---

## Contact

- **Nom** : Jean Dupont
- **Email** : exemple@gmail.com
- **Site Web** : [Votre Site](https://Votre-site.com)

---

Merci d'utiliser BreafCommande !
