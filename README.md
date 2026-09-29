
# -ProjetDB_Chapotot_Razouk
Premier miniprojet Base de donnée


<img width="1907" height="1012" alt="image" src="https://github.com/user-attachments/assets/894e7239-97fb-4b6f-8546-c8a759bd8d66" />


Tu travailles dans le domaine de l’exploration spatiale. Ton organisation a pour activité de concevoir, préparer, lancer et suivre des missions spatiales à objectifs scientifiques et technologiques. C’est une agence spatiale comme la NASA, l’ESA ou la JAXA. [AJOUTER UNE LISTE DE CE SUR QUOI LES DONNEES ONT ETE COLLECTEES, SANS ETRE TROP PRECIS]. Inspire-toi [du site web / de la présentation / de l’article] suivant : [A COMPLETER AVEC DES REFERENCES].
Ton organisation veut appliquer MERISE pour concevoir un système d'information. Tu es chargé de la partie analyse, c’est-à-dire de collecter les besoins auprès de l’entreprise. Elle a fait appel à un étudiant en ingénierie informatique pour réaliser ce projet, tu dois lui fournir les informations nécessaires pour qu’il applique ensuite lui-même les étapes suivantes de conception et développement de la base de données.
D’abord, établis les règles de gestions des données de ton organisation, sous la forme d'une liste à puce. Elle doit correspondre aux informations que fournit quelqu’un qui connaît le fonctionnement de l’entreprise, mais pas comment se construit un système d’information.
Ensuite, à partir de ces règles, fournis un dictionnaire de données brutes avec les colonnes suivantes, regroupées dans un tableau : signification de la donnée, type, taille en nombre de caractères ou de chiffres. Il doit y avoir entre 25 et 35 données. Il sert à fournir des informations supplémentaires sur chaque donnée (taille et type) mais sans a priori sur comment les données vont être modélisées ensuite.
Fournis donc les règles de gestion et le dictionnaire de données.


1. AGENCE — 4 données
agence_id
agence_nom
agence_pays
agence_date_creation
2. MISSION — 6 données
mission_id
mission_nom
mission_date_debut
mission_date_fin
mission_statut
mission_type
3. SITE DE LANCEMENT — 4 données
site_id
site_nom
site_pays
site_localisation
4. LANCEUR — 3 données
lanceur_id
lanceur_nom
lanceur_constructeur
5. ENGIN SPATIAL — 4 données
e_id
e_nom
e_type
e_masse
6. ASTRONAUTE — 4 données
astronaute_id
astronaute_nom
astronaute_prénom
astronaute_nationalité
7. INSTRUMENT — 3 données
instrument_id
instrument_nom
instrument_type
8. CORPS CÉLESTE — 3 données
c_id
c_nom
c_type
9. OBJECTIF — 3 données
objectif_id
objectif_description
objectif_type
10. PARTICIPER — 1 donnée
astronaute_role
astronaute_role est un attribut de l'association PARTICIPER, et non une donnée de l'entité ASTRONAUTE.



1. Règles de gestion
* L’agence spatiale organise et supervise plusieurs missions spatiales.
* Une mission spatiale est organisée par une seule agence spatiale.
* Chaque agence spatiale possède un nom, un pays d’origine et une date de création.
* Une mission possède un nom, une date de début prévue, une date de fin prévue et un état d’avancement.
* Une mission utilise un lanceur pour être envoyée dans l’espace.
* Un lanceur est fabriqué par un constructeur et possède un nom.
* Une mission peut utiliser un ou plusieurs engins spatiaux.
* Un engin spatial possède un nom, un type et une masse.
* Une mission habitée peut accueillir plusieurs astronautes.
* Un astronaute peut participer à plusieurs missions au cours de sa carrière.
* Chaque astronaute possède un nom, un prénom et une nationalité.
* Une mission peut avoir pour destination ou pour objet d’étude un ou plusieurs corps célestes.
* Un corps céleste possède un nom et un type, par exemple planète, lune, astéroïde ou comète.
* Une mission peut embarquer plusieurs instruments scientifiques.
* Un instrument scientifique possède un nom et un type.
* Un même type d’instrument peut être utilisé dans plusieurs missions.
* Une mission se déroule en plusieurs phases successives.
* Chaque phase d’une mission possède un nom permettant d’identifier son étape, par exemple lancement, transit, mise en orbite ou exploration.



  
Dictionnaire de données brutes


* Donnée	              Signification de la donnée	          Type	  Taille
* agence_id	            Identifiant de l'agence spatiale	    Entier	5 chiffres
* agence_nom	          Nom de l'agence spatiale	            Texte	  60 caractères
* agence_pays	          Pays d'origine de l'agence spatiale	  Texte	  40 caractères
* agence_date_creation  Date de création de l'agence spatiale Date	  10 caractères
* mission_id            Identifiant de la mission spatiale	  Entier	6 chiffres
* mission_nom	          Nom de la mission spatiale	          Texte	  80 caractères
* mission_date_debut	  Date de début de la mission	          Date	  10 caractères
* mission_date_fin	    Date de fin de la mission	            Date	  10 caractères
* mission_statut	      État actuel de la mission	            Texte	  30 caractères
* mission_type	        Type de mission spatiale	            Texte	  40 caractères
* site_id	              Identifiant du site de lancement	    Entier	6 chiffres
* site_nom	            Nom du site de lancement	            Texte	  80 caractères
* site_pays	            Pays où se situe le site de lancement	Texte	  40 caractères
* site_localisation	    Localisation du site de lancement	    Texte	  100 caractères
* lanceur_id	          Identifiant du lanceur	              Entier	5 chiffres
* lanceur_nom	          Nom du lanceur	                      Texte	  60 caractères
* lanceur_constructeur	Nom du constructeur du lanceur	      Texte	  60 caractères
* e_id	                Identifiant de l'engin spatial	      Entier	6 chiffres
* e_nom	                Nom de l'engin spatial	              Texte	  80 caractères
* e_type	              Type d'engin spatial	                Texte	  40 caractères
* e_masse	              Masse de l'engin spatial	            Nb décimal	8 chiffres
* astronaute_id	        Identifiant de l'astronaute	          Entier	6 chiffres
* astronaute_nom	      Nom de famille de l'astronaute	      Texte	  40 caractères
* astronaute_prénom	    Prénom de l'astronaute	              Texte	  40 caractères
* astronaute_nationalité	Nationalité de l'astronaute	        Texte	  40 caractères
* astronaute_role	      Rôle de l'astronaute lors de sa participation à la mission	Texte	40 caractères
* c_id	                Identifiant du corps céleste	        Entier	6 chiffres
* c_nom	                Nom du corps céleste	                Texte	  50 caractères
* c_type	              Type de corps céleste	                Texte	  30 caractères
* instrument_id	        Identifiant de l'instrument scientifique	Entier	6 chiffres
* instrument_nom	      Nom de l'instrument scientifique	    Texte  	80 caractères
* instrument_type	      Type d'instrument scientifique	      Texte	  40 caractères
* objectif_id	          Identifiant de l'objectif	            Entier	6 chiffres
* objectif_description	Description de l'objectif de la mission	Texte	150 caractères
* objectif_type	        Type d'objectif de la mission	Texte	40 caractères


























