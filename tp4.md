#TP4

- Ecrire le code de création de 3 nouvelles tables dans la base de données YnovPrem (script.sql)
- Copier le code de votre machine vers votre container Mysql
- Import le fichier
- Checker l’existence des données importées

## Etapes:
- Créer un répertoire sur votre machine (docker) et créer un fichier .sql dans ce répertoire
- Ecrivez votre script dans ce fichier .sql
    Une fois terminé, exécuter la commande `docker cp path_du_fichier id_container:path_ou_sauvegarder_le_fichier`
- Connectez-vous au container puis rendez-vous dans le répertoire du fichier
- Connectez-vous à Mysql puis exécuter SOURCE le_nom_du_fichier.sql
