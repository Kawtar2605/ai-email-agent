# AI Email Agent – Workflow d’automatisation intelligent

Ce projet consiste en la conception et le déploiement d’un agent IA capable d’automatiser la gestion des emails professionnels, en s’appuyant sur une architecture workflow no-code avec n8n et des modèles LLM.

L’objectif est de réduire les tâches répétitives liées aux emails (lecture, compréhension, réponse), tout en proposant des réponses contextualisées et exploitables.

---

## Objectif du projet

Automatiser la gestion des emails professionnels grâce à un agent IA capable de comprendre, répondre et proposer des actions automatiquement.

---

## Demo

Une démonstration vidéo du workflow est disponible ici :  
[Accéder à la vidéo de démonstration] ( https://drive.google.com/file/d/1Sy7yiSJgjtvvzECqEOB4VA2wF3c0uJpk/view?usp=sharing )

---

## Fonctionnement global

Le système intercepte les emails entrants et exécute automatiquement les étapes suivantes :

- Analyse du contenu du mail via un modèle LLM  
- Détection de l’intention (prise de rendez-vous, demande d’information, etc.)  
- Génération d’une réponse contextualisée et professionnelle  
- Proposition automatique de créneaux de rendez-vous basée sur une logique définie  
- Création d’un brouillon de réponse dans Outlook  
- Notification de l’utilisateur via Telegram  

> Une intégration dynamique avec le calendrier est actuellement en cours de développement afin de proposer des créneaux en temps réel basés sur les disponibilités réelles.

---

## Architecture technique

Le workflow a été entièrement conçu avec n8n et repose sur les composants suivants :

### 1. Microsoft Outlook Trigger  
Détection des emails entrants en temps réel  

### 2. Node IA (LLM)  
Analyse du contenu du mail et génération d’une réponse adaptée  

### 3. Node JavaScript (traitement des données)  
- Développement d’une logique de proposition de créneaux  
- Formatage des disponibilités  
- Structuration des réponses  

### 4. Second Node IA  
Injection des créneaux dans la réponse pour produire un message naturel et cohérent  

### 5. Microsoft Outlook – Create Draft  
Création automatique d’un brouillon prêt à être envoyé  

### 6. Telegram Node  
Notification utilisateur en temps réel  

### 7. (En cours) Microsoft Outlook Calendar Integration  
Connexion au calendrier pour récupérer les disponibilités réelles et générer des créneaux dynamiques sans conflit  

---

## Exemple concret

Email reçu :

> Bonjour, je souhaiterais organiser un rendez-vous cette semaine.

Réponse générée automatiquement :

> Bonjour,  
> Merci pour votre message. Voici quelques créneaux disponibles :  
> - Mardi à 10h  
> - Jeudi à 14h  
> - Vendredi à 11h  
>  
> N’hésitez pas à me dire ce qui vous convient.

---

## Valeur ajoutée

- Automatisation des tâches à faible valeur ajoutée  
- Réduction du temps de traitement des emails  
- Standardisation des réponses professionnelles  
- Intégration directe avec outils métiers (Outlook, Telegram)  
- Approche scalable et adaptable à d’autres cas d’usage  

---

## Stack technique

- n8n (workflow automation)  
- OpenAI / LLM  
- Microsoft Outlook API  
- JavaScript (data processing)  
- Telegram API  

---

## Perspectives d’amélioration

- Intégration complète du calendrier pour gestion dynamique des disponibilités  
- Détection automatique des conflits de planning  
- Gestion des fuseaux horaires  
- Personnalisation avancée du ton  
- Priorisation automatique plus fine  
- Ajout d’un système de validation humaine  
