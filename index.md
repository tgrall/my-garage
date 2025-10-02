# 🚗 My Garage - Documentation Index

## 📋 Vue d'ensemble

Bienvenue dans la documentation complète de l'application **My Garage** - une solution de gestion de rendez-vous pour garage automobile.

## 🗂️ Navigation Principale

### 📚 Documentation Technique
- **[README Principal](./README.md)** - Description générale du projet, objectifs et roadmap
- **[Documentation Détaillée](./docs/index.md)** - Accès à toute la documentation technique

### 🎯 Épics & Fonctionnalités
- **[EPIC 01 - Gestion des Clients](./docs/epics/EPIC-01-gestion-clients.md)** - Comptes clients et véhicules
- **[EPIC 02 - Prise de RDV](./docs/epics/EPIC-02-prise-rdv.md)** - Système de réservation
- **[EPIC 03 - Planning](./docs/epics/EPIC-03-planning.md)** - Gestion des ressources et planification
- **[EPIC 04 - Interventions](./docs/epics/EPIC-04-interventions.md)** - Cycle de vie des interventions

### 📐 Règles Métier
- **[Règles Métier](./docs/business-rules/BUSINESS-RULES.md)** - Contraintes et règles de gestion

### 📅 Planning & Stratégie
- **[📅 Planning Stratégique](./docs/PLANNING-STRATEGIQUE.md)** - Roadmap 11 sprints et milestones
- **[🏗️ Guide d'Organisation](./docs/GUIDE-ORGANISATION.md)** - Méthodologie et séquencement
- **[📋 Issues GitHub](https://github.com/tgrall/my-garage/issues)** - Épics et User Stories

## 🔍 User Stories par Epic

### 👤 Gestion des Clients (EPIC 01)
- **US-01** - Création de compte client
- **US-02** - Gestion des véhicules
- **US-03** - Consultation historique

### 📅 Prise de RDV (EPIC 02)
- **US-04** - Prise de RDV en ligne
- **US-05** - Modification/Annulation de RDV
- **US-06** - Validation RDV par le garage

### 🗓️ Planning (EPIC 03)
- **US-07** - Visualisation planning mécanicien
- **US-08** - Gestion des disponibilités garage
- **US-09** - Affectation intelligente des RDV

### 🔧 Interventions (EPIC 04)
- **US-10** - Documentation de l'intervention
- **US-11** - Création et gestion des devis
- **US-12** - Facturation et paiement

## 🚀 Comment naviguer

1. **Pour une vue d'ensemble** : Commencez par le [README principal](./README.md)
2. **Pour les détails techniques** : Explorez le dossier [docs/](./docs/index.md)
3. **Pour une fonctionnalité spécifique** : Accédez directement à l'epic correspondant
4. **Pour les contraintes** : Consultez les [règles métier](./docs/business-rules/BUSINESS-RULES.md)

## 📊 État d'avancement

```mermaid
pie title Répartition des User Stories par Phase
    "Phase 1 - MVP (9 US)" : 75
    "Phase 2 - Optimisation (3 US)" : 25
```

```mermaid
graph LR
    subgraph "✅ Phase 1 - MVP (Sprints 1-6)"
        EP1[Epic 01<br/>Gestion Clients<br/>US-01 à US-03]
        EP2[Epic 02<br/>Prise de RDV<br/>US-04 à US-06]
        EP3[Epic 03<br/>Planning<br/>US-07 à US-09]
    end
    
    subgraph "🔄 Phase 2 - Optimisation (Sprints 7-11)"
        EP4[Epic 04<br/>Interventions<br/>US-10 à US-12]
    end
    
    subgraph "📅 Phase 3 - Extensions Futures"
        COMM[Communication<br/>Notifications avancées]
        REPORT[Reporting<br/>Analytics & BI]
        MOBILE[Mobile App<br/>Application native]
    end
    
    EP1 --> EP2
    EP2 --> EP3
    EP3 --> EP4
    EP4 -.-> COMM
    EP4 -.-> REPORT
    EP4 -.-> MOBILE
    
    classDef mvp fill:#e8f5e8,stroke:#2e7d32,stroke-width:2px
    classDef current fill:#fff3e0,stroke:#ef6c00,stroke-width:2px
    classDef future fill:#e3f2fd,stroke:#1565c0,stroke-width:1px,stroke-dasharray: 5 5
    
    class EP1,EP2,EP3 mvp
    class EP4 current
    class COMM,REPORT,MOBILE future
```

- ✅ **Phase 1 (MVP)** : Epics 01, 02, 03 - Fonctionnalités de base
- 🔄 **Phase 2** : Epic 04 - Gestion complète des interventions
- 📅 **Phase 3** : Extensions futures (communication, reporting)

---
*Dernière mise à jour : Octobre 2025*