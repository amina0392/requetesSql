# RequêtesSql

# Exercice Basic 1
- SELECT * FROM `plat` WHERE 1;
  
# Exercice Basic 2
- SELECT `DetailPlat`, `Prix` FROM `plat` WHERE `Prix` > 4 AND `Prix` < 5;
  
# Exercice Basic 3
- SELECT `DateLogique`, DATE_FORMAT(`DateLogique`, '%e %M %Y', 'fr-FR') AS date_formatee
FROM `commande` WHERE `DateLogique` = '22-05-13';

# Exercice Basic 4
- SELECT
    `NumeroServeur`,
    DATE_FORMAT(`DateLogique`, '%e %M %Y') AS date_formatee,
    `NumeroCommande`
FROM
    `commande`
ORDER BY
    `NumeroServeur`,
    `DateLogique`;
  
  # Exercice Basic 5
  - SELECT `DateLogique`, COUNT(*) AS `NumeroCommande`
FROM `commande`
GROUP BY `DateLogique`
ORDER BY `DateLogique`;

# Exercice Medium 6
- SELECT AVG(`Prix`) AS prix_moyen
FROM `plat`
WHERE `Prix` > 5;

# Exercice Medium 7
- SELECT AVG(nombre_commandes) AS moyenne_commandes_par_jour
FROM (
    SELECT COUNT(*) AS nombre_commandes
    FROM `commande`
    GROUP BY DATE(`DateLogique`) 
)sous_requete;


  
