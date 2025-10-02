# 📐 Règles Métier - Application Gestion RDV Garage

## 🔗 Navigation Rapide
- **[📋 Index Général](../../index.md)** | **[📚 Documentation](../index.md)** | **[📐 Règles Métier](./index.md)**
- **Épics :** [Epic 01 - Clients](../epics/EPIC-01-gestion-clients.md) | [Epic 02 - RDV](../epics/EPIC-02-prise-rdv.md) | [Epic 03 - Planning](../epics/EPIC-03-planning.md) | [Epic 04 - Interventions](../epics/EPIC-04-interventions.md)

## 📋 Règles par catégorie
- **[1. Règles de Planification](#1-règles-de-planification-)** - Contraintes temporelles et capacitaires
- **[2. Plus de règles](#2-règles-de-planification-)** - À venir selon évolution du document

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
  - Carrosserie/peinture: 80€/h HT
  - Électronique auto: 90€/h HT
  - Diagnostic spécialisé: 100€/h HT
  ```

---

## 🔗 Navigation

### 📐 Règles par Epic
- **[Epic 01 - Gestion Clients](../epics/EPIC-01-gestion-clients.md)** - RG-CLIENT-xxx
- **[Epic 02 - Prise de RDV](../epics/EPIC-02-prise-rdv.md)** - RG-RDV-xxx  
- **[Epic 03 - Planning](../epics/EPIC-03-planning.md)** - RG-PLAN-xxx
- **[Epic 04 - Interventions](../epics/EPIC-04-interventions.md)** - RG-INT-xxx

### 📚 Documentation
- **[📐 Index Règles Métier](./index.md)** - Vue d'ensemble des règles
- **[🎯 Index des Épics](../epics/index.md)** - Vue d'ensemble des épics
- **[📚 Documentation](../index.md)** - Accès à toute la documentation
- **[🏠 Accueil](../../index.md)** - Vue d'ensemble du projet

*Dernière mise à jour : Octobre 2025*