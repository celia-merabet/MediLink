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

Domaine 1 : Gestion des utilisateurs et authentification

Fonctionnalités :

créer un compte patient
créer un compte médecin
se connecter
se déconnecter
réinitialiser le mot de passe
modifier son profil
gérer les comptes
valider les comptes médecins

Rôle :
Gérer l’identité, les rôles (patient/médecin) et la sécurité des accès

 Domaine 2 : Annuaire médical

Fonctionnalités :

rechercher un médecin
filtrer par spécialité
filtrer par ville

Rôle :
Permettre aux patients de trouver facilement un médecin.

Domaine 3 : Gestion des créneaux

Fonctionnalités :

créer des créneaux
modifier les créneaux
supprimer des créneaux
consulter les disponibilités

Rôle :
Gérer les disponibilités des médecins.

Domaine 4 : Gestion des rendez-vous

Fonctionnalités :

réserver un rendez-vous
annuler un rendez-vous
reporter un rendez-vous
consulter l’historique des rendez-vous

Rôle :
Gérer les interactions entre patients et médecins.

Domaine 5 : Documents médicaux

Fonctionnalités :

déposer un document médical
consulter un document médical
déposer une ordonnance
déposer un compte rendu

Rôle :
Centraliser les informations médicales du patient.

Domaine 6 : Notifications

Fonctionnalités :

recevoir une confirmation de rendez-vous
recevoir un rappel automatique

Rôle :
Informer les utilisateurs et réduire les oublis.

Domaine 7 : Avis et administration

Fonctionnalités :

laisser un avis
modérer les avis
consulter les statistiques

Rôle :
Améliorer la qualité du service et superviser la plateforme.

# 6. Modules de conception : 

UserManagement
AuthenticationService (ajout important)
DoctorDirectory
ScheduleManagement (créneaux)
AppointmentManagement
MedicalDocumentManagement
NotificationService
AdministrationService

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

# 7. Schéma global de l’application

         Patient                       Médecin
            |                                |
            |                                |
            +----------- Utilisent ----------+
                            |
                            v
                  Interface Web / Mobile
                            |
                            v
                       API Backend
              _____________|______________
             |             |              |
             v             v              v
    Base de données    Notifications    Authentification
             |
             v
      Stockage documents


---

# 8 . MCD (Modèle Conceptuel de Données)

## Entités

* **UTILISATEUR** *(idUtilisateur, nom, prénom, email, motDePasse, rôle, téléphone)*
* **PATIENT** *(idPatient, numeroSecu, dateNaissance, adresse)*
* **MEDECIN** *(idMedecin, specialite, numeroRPPS, ville, adresseCabinet)*
* **CRENEAU** *(idCreneau, date, heureDebut, heureFin, disponibilite)*
* **RENDEZVOUS** *(idRendezVous, dateHeure, statut, motif)*
* **DOCUMENT_MEDICAL** *(idDocument, typeDocument, fichier, dateDepot)*
* **AVIS** *(idAvis, note, commentaire, dateAvis)*
* **NOTIFICATION** *(idNotification, type, contenu, dateEnvoi, statut)*

---

## Relations : 
• Un utilisateur peut être un patient.
• Un utilisateur peut être un médecin.
• Un médecin propose plusieurs créneaux.
• Un patient réserve plusieurs rendez-vous.
• Un médecin est concerné par plusieurs rendez-vous.
• Un rendez-vous utilise un créneau.
• Un patient possède plusieurs documents médicaux.
• Un médecin dépose plusieurs documents médicaux.
• Un patient laisse plusieurs avis.
• Un médecin reçoit plusieurs avis.
• Un rendez-vous déclenche plusieurs notifications.


---

# . MLD (Modèle Logique de Données)

## Tables relationnelles

### UTILISATEUR

* **id_utilisateur** (PK)
* nom
* prenom
* email (UNIQUE)
* mot_de_passe
* role
* telephone

---

### PATIENT

* **id_patient** (PK)
* id_utilisateur (FK → UTILISATEUR.id_utilisateur)
* numero_secu
* date_naissance
* adresse

---

### MEDECIN

* **id_medecin** (PK)
* id_utilisateur (FK → UTILISATEUR.id_utilisateur)
* specialite
* numero_rpps
* ville
* adresse_cabinet

---

### CRENEAU

* **id_creneau** (PK)
* id_medecin (FK → MEDECIN.id_medecin)
* date_creneau
* heure_debut
* heure_fin
* disponibilite

---

### RENDEZVOUS

* **id_rendezvous** (PK)
* id_patient (FK → PATIENT.id_patient)
* id_medecin (FK → MEDECIN.id_medecin)
* id_creneau (FK → CRENEAU.id_creneau)
* date_heure
* statut
* motif

---

### DOCUMENT_MEDICAL

* **id_document** (PK)
* id_patient (FK → PATIENT.id_patient)
* id_medecin (FK → MEDECIN.id_medecin)
* type_document
* fichier
* date_depot

---

### AVIS

* **id_avis** (PK)
* id_patient (FK → PATIENT.id_patient)
* id_medecin (FK → MEDECIN.id_medecin)
* note
* commentaire
* date_avis

---

### NOTIFICATION

* **id_notification** (PK)
* id_rendezvous (FK → RENDEZVOUS.id_rendezvous)
* type_notification
* contenu
* date_envoi
* statut

---


