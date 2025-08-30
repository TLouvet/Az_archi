# 🛡️ Checklist Défense en Profondeur (Azure & Cloud)

## 1. Identité & Accès

- [ ] Activer **MFA** pour tous les comptes
- [ ] Pas de comptes admins permanents (utiliser **PIM**)
- [ ] Appliquer le **Principe du Moindre Privilège** (RBAC fin)
- [ ] Isoler les comptes **utilisateurs** et **services** (Managed Identities)
- [ ] Vérifier régulièrement les **logs Azure AD** (sign-ins suspects)

---

## 2. Périmètre Réseau

- [ ] Isoler les ressources dans des **VNets**
- [ ] Segmenter avec des **Subnets** (Front, Back, DB)
- [ ] Appliquer des **NSG** (Network Security Groups) pour contrôler le trafic
- [ ] Utiliser un **Azure Firewall / WAF** pour filtrer les accès externes
- [ ] Mettre en place des **Private Endpoints** pour éviter les expos publics
- [ ] Restreindre par **IP Whitelisting** quand c’est possible

---

## 3. Sécurité des Workloads (Compute)

- [ ] Appliquer les **mises à jour automatiques** (VM, containers, App Services)
- [ ] Limiter les ports ouverts (SSH/RDP via Bastion ou JIT Access)
- [ ] Activer **Defender for Cloud** pour détection avancée
- [ ] Scanner les images Docker (ACR tasks, Defender)
- [ ] Chiffrer les disques (Azure Disk Encryption)

---

## 4. Données

- [ ] Activer le **chiffrement au repos** (Storage/SQL/Disks par défaut)
- [ ] Utiliser **TLS/HTTPS** pour le chiffrement en transit
- [ ] Protéger les secrets via **Key Vault**
- [ ] Utiliser des **Managed Identities** pour l’accès aux ressources
- [ ] Configurer des **backups réguliers** et tester la restauration

---

## 5. Supervision & Logs

- [ ] Centraliser les logs dans **Log Analytics**
- [ ] Configurer **Azure Monitor + Alerts**
- [ ] Activer les **NSG Flow Logs** si besoin d’auditer le réseau
- [ ] Connecter à **Microsoft Sentinel** (SIEM/SOC)
- [ ] Faire des **revues régulières** des journaux d’accès

---

## 6. Applications & DevSecOps

- [ ] Activer les **scans de dépendances** (Dependabot, GitHub Advanced Security)
- [ ] Mettre des **tests de sécurité automatiques** dans la CI/CD
- [ ] Utiliser **API Management** pour sécuriser et monitorer les API
- [ ] Réduire la **surface d’attaque** (désactiver endpoints inutiles)
- [ ] Appliquer **rate limiting / throttling** sur les API exposées

---

## 7. Gouvernance & Bonnes Pratiques

- [ ] Définir une **Azure Policy** (pas de VM publiques, HTTPS obligatoire, etc.)
- [ ] Utiliser **blueprints** ou IaC (Terraform/Bicep/ARM)
- [ ] Vérifier la **conformité réglementaire** (RGPD, ISO, PCI, etc.)
- [ ] Former les équipes (phishing, sécurité opérationnelle)
- [ ] Organiser des **tests d’intrusion / Red Team** réguliers

---
