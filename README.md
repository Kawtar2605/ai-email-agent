# Agent IA de gestion d’emails

Ce projet présente un workflow d’automatisation permettant d’assister la gestion d’emails professionnels grâce à l’intelligence artificielle.

L’objectif est d’analyser automatiquement les emails entrants, détecter leur intention et proposer une réponse générée par IA.

Le système peut ensuite créer automatiquement un brouillon de réponse dans Outlook et notifier l’utilisateur.

---

## Fonctionnalités

- Analyse automatique des emails entrants
- Détection de l’intention du message
- Identification de la priorité
- Génération automatique d’une réponse par IA
- Création d’un brouillon dans Outlook
- Notification utilisateur via Telegram

---

## Architecture du workflow

Le système repose sur un workflow automatisé avec n8n.

Flux de fonctionnement :

Email reçu (Outlook Trigger)  
↓  
Analyse du contenu par un modèle OpenAI  
↓  
Extraction des informations clés (intention, priorité, besoin de réponse)  
↓  
Logique de décision (Switch)  
↓  
Création d’un brouillon de réponse dans Outlook  
↓  
Notification de l’utilisateur via Telegram  

---

## Exemple de sortie générée par l’IA

```json
{
 "intent": "job offer acceptance",
 "needs_reply": "yes",
 "priority": "high",
 "suggested_reply": "Thank you for the job offer. I am excited to discuss the details further."
}
