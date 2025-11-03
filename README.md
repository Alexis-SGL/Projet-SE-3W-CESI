<img src="https://github.com/user-attachments/assets/14f92d9c-cd22-4b7d-b6be-ed5ceb1216b8" alt="Logo 3W" width="100" align="right" />
<br><br>


# 🌍 Projet 3W – Worldwide Weather Watcher

## 🧭 Introduction
Le projet **3W (Worldwide Weather Watcher)** consiste à concevoir un **prototype de station météo embarquée** destinée à équiper des navires.  
Ces stations permettront, à long terme, **d’échanger des données météorologiques** afin de **prévoir des catastrophes naturelles** telles que les cyclones.

La station météo recueille différentes mesures à l’aide de capteurs (température, pression, humidité, etc.) et exploite ces données :
- pour fournir des **informations instantanées** à l’équipage ;
- pour **enregistrer les mesures** sur une carte SD afin d’assurer un suivi dans le temps.


---

## 📄 Sujet du projet
### Énoncé
L’**Agence Internationale pour la Vigilance Météorologique (AIVM)** lance un projet ambitieux :  
déployer dans les océans des **navires de surveillance équipés de stations météo embarquées**, capables de mesurer les paramètres influant sur la formation de cyclones et autres phénomènes extrêmes.

Plusieurs sociétés de transport maritime ont accepté d’équiper leurs navires avec ces stations, à condition qu’elles soient :
- **simples à utiliser**,  
- **efficaces**,  
- **pilotables par un membre d’équipage** à l’aide d’une **documentation technique utilisateur**.

Une startup partenaire a été choisie pour la **conception du prototype**.

---

## ⚙️ Ressources et matériel

### 🧩 Matériel principal
- **Microcontrôleur :** AVR ATmega328 (intégré à une carte Arduino)
- **Lecteur de carte SD (SPI)** → sauvegarde des données
- **Horloge RTC (I2C)** → gestion de la date et de l’heure
- **LED RGB (2-wire)** → communication de l’état du système
- **2 boutons poussoirs (numériques)** → interaction avec le système

### 🌡️ Capteurs
- Pression atmosphérique (I2C ou SPI)
- Température de l’air (I2C ou SPI)
- Hygrométrie (I2C ou SPI)
- GPS (UART)
- Luminosité (analogique)

