<img src="https://github.com/user-attachments/assets/311a3983-f518-4410-8429-bc025f07f575" alt="Logo 3W" width="100" align="right" />
<br><br>


# 🌍 Projet 3W – Worldwide Weather Watcher

![C++](https://img.shields.io/badge/C++-17-blue.svg) ![Arduino](https://img.shields.io/badge/Arduino-1.8-orange.svg) 

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

---

## ⚙️ Ressources et matériel

### 🧩 Matériel principal
- **Microcontrôleur :** AVR ATmega328 (intégré à une carte Arduino)
- **Lecteur de carte SD (SPI)** → sauvegarde des données
- **Horloge RTC (I2C)** → gestion de la date et de l’heure
- **LED RGB (2-wire)** → communication de l’état du système
- **2 boutons poussoirs (numériques)** → interaction avec le système

### 🌡️ Capteurs
- Pression atmosphérique (I2C)
- Température de l’air (I2C)
- Hygrométrie (I2C)
- GPS (UART)
- Luminosité (analogique)

![Photo-Montage-CarteArduino](https://github.com/user-attachments/assets/112b3599-1fb2-40b1-9728-387c1b513694)

## ⚙️ Les fonctionnalités clés du système

- 🟢 **Mode Standard (LED verte)** : fonctionnement normal. Acquisition complète et enregistrement sur la carte SD de toutes les données à intervalles réguliers.  
- 🔵 **Mode Économique (LED bleue)** : optimisation de la batterie 🔋. L’intervalle de mesure est doublé et l’acquisition GPS n’est effectuée qu’une fois sur deux.  
- 🟡 **Mode Configuration (LED jaune)** : mode technicien (accessible au démarrage) permettant de régler les paramètres du système et des capteurs (seuils, intervalles) via le moniteur série.  
- 🟠 **Mode Maintenance (LED orange)** : mode technicien qui suspend l’écriture sur la carte SD pour permettre son retrait en toute sécurité et la consultation des données en direct sur le moniteur série.


---
Projet réalisé dans le cadre du module SE (Systèmes Embarqués) de l'école d'ingénieurs CESI.
