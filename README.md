# Exercices Hive du cours de big data

## Préparation

Vous devriez avoir ces données sur HDFS:

``` 
bigdata@bigdatavm:~$ hadoop fs -ls /user/bigdata/ontime
Found 12 items
-rw-r--r--   3 bigdata supergroup  185023020 2014-03-04 23:35 /user/bigdata/ontime/On_Time_On_Time_Performance_2013_1.tsv
-rw-r--r--   3 bigdata supergroup  194935678 2014-03-04 23:35 /user/bigdata/ontime/On_Time_On_Time_Performance_2013_10.tsv
-rw-r--r--   3 bigdata supergroup  183225311 2014-03-04 23:35 /user/bigdata/ontime/On_Time_On_Time_Performance_2013_11.tsv
-rw-r--r--   3 bigdata supergroup  188932831 2014-03-04 23:35 /user/bigdata/ontime/On_Time_On_Time_Performance_2013_12.tsv
-rw-r--r--   3 bigdata supergroup  170321373 2014-03-04 23:35 /user/bigdata/ontime/On_Time_On_Time_Performance_2013_2.tsv
-rw-r--r--   3 bigdata supergroup  200623175 2014-03-04 23:35 /user/bigdata/ontime/On_Time_On_Time_Performance_2013_3.tsv
-rw-r--r--   3 bigdata supergroup  195092875 2014-03-04 23:35 /user/bigdata/ontime/On_Time_On_Time_Performance_2013_4.tsv
-rw-r--r--   3 bigdata supergroup  199565735 2014-03-04 23:35 /user/bigdata/ontime/On_Time_On_Time_Performance_2013_5.tsv
-rw-r--r--   3 bigdata supergroup  201444620 2014-03-04 23:36 /user/bigdata/ontime/On_Time_On_Time_Performance_2013_6.tsv
-rw-r--r--   3 bigdata supergroup  208462555 2014-03-04 23:36 /user/bigdata/ontime/On_Time_On_Time_Performance_2013_7.tsv
-rw-r--r--   3 bigdata supergroup  204895171 2014-03-04 23:36 /user/bigdata/ontime/On_Time_On_Time_Performance_2013_8.tsv
-rw-r--r--   3 bigdata supergroup  185449053 2014-03-04 23:36 /user/bigdata/ontime/On_Time_On_Time_Performance_2013_9.tsv
``` 

Si vous ne les avez pas, allez chercher les fichiers sur R:\H14N\INF-O17 gr.000001\documents. Vous devez monter un lecteur réseau avec l'adresse de votre machine (avec l'adresse \\<adresse IP>\data dans l'explorateur windows) puis y extraire les fichiers. Finalement, vous devez copier les fichiers sur HDFS à l'aide de la commande

``` 
hadoop fs -put <les fichiers a mettre> /user/bigdata/ontime
``` 

## Création de la table Hive

    cd /data/bigdata-exercices-hive
	hive -f import.q

Vous pouvez voir le contenu du fichier qui importe les données à https://github.com/jfim/bigdata-exercices-hive/blob/master/create.q

## Activation de Apache Hue

Voir instructions en classe.

## Questions

- Combien de vols est-ce que chaque compagnie aerienne a opéré en 2013?
- Quelle paire d'aéroports à eu le plus de vols en 2013?
- Quel avion a le plus volé en 2013? Quel quantité de milles a-t-il volé? Est-il arrivé plus en retard que la moyenne?
- En moyenne, quelle compagnie aerienne a le plus de retards?
- Quel mois est-ce qu'il y a le plus de retards? Quelle heure? Quel jour de la semaine?
- Quel jour de l'année est-ce qu'il y a le plus d'annulations de vols?
- Est-ce qu'il y a une correlation entre la duree d'un vol et la quantite de retards?
- Quels conseils donneriez-vous a quelqu'un qui veut eviter d'etre en retard?

## Questions avec le nouvel ensemble de données

- Quel est le fabriquant de l'avion ayant le plus volé en 2013 (ex: Boeing, Airbus, etc.)
- Est-ce qu'il y a une différence entre les retards et les annulations de vol par manufacturier?
- Est-ce qu'il y a une différence de vitesse entre les divers types de moteurs d'avion? Quel est la vitesse moyenne de chaque type de moteur?
