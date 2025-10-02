# 📐 Règles Métier - Application Gestion RDV Garage

## 1. Règles de Planification 📅

### RG-PLAN-001: Durée des interventions
- **Description**: Définit les contraintes temporelles des interventions
- **Règles**:
  - Durée minimale: 30 minutes
  - Durée maximale: 8 heures (480 minutes)
  - Incrément: par tranche de 15 minutes
- **Exemple**: Une vidange = 30 min, une restauration complète moteur = 8h max

### RG-PLAN-002: Jours d'ouverture
- **Description**: Gestion des jours travaillés
- **Règles**:
  - Fermé le dimanche par défaut (paramétrable)
  - Ouverture samedi avec majoration 25%
  - Fermetures exceptionnelles à déclarer 1 mois avant
- **Exceptions**: Urgences dépannage 24/7 avec majoration 100%

### RG-PLAN-003: Capacité simultanée
- **Description**: Limite le nombre d'interventions parallèles
- **Règles**:
  - Maximum 3 véhicules par mécanicien
  - Maximum 1 véhicule par pont élévateur
  - Zone diagnostic: 2 véhicules max simultanés
- **Calcul**: Capacité = MIN(nb_ponts, nb_mécaniciens × 3)

### RG-PLAN-004: Buffer entre RDV
- **Description**: Temps tampon obligatoire
- **Règles**:
  - 15 minutes minimum entre 2 RDV même mécanicien
  - 30 minutes si changement de type intervention (mécanique → carrosserie)
  - Pas de buffer pour RDV urgents
- **Application**: Automatique lors de la réservation

### RG-PLAN-005: Gestion des urgences
- **Description**: Priorisation des interventions urgentes
- **Règles**:
  - 20% du planning réservé aux urgences
  - Priorité absolue si sécurité compromise
  - Majoration tarifaire +50€ fixe
  - Délai intervention < 4h
- **Exemple**: Panne sur autoroute, frein défaillant

## 2. Règles de Tarification 💰

### RG-TARIF-001: Taux horaire main d'œuvre
- **Description**: Différenciation des taux selon spécialité
- **Tarifs standard**:
  ```
  - Mécanique générale: 70€/h HT
  - Carrosserie/pein