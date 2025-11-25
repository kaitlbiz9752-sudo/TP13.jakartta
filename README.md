# Projet Spring Boot + Bash (ens-springbash)

Ce projet illustre l’automatisation du cycle de vie d'une application **Spring Boot** à l’aide de **scripts Bash**.  
Il s’inscrit dans le cadre d’un TP visant la maîtrise du déploiement, supervision, arrêt, health-check et archivage des logs.

---

##  Structure du projet

```
ens-springbash/
├─ src/
│  ├─ main/java/ma/ens/springbash/
│  └─ main/resources/
├─ scripts/
│  ├─ run.sh
│  ├─ stop.sh
│  ├─ logs.sh
│  ├─ deploy.sh
│  └─ healthcheck.sh
├─ logs/
├─ pom.xml
└─ README.md
```

---

##  Démarrage de l'application

```
./scripts/run.sh
```

Ce script :
- Démarre l’application en arrière‑plan via `nohup mvn spring-boot:run &`
- Enregistre les logs dans `logs/app.log`
- Affiche le PID du processus lancé

---

##  Arrêt de l'application

```
./scripts/stop.sh
```

Ce script :
- Recherche le processus Spring Boot actif via `ps aux | grep`
- Tue le processus grâce à `kill -9`

---

##  Consultation des logs

```
./scripts/logs.sh
```

Affiche les **30 dernières lignes** des logs.

---

##  Health Check

Avant d'utiliser ce script, assurez-vous que **Spring Boot Actuator** est activé.

Test :

```
./scripts/healthcheck.sh
```

---

![WhatsApp Image 2025-11-25 at 17 51 59](https://github.com/user-attachments/assets/200a3da5-7bc0-48a2-93b4-71ecd3dc4dd1)




---




---

## 📝 Technologies utilisées

- **Java 17**
- **Spring Boot 3.2.x**
- **Maven**
- **H2 Database**
- **Bash**
- **Actuator (health endpoint)**

---

## 👤 Auteur

TP réalisé par : **Kaoutar Aitlbiz**  
Encadré par : **ENS**  

---

## ✔️ Objectif pédagogique

Ce TP permet de maîtriser :

- L'automatisation DevOps
- Le cycle de vie d’une application Spring Boot
- La gestion des processus Linux
- La supervision via logs et health-check
- Le déploiement continu

Bonne continuation ! 



