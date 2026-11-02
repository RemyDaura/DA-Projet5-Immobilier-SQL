# Projet 5 : Conception d'une base de données immobilière (SQL)

### Contexte
Le projet **DATAImmo** vise à améliorer la prévision des prix immobiliers. Première phase : concevoir une base qui consolide les transactions immobilières (DVF), les données de population de l'INSEE et un référentiel géographique.

**Mon objectif :** passer de données brutes et éclatées à une base normalisée, conforme et déjà exploitable pour trois besoins : la valorisation (cibler les biens de luxe), la pression démographique (dynamisme du marché) et la segmentation (prix selon le type de bien).

### Missions réalisées
* **Dictionnaire de données :** atomicité des variables, typage précis, et vérification qu'aucune donnée personnelle n'est stockée.
* **Modélisation en 3NF :** 5 entités liées en cascade (VENTE, BIEN, COMMUNE, DÉPARTEMENT, RÉGION) pour analyser un bien à n'importe quel niveau géographique sans dupliquer d'information.
* **Création de la base sous MySQL :** conversion des dates en type DATE, clés étrangères activées, index sur la colonne géographique la plus sollicitée.
* **Requêtes analytiques :**
    * classement des 3 communes les plus chères par département avec `RANK() OVER (PARTITION BY ...)` ;
    * nombre de transactions pour 1 000 habitants ;
    * prix au m² des 2 et 3 pièces comparés en une seule requête (`AVG` avec `CASE WHEN`).

### Résultats
* **5 entités** normalisées, sans redondance.
* **3 requêtes stratégiques** livrées et fonctionnelles.
* Aucune donnée personnelle stockée : base conforme au RGPD.

### Compétences & Outils
* **Outils :** MySQL, SQL
* **Techniques :** modélisation (MCD / MLD, 3NF), contraintes d'intégrité, index, fonctions de fenêtre, agrégation conditionnelle

### Contenu du dépôt
* `data-raw/` : transactions DVF, données des communes, référentiel géographique
* `reports/` : dictionnaire de données et présentation
* `images/` : captures d'écran

<img src="images/Capture d'écran 2025-11-05 153104.png" width="500px"><img src="images/Capture d'écran 2025-11-05 153124.png" width="500px">
<img src="images/Capture d'écran 2025-11-05 152744.png" width="500px"><img src="images/Capture d'écran 2025-11-05 152755.png" width="500px">

---
📂 Dossier complet sur mon portfolio : [remydaura.github.io/p5.html](https://remydaura.github.io/p5.html)

*Ce projet fait partie de la formation Data Analyst d'OpenClassrooms.*
