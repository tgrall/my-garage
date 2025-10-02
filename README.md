# 🚗 My Garage - Application de Gestion de RDV pour Garage Automobile

## 📋 Description

Application web permettant la gestion complète des rendez-vous et interventions d'un garage automobile. Cette solution digitale facilite la prise de RDV en ligne, la gestion du planning des mécaniciens et le suivi des interventions.

## 🎯 Objectifs

- **Digitaliser** la prise de rendez-vous
- **Optimiser** le planning des mécaniciens
- **Améliorer** l'expérience client
- **Tracer** les interventions et l'historique
- **Automatiser** les processus administratifs

## 📚 Documentation

### 🔗 Navigation Rapide
- **[📋 Index Général](./index.md)** - Vue d'ensemble et navigation complète
- **[📚 Documentation Complète](./docs/index.md)** - Accès à toute la documentation technique

### 🎯 Épics & Fonctionnalités
| Epic | Description | User Stories | Statut |
|------|-------------|-------------|--------|
| **[Epic 01 - Gestion Clients](./docs/epics/EPIC-01-gestion-clients.md)** | Comptes clients et véhicules | US-01, US-02, US-03 | ✅ Spécifiée |
| **[Epic 02 - Prise de RDV](./docs/epics/EPIC-02-prise-rdv.md)** | Système de réservation | US-04, US-05, US-06 | ✅ Spécifiée |
| **[Epic 03 - Planning](./docs/epics/EPIC-03-planning.md)** | Gestion des ressources | US-07, US-08, US-09 | ✅ Spécifiée |
| **[Epic 04 - Interventions](./docs/epics/EPIC-04-interventions.md)** | Cycle des interventions | US-10, US-11, US-12 | ✅ Spécifiée |

### 📐 Règles & Contraintes
- **[Règles Métier](./docs/business-rules/BUSINESS-RULES.md)** - Contraintes fonctionnelles et de gestion

### 📅 Planning & Organisation
- **[Planning Stratégique](./docs/PLANNING-STRATEGIQUE.md)** - Roadmap détaillé et milestones
- **[Guide d'Organisation](./docs/GUIDE-ORGANISATION.md)** - Méthodologie et séquencement optimal
- **[Issues GitHub](https://github.com/tgrall/my-garage/issues)** - Épics et User Stories trackées

### Structure de la Documentation

```
docs/
├── index.md                  # Navigation documentation
├── epics/                    # Épics détaillées
│   ├── index.md             # Index des épics
│   ├── EPIC-01-gestion-clients.md
│   ├── EPIC-02-prise-rdv.md
│   ├── EPIC-03-planning.md
│   └── EPIC-04-interventions.md
└── business-rules/           # Règles métier
    ├── index.md             # Index des règles
    └── BUSINESS-RULES.md
```

## 🚀 Roadmap & Architecture

### 📊 Vue d'ensemble du Projet

```mermaid
graph TB
    subgraph "👥 Acteurs"
        CLIENT[👤 Client<br/>Réservation RDV<br/>Suivi véhicules]
        GARAGE[🏢 Responsable Garage<br/>Validation RDV<br/>Gestion planning]
        MECHANIC[🔧 Mécanicien<br/>Planning personnel<br/>Documentation]
    end
    
    subgraph "🎯 Fonctionnalités Core"
        AUTH[🔐 Authentification<br/>Comptes & Sécurité]
        BOOKING[📅 Système RDV<br/>Réservation & Gestion]
        PLANNING[🗓️ Planning Intelligent<br/>Optimisation Ressources]
        INTERVENTION[🔧 Interventions<br/>Documentation & Facturation]
    end
    
    subgraph "⚙️ Architecture Technique"
        FRONTEND[🌐 Frontend Web<br/>React + TypeScript]
        API[🔌 API REST<br/>Node.js + Express]
        DATABASE[💾 Base de Données<br/>PostgreSQL]
        CLOUD[☁️ Cloud Services<br/>AWS/Azure + CI/CD]
    end
    
    CLIENT --> AUTH
    CLIENT --> BOOKING
    GARAGE --> BOOKING
    GARAGE --> PLANNING
    MECHANIC --> PLANNING
    MECHANIC --> INTERVENTION
    
    AUTH --> FRONTEND
    BOOKING --> FRONTEND
    PLANNING --> FRONTEND
    INTERVENTION --> FRONTEND
    
    FRONTEND --> API
    API --> DATABASE
    API --> CLOUD
    
    classDef user fill:#ffebee,stroke:#c62828,stroke-width:2px
    classDef feature fill:#e8f5e8,stroke:#2e7d32,stroke-width:2px
    classDef tech fill:#e3f2fd,stroke:#1565c0,stroke-width:2px
    
    class CLIENT,GARAGE,MECHANIC user
    class AUTH,BOOKING,PLANNING,INTERVENTION feature
    class FRONTEND,API,DATABASE,CLOUD tech
```

### 📅 Planning Stratégique

```mermaid
timeline
    title Roadmap My Garage - 11 Sprints (5.5 mois)
    
    section Phase 1 - MVP
        Sprint 1-2 : Fondations Client
                   : Comptes & Véhicules
                   : Historique de base
        
        Sprint 3 : 🎯 Milestone 1
                 : Réservation Client
                 : Premier value delivery
        
        Sprint 4-6 : Complétion MVP
                   : Gestion RDV complète
                   : Interface garage
                   : 🚀 MVP Release
    
    section Phase 2 - Optimisation
        Sprint 7-8 : Intelligence & Mobile
                   : Affectation automatique
                   : Interface mécaniciens
        
        Sprint 9-11 : Cycle Commercial
                    : Documentation complète
                    : Devis & Facturation
                    : 🎯 Lancement Général
```

### Phase 1 - MVP (3 mois)
- ✅ Gestion des comptes clients
- ✅ Prise de RDV basique
- ✅ Planning simple

### Phase 2 - Enrichissement (2 mois)
- 🔄 Gestion complète des interventions
- 🔄 Facturation
- 🔄 Affectation intelligente

### Phase 3 - Optimisation (2 mois)
- 📊 Analytics et reporting
- 💬 Communication automatisée
- 🤖 IA pour suggestions

## 🛠 Stack Technique Suggérée

- **Frontend**: React/Vue.js + TypeScript
- **Backend**: Node.js/Spring Boot
- **Database**: PostgreSQL
- **Cache**: Redis
- **Messaging**: RabbitMQ
- **Storage**: S3/MinIO

## 📈 KPIs Principaux

- Taux de RDV en ligne vs téléphone
- Temps moyen de prise de RDV
- Taux d'occupation des mécaniciens
- NPS (Net Promoter Score)
- Délai moyen d'intervention

## 🤝 Contributeurs

- Product Owner: [À définir]
- Scrum Master: [À définir]
- Dev Team: [À définir]

## 📄 License

Propriétaire - Tous droits réservés

---

## 🔗 Navigation

- **[📋 Index Général](./index.md)** - Vue d'ensemble complète du projet
- **[📚 Documentation](./docs/index.md)** - Accès à toute la documentation
- **[🎯 Épics](./docs/epics/index.md)** - Liste des fonctionnalités détaillées
- **[📐 Règles Métier](./docs/business-rules/index.md)** - Contraintes et règles de gestion

*Dernière mise à jour : Octobre 2025*