# MediLink
Sujet proposé : MediLink
Application de prise de rendez-vous et de suivi médical

Type :  Application web et mobile de gestion de rendez-vous médicaux et de suivi patient.

Idée : 

MediLink permet aux patients de :
•	rechercher un professionnel de santé,
•	prendre rendez-vous en ligne,
•	recevoir des rappels,
•	consulter leur historique de rendez-vous,
•	déposer des documents médicaux.
Elle permet aussi aux médecins de :
•	gérer leur agenda,
•	consulter les demandes de rendez-vous,
•	suivre les patients,
•	partager des ordonnances ou comptes rendus.

# 2. Décrire l’application

L’objectif de MediLink est de simplifier l’accès aux soins en centralisant la prise de rendez-vous, le suivi administratif et certains échanges entre patients et professionnels de santé.

Cette application répond à plusieurs problèmes :

•	difficulté à obtenir rapidement un rendez-vous,
•	appels téléphoniques trop longs pour réserver,
•	oublis de rendez-vous,
•	mauvaise organisation des dossiers et documents,
•	manque de visibilité sur les disponibilités des médecins,
•	surcharge administrative pour les secrétariats médicaux.

L’application est utile car elle :

•	fait gagner du temps aux patients,
•	réduit les appels téléphoniques,
•	améliore l’organisation des cabinets,
•	limite les rendez-vous oubliés grâce aux rappels,
•	facilite le suivi des documents médicaux.
 
# 3. Fonctionnalités principales

Côté patient :

•	créer un compte,
•	se connecter,
•	modifier son profil,
•	rechercher un médecin par spécialité, ville ou nom,
•	consulter les créneaux disponibles,
•	prendre rendez-vous,
•	annuler ou déplacer un rendez-vous,
•	recevoir des rappels par notification ou email,
•	consulter l’historique des rendez-vous,
•	déposer des documents médicaux,
•	consulter des ordonnances ou comptes rendus,
•	laisser un avis sur le praticien.

Côté médecin :

•	créer un compte professionnel,
•	renseigner sa spécialité,
•	définir ses horaires de consultation,
•	ouvrir ou fermer des créneaux,
•	consulter son agenda,
•	accepter ou refuser certaines demandes,
•	consulter le dossier administratif du patient,
•	déposer une ordonnance,
•	déposer un compte rendu,
•	suivre l’historique des rendez-vous.

Côté administrateur :

•	gérer les comptes utilisateurs,
•	vérifier les comptes médecins,
•	modérer les avis,
•	superviser la plateforme,
•	gérer les catégories de spécialités médicales,
•	consulter des statistiques globales.
 
# Étape 1 — 4. Liste brute des fonctionnalités
•	créer un compte patient
•	créer un compte médecin
•	se connecter
•	se déconnecter
•	réinitialiser le mot de passe
•	modifier son profil
•	rechercher un médecin
•	filtrer par spécialité
•	filtrer par ville
•	consulter les créneaux disponibles
•	réserver un rendez-vous
•	annuler un rendez-vous
•	reporter un rendez-vous
•	recevoir un rappel
•	consulter l’historique des rendez-vous
•	déposer un document médical
•	consulter un document médical
•	déposer une ordonnance
•	déposer un compte rendu
•	laisser un avis
•	modérer les avis
•	gérer les horaires du médecin
•	ouvrir ou fermer des créneaux
•	gérer les comptes
•	valider les comptes médecins
•	consulter les statistiques de la plateforme
 
# Étape 2 - 5. Tri des fonctionnalités par domaines métiers

Domaine 1 : Gestion des utilisateurs

Fonctionnalités :
•	créer un compte patient
•	créer un compte médecin
•	se connecter
•	se déconnecter
•	réinitialiser le mot de passe
•	modifier son profil
•	gérer les comptes
•	valider les comptes médecins
Rôle :
Ce domaine gère l’identité, les droits et les profils.
 
Domaine 2 : Annuaire médical
Fonctionnalités :
•	rechercher un médecin
•	filtrer par spécialité
•	filtrer par ville
Rôle :
Permet de trouver un praticien adapté.
 
Domaine 3 : Gestion des rendez-vous
Fonctionnalités :
•	consulter les créneaux disponibles
•	réserver un rendez-vous
•	annuler un rendez-vous
•	reporter un rendez-vous
•	consulter l’historique des rendez-vous
•	gérer les horaires du médecin
•	ouvrir ou fermer des créneaux
Rôle :
C’est le cœur fonctionnel de l’application.
 
Domaine 4 : Documents médicaux
Fonctionnalités :
•	déposer un document médical
•	consulter un document médical
•	déposer une ordonnance
•	déposer un compte rendu
Rôle :
Centraliser les documents liés au suivi du patient.
 
Domaine 5 : Notifications
Fonctionnalités :
•	recevoir un rappel
Rôle :
Prévenir les utilisateurs pour éviter les oublis.
 
Domaine 6 : Administration et qualité
Fonctionnalités :
•	laisser un avis
•	modérer les avis
•	consulter les statistiques de la plateforme
Rôle :
Améliorer la qualité du service et superviser la plateforme.

# 6. Modules de conception
À partir des domaines métiers, on déduit les modules suivants :
•	UserManagement
•	DoctorDirectory
•	AppointmentManagement
•	MedicalDocumentManagement
•	NotificationManagement
•	Administration

# Étape 3 — Entités métier principales
Utilisateur

•	id
•	nom
•	prénom
•	email
•	motDePasse
•	rôle
•	téléphone

Patient

•	idPatient
•	numéroSécuritéSociale
•	dateNaissance
•	adresse

Médecin

•	idMedecin
•	spécialité
•	numéroRPPS
•	ville
•	adresseCabinet

Créneau

•	idCréneau
•	date
•	heureDébut
•	heureFin
•	disponibilité

RendezVous

•	idRendezVous
•	dateHeure
•	statut
•	motif
•	patient
•	médecin
•	créneau

DocumentMedical

•	idDocument
•	typeDocument
•	fichier
•	dateDepot
•	patient
•	médecin

Avis

•	idAvis
•	note
•	commentaire
•	date
•	patient
•	médecin

Notification

•	idNotification
•	type
•	contenu
•	dateEnvoi
•	statut


