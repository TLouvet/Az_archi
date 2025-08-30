# Azure Service Health

## 🌍 Description

Azure Service Health fournit des informations personnalisées sur l’état des services Azure, les incidents en cours et les maintenances planifiées qui affectent directement les ressources d’un abonnement.

https://learn.microsoft.com/fr-fr/azure/service-health/

---

## 🎯 Usage principal

- Alerter rapidement en cas de panne ou dégradation d’un service Azure utilisé (ex. App Service, VM, SQL Database).
- Suivre les maintenances planifiées susceptibles d’impacter la plateforme.
- Accéder à un historique des incidents pour réaliser des analyses post-mortem.

---

## 📌 Cas d’utilisation

- Mise en place d’alertes pour une équipe IT/OPS supervisant une infrastructure Azure.
- Configuration de notifications sur des applications critiques (mail, Teams, webhook).
- Suivi centralisé de l’état des services dans le cadre de la gouvernance cloud.

---

## ⚠️ Limites

- Ne remplace pas la supervision interne (Azure Monitor, Log Analytics) : Service Health se concentre uniquement sur la santé des services Azure eux-mêmes.
- Notifications avec un léger délai possible par rapport à l’incident réel.
- Pas de métriques techniques détaillées (uniquement incidents/maintenances globales).

---

## ✅ Bonnes pratiques

- [ ] Configurer des alertes Service Health via **Action Groups** (mail, SMS, Teams, webhook).
- [ ] Intégrer Service Health aux outils d’ITSM ou de monitoring existants.
- [ ] Vérifier régulièrement les maintenances planifiées pour anticiper les impacts.
- [ ] Définir les destinataires des notifications en fonction des rôles :
  - Équipe **Ops/Infra** : incidents sur VM, réseaux, bases de données.
  - Équipe **Développement/DevOps** : incidents sur App Service, fonctions serverless, pipelines CI/CD.
  - **Responsable applicatif** ou **Product Owner** : impact potentiel sur les utilisateurs finaux.
  - **Service support/N1** : pour préparer les communications aux utilisateurs.
  - **RSSI / Sécurité** : en cas d’incident lié à la conformité ou à la disponibilité.
