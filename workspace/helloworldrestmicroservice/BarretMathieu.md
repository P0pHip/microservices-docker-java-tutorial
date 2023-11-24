QUESTION 1: POURQUOI SUR ECLIPSE LA CONFIGURATION D'EXECUTION EST DEJA PRESENTE ? 

-La configuration d'execution est deja presente grâce à maven. 

QUESTION 2: QUELLE SERAIT LA COMMANDE A UTILISER SOUS WINDOWS ? ET EXPLIQUER POURQUOI ? 

-java -cp 'target/classes;target/dependency/*' com.kumuluz.ee.EeApplication
et parce que c'est pour ça

QUESTION 3: QUELLE DIFFÉRENCE ENTRE UNE IMAGE ET UN CONTENEUR ?

-Une image est un capture instantané d'un conteneur, elles sont stockés dans un registre docker. Un conteneur docker est une instance exécutable d'une image. 

QUESTION 4: POURQUOI QUAND VOUS FAITES UN "DOCKER HISTORY REDIS" VOUS N OBTENEZ PAS 
LA MÊME CHOSE 	QUE LE TEXTE AFFICHÉ À L ÉCRAN ?

-On obtient pas la même chose car la date de création de l'image docker s'actualise.


QUESTION 5: QUELLE EST L'OPTION (CLI) QUI PERMET DE SUPPRIMER UN CONTENEUR APRÈS SON ARRÊT ?

-docker run -rm

QUESTION 6: RETOURNER LE RÉSULTAT DE CURL (FIN EXERCICE) EN MODIFIANT LE MESSAGE TRANSMIS AU SERVICE WEB.

curl -H "Content-Type: application/json" -X POST -d '{"message":"Hello Mathieu Barret"}' http://localhost:8080/helloworld
pophip@pophip-HP-Laptop:~$ curl http://localhost:8080/helloworld
[{"rid":2,"message":"Hello Mathieu Barret","startDate":"Thu Sep 28 16:08:31 CEST 2023"},{"rid":1,"message":"Mon HelloWorld","startDate":"Thu Sep 28 16:05:48 CEST 2023"}]pophip@pophip-HP-Laptop:~$

QUESTION 7: CORRIGER LE DOCKERFILE AFIN D'UTILISER COMPLÈTEMENT LA VARIABLE D'ENVIRONEMENT ET CHANGER LA VERSION DE MAVEN 

changer "ENV MAVEN_VERSION 3.8.5" en "ENV MAVEN_VERSION 3.8.8" et modifier :
" maven/maven-3/3.8.5/binaries/apache-maven-$MAVEN_VERSION "
en :
" maven/maven-3/$MAVEN_VERSION/binaries/apache-maven-$MAVEN_VERSION "

cf Dockerfile pour plus de lisibilité.









