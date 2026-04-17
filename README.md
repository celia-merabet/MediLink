# MediLink
#### Sujet proposé : MediLink
#### Application de prise de rendez-vous et de suivi médical

#### Type :  Application web et mobile de gestion de rendez-vous médicaux et de suivi patient.

# Idée  

MediLink permet aux patients de :
- Rechercher un professionnel de santé,
- Prendre rendez-vous en ligne,
- Recevoir des rappels,
- Consulter leur historique de rendez-vous,
- Déposer des documents médicaux.
Elle permet aussi aux médecins de :
- Gérer leur agenda,
- Consulter les demandes de rendez-vous,
- Suivre les patients,
- Partager des ordonnances ou comptes rendus.

# Décrire l’application

L’objectif de *MediLink* est de simplifier l’accès aux soins en centralisant la prise de rendez-vous, le suivi administratif et certains échanges entre patients et professionnels de santé.

Cette application répond à plusieurs problèmes :

- Difficulté à obtenir rapidement un rendez-vous,
- Appels téléphoniques trop longs pour réserver,
- Oublis de rendez-vous,
- Mauvaise organisation des dossiers et documents,
- Manque de visibilité sur les disponibilités des médecins,
- Surcharge administrative pour les secrétariats médicaux.

L’application est utile car elle :

- Fait gagner du temps aux patients,
- Réduit les appels téléphoniques,
- Améliore l’organisation des cabinets,
- Limite les rendez-vous oubliés grâce aux rappels,
- Facilite le suivi des documents médicaux.
 
# Fonctionnalités principales

**Côté patient :**

- Créer un compte,
- Se connecter,
- Modifier son profil,
- Rechercher un médecin par spécialité, ville ou nom,
- Consulter les créneaux disponibles,
- Prendre rendez-vous,
- Annuler ou déplacer un rendez-vous,
- Recevoir des rappels par notification ou email,
- Consulter l’historique des rendez-vous,
- Déposer des documents médicaux,
- Consulter des ordonnances ou comptes rendus,
- Laisser un avis sur le praticien.

**Côté médecin :**

- créer un compte professionnel,
- renseigner sa spécialité,
- définir ses horaires de consultation,
- ouvrir ou fermer des créneaux,
- consulter son agenda,
- accepter ou refuser certaines demandes,
- consulter le dossier administratif du patient,
- déposer une ordonnance,
- déposer un compte rendu,
- suivre l’historique des rendez-vous.

**Côté administrateur :**

- gérer les comptes utilisateurs,
- vérifier les comptes médecins,
- modérer les avis,
- superviser la plateforme,
- gérer les catégories de spécialités médicales,
- consulter des statistiques globales.
 
# Étape 1 : Liste brute des fonctionnalités
- créer un compte patient
- créer un compte médecin
- se connecter
- se déconnecter
- réinitialiser le mot de passe
- modifier son profil
- rechercher un médecin
- filtrer par spécialité
- filtrer par ville
- consulter les créneaux disponibles
- réserver un rendez-vous
- annuler un rendez-vous
- reporter un rendez-vous
- recevoir un rappel
- consulter l’historique des rendez-vous
- déposer un document médical
- consulter un document médical
- déposer une ordonnance
- déposer un compte rendu
- laisser un avis
- modérer les avis
- gérer les horaires du médecin
- ouvrir ou fermer des créneaux
- gérer les comptes
- valider les comptes médecins
- consulter les statistiques de la plateforme
 
# Étape 2 : Tri des fonctionnalités par domaines métiers

## Domaine 1 : Gestion des utilisateurs

**Fonctionnalités :**
- créer un compte patient
- créer un compte médecin
- se connecter
- se déconnecter
- réinitialiser le mot de passe
- modifier son profil
- gérer les comptes
- valider les comptes médecins

**Rôle :**
Ce domaine gère l’identité, les droits et les profils.
 
## Domaine 2 : Annuaire médical

**Fonctionnalités :**
- rechercher un médecin
- filtrer par spécialité
- filtrer par ville

**Rôle :**
Permet de trouver un praticien adapté.
 
## Domaine 3 : Gestion des rendez-vous

**Fonctionnalités :**
- consulter les créneaux disponibles
- réserver un rendez-vous
- annuler un rendez-vous
- reporter un rendez-vous
- consulter l’historique des rendez-vous
- gérer les horaires du médecin
- ouvrir ou fermer des créneaux

**Rôle :**
C’est le cœur fonctionnel de l’application.
 
## Domaine 4 : Documents médicaux

**Fonctionnalités :**
- déposer un document médical
- consulter un document médical
- déposer une ordonnance
- déposer un compte rendu

**Rôle :**
Centraliser les documents liés au suivi du patient.
 
## Domaine 5 : Notifications

**Fonctionnalités :**
- recevoir un rappel

**Rôle :**
Prévenir les utilisateurs pour éviter les oublis.
 
##  Domaine 6 : Administration et qualité

**Fonctionnalités :**
- laisser un avis
- modérer les avis
- consulter les statistiques de la plateforme

**Rôle :**
Améliorer la qualité du service et superviser la plateforme.

# 6. Modules de conception

À partir des domaines métiers, on déduit les modules suivants :
- UserManagement
- DoctorDirectory
- AppointmentManagement
- MedicalDocumentManagement
- NotificationManagement
- Administration

# Étape 3 — Entités métier principales
**Utilisateur**

- id
- nom
- prénom
- email
- motDePasse
- rôle
- téléphone

**Patient**

- idPatient
- numéroSécuritéSociale
- dateNaissance
- adresse

**Médecin**

- idMedecin
- spécialité
- numéroRPPS
- ville
- adresseCabinet

**Créneau**

- idCréneau
- date
- heureDébut
- heureFin
- disponibilité

**RendezVous**

- idRendezVous
- dateHeure
- statut
- motif
- patient
- médecin
- créneau

**DocumentMedical**

- idDocument
- typeDocument
- fichier
- dateDepot
- patient
- médecin

**Avis**

- idAvis
- note
- commentaire
- date
- patient
- médecin

**Notification**

- idNotification
- type
- contenu
- dateEnvoi
- statut

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
* Un utilisateur peut être un patient.
* Un utilisateur peut être un médecin.
* Un médecin propose plusieurs créneaux.
* Un patient réserve plusieurs rendez-vous.
* Un médecin est concerné par plusieurs rendez-vous.
* Un rendez-vous utilise un créneau.
* Un patient possède plusieurs documents médicaux.
* Un médecin dépose plusieurs documents médicaux.
* Un patient laisse plusieurs avis.
* Un médecin reçoit plusieurs avis.
* Un rendez-vous déclenche plusieurs notifications.

---

# . MLD (Modèle Logique de Données)

## Tables relationnelles

**UTILISATEUR :** <br>
(id_utilisateur PK, nom, prenom, email UNIQUE, mot_de_passe, role, telephone)

**PATIENT :** <br>
(id_patient PK, *id_utilisateur FK → UTILISATEUR.id_utilisateur*, numero_secu, date_naissance, adresse)

**MEDECIN :** <br>
(id_medecin PK, *id_utilisateur FK → UTILISATEUR.id_utilisateur*, specialite, numero_rpps, ville, adresse_cabinet)

**CRENEAU :** <br>
(id_creneau PK, *id_medecin FK → MEDECIN.id_medecin*, date_creneau, heure_debut, heure_fin, disponibilite)

**RENDEZVOUS :** <br>
(id_rendezvous PK, *id_patient FK → PATIENT.id_patient*, *id_medecin FK → MEDECIN.id_medecin*, *id_creneau FK → CRENEAU.id_creneau*, date_heure, statut, motif)

**DOCUMENT_MEDICAL :** <br>
(id_document PK, *id_patient FK → PATIENT.id_patient*, *id_medecin FK → MEDECIN.id_medecin*, type_document, fichier, date_depot)

**AVIS :** <br>
(id_avis PK, *id_patient FK → PATIENT.id_patient*, *id_medecin FK → MEDECIN.id_medecin*, note, commentaire, date_avis)

**NOTIFICATION :** <br>
(id_notification PK, *id_rendezvous FK → RENDEZVOUS.id_rendezvous*, type_notification, contenu, date_envoi, statut)

---


