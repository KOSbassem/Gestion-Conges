# 🗓️ Leave Management System (Gestion des Congés)

Application complète de gestion des congés et des autorisations de sortie,
développée avec **Spring Boot** (Backend) et **Vue.js** (Frontend).

Le système gère :
- les demandes de congé
- les autorisations de sortie (en heures)
- un workflow de validation multi-niveaux
- la gestion automatique des soldes (réservé / réel)

---

## 🧩 Architecture du projet

Ce repository contient **deux branches principales** :

| Branche   | Description |
|----------|-------------|
| backend  | API REST Spring Boot |
| frontend | Application Vue.js |

---

## ⚙️ Backend — Spring Boot

### Technologies
- Java 17
- Spring Boot
- Spring Security + JWT
- JPA / Hibernate
- MySQL
- Maven

### Fonctionnalités clés
- Authentification JWT
- Gestion des rôles (Admin, Directeur, Chef d’équipe, Employé)
- Demandes de congé (jours)
- Autorisations de sortie (heures → équivalent jours)
- Solde **réservé** vs **solde réel**
- Tâches planifiées (`@Scheduled`) :
  - application automatique du solde
  - passage des demandes à l’état *traitée*

### Lancer le backend
```bash
git checkout backend
mvn clean install
java -jar target/*.jar
