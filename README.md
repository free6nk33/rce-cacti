Ce script Bash exploite une vulnérabilité potentielle dans les installations de Cacti Monitoring pour tenter de récupérer des informations sensibles, comme des clés d'accès AWS (AKIA keys), depuis les fichiers de configuration sur le serveur ciblé.
Fonctionnalités :

Exploit sur des domaines multiples : Le script lit un fichier contenant des domaines et exécute une exploitation sur chaque domaine en utilisant une URL spécifique pour tenter d'accéder aux fichiers AWS credentials.
Récupération de clés AWS (AKIA) : Il envoie une requête pour récupérer le fichier .aws/credentials et extrait les clés AWS si elles sont présentes.
Sauvegarde dans un fichier de sortie : Si des clés AWS sont trouvées, elles sont enregistrées dans un fichier de sortie spécifié.
Utilisation d'un service interactif : Le script prend en compte une URL Interactsh pour recevoir les interactions après l'exploitation.

Utilisation :

    ./exp.sh <fichier_de_domaines> <interactsh_url> <fichier_de_sortie>

<fichier_de_domaines> : Fichier contenant une liste de domaines à tester.
<interactsh_url> : URL d'interaction pour recueillir les retours d'exploitation.
<fichier_de_sortie> : Fichier où seront stockées les clés AWS trouvées.
