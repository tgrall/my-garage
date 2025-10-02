# 📐 Règles Métier - My Garage

## 📋 Vue d'ensemble

Cette section contient toutes les règles métier qui régissent le fonctionnement de l'application My Garage. Ces règles définissent les contraintes, les validations et les comportements attendus du système.

## 📄 Documents

### [📋 BUSINESS-RULES.md](./BUSINESS-RULES.md)
Document principal contenant l'ensemble des règles métier organisées par domaine fonctionnel.

## 🏷️ Classification des Règles

### 🕐 Règles de Planification (RG-PLAN-xxx)
Règles liées à la gestion du temps et des créneaux de rendez-vous.

**Principales règles :**
- **RG-PLAN-001** : Durée des interventions (30 min à 8h par tranche de 15 min)
- **RG-PLAN-002** : Jours d'ouverture (fermé dimanche, majoration samedi)
- **RG-PLAN-003** : Capacité simultanée (3 véhicules/mécanicien max)
- **RG-PLAN-004** : Buffer entre RDV (temps tampon obligatoire)

### 👥 Règles Client (RG-CLIENT-xxx)
Règles concernant la gestion des comptes clients et de leurs données.

### 🚗 Règles Véhicule (RG-VEH-xxx)
Contraintes liées aux informations et à la gestion des véhicules.

### 💰 Règles Commerciales (RG-COM-xxx)
Règles de tarification, facturation et conditions commerciales.

### 🔧 Règles Techniques (RG-TECH-xxx)
Contraintes techniques et de performance du système.

## 🔗 Liens avec les Épics

Ces règles métier sont appliquées dans les différentes épics :

| Règle | Epic(s) Concernée(s) | Impact |
|-------|---------------------|--------|
| RG-PLAN-001 à 004 | [Epic 02](../epics/EPIC-02-prise-rdv.md), [Epic 03](../epics/EPIC-03-planning.md) | Gestion des créneaux et planning |
| RG-CLIENT-xxx | [Epic 01](../epics/EPIC-01-gestion-clients.md) | Validation des données client |
| RG-VEH-xxx | [Epic 01](../epics/EPIC-01-gestion-clients.md) | Gestion du parc automobile |
| RG-COM-xxx | [Epic 04](../epics/EPIC-04-interventions.md) | Facturation et devis |
| RG-TECH-xxx | Toutes les épics | Performance et fiabilité |

## 📊 Impact sur les User Stories

Les règles métier impactent directement les user stories :

### 📅 Planning & RDV
- **US-04** (Prise de RDV) : Application de RG-PLAN-001, 002, 003
- **US-07** (Visualisation planning) : Respect de RG-PLAN-003, 004
- **US-08** (Gestion disponibilités) : Application de RG-PLAN-002
- **US-09** (Affectation intelligente) : Optimisation selon RG-PLAN-003

### 👤 Gestion Client
- **US-01** (Création compte) : Validation selon RG-CLIENT-xxx
- **US-02** (Gestion véhicules) : Contraintes RG-VEH-xxx

### 🔧 Interventions
- **US-11** (Gestion devis) : Application de RG-COM-xxx
- **US-12** (Facturation) : Respect des règles commerciales

## 🔄 Mise à jour des Règles

Les règles métier évoluent avec le projet. Chaque modification doit :

1. **Être documentée** dans BUSINESS-RULES.md
2. **Être versionée** avec impact sur les épics
3. **Être validée** par les parties prenantes
4. **Être tracée** dans les user stories concernées

## 🔗 Navigation

- **[📚 Documentation principale](../index.md)**
- **[🎯 Épics](../epics/index.md)**  
- **[🏠 Accueil du projet](../../index.md)**

---
*Dernière mise à jour : Octobre 2025*