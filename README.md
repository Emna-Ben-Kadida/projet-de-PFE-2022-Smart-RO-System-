# projet-de-PFE-2022-Smart-RO-System-
# 🌊 Smart RO System 🌊

## Contexte et Objectifs 🚰
Le projet **Smart RO System**, réalisé par moi, Emna Ben Kadida et ma partenaire Nour Challouf, a pour objectif de moderniser un système de **dessalement par osmose inverse (RO)** au **Centre de Recherches et des Technologies des Eaux (CERTE)** en Tunisie. Dans un contexte de pénurie hydrique croissante, le projet s'inscrit dans le cadre du programme **TWEED** financé par le **DAAD**, visant à renforcer les capacités en gestion de l'eau et de l'énergie.

### Objectifs principaux :
- 🌐 **Surveillance en temps réel** des paramètres de l'eau (pH, conductivité, débit, niveau).
- ⚙️ **Contrôle automatisé** des électrovannes pour ajuster la qualité de l'eau.
- 🖥️ **Interface de supervision** à distance via un tableau de bord et une interface web.

## État de l'art et Innovations 💡

### 1. Dessalement par osmose inverse (RO) 🔬
**Technologie existante** : L'osmose inverse est une méthode éprouvée pour éliminer les sels et minéraux de l'eau. Cependant, les systèmes traditionnels reposent sur des opérations manuelles, entraînant des risques d'erreurs et une faible réactivité.

**Innovation du projet** : Le projet intègre des **capteurs IoT** et de l'**automatisation** pour optimiser le processus, avec trois qualités d'eau produites (osmose, déminéralisée, ultrapure) et une précision accrue.

### 2. Internet des Objets (IoT) 🌐
**État de l'art** : L'IoT est utilisé pour la **gestion de l'eau**, la collecte de données, la surveillance à distance et l'automatisation. Les protocoles comme **MQTT** et les microcontrôleurs tels que **ESP32** sont utilisés pour leur faible consommation énergétique.

**Choix technologiques** :
- **ESP32-WROOM-32** : Pour sa double connectivité (Wi-Fi/Bluetooth), sa puissance de traitement (160 MHz, double cœur) et son coût modéré.
- **Raspberry Pi 4** : Serveur central pour le traitement des données, compatible avec plusieurs OS et doté de capacités réseau puissantes.
- **Capteurs** : YF-S401 (débit), électrovannes à solénoïde (contrôle NC/NO), et API REST pour récupérer des données (pH, conductivité).
- **Protocoles** : **MQTT** pour une communication fluide entre l'ESP32 et le Raspberry Pi.

## Architecture du Système 🛠️

### 1. Niveaux fonctionnels 🔄
- **Acquisition de données** : Les capteurs de débit et les électrovannes sont connectés à l'ESP32, qui collecte et transmet les données au Raspberry Pi via MQTT.
- **Traitement** : Le Raspberry Pi analyse les données (y compris pH, conductivité via API), et envoie des commandes aux électrovannes.
- **Visualisation** : Un tableau de bord Node-RED affiche les paramètres en temps réel, avec contrôle manuel ou automatique via une interface web dynamique (HTML/CSS, BootstrapVue).

### 2. Automatisation 🤖
- **Contrôle des électrovannes** :
  - **Valve 1 (osmose)** : Activée par le niveau d'eau (ouverte si niveau ≥ 5 cm).
  - **Valve 2 (prétraitée)** : Contrôlée par le pH (6,5–8,5), la conductivité (0,3–0,6 mS/cm) et le niveau.

- **Modes de fonctionnement** :
  - **Automatique** : Production d'eau "douce" ou "salée" via des ratios prédéfinis.
  - **Manuel** : Permet à l'utilisateur de spécifier la quantité de sel désirée.

## Avantages par rapport aux systèmes traditionnels ⚖️

| Fonctionnalité  | Sans IoT  | Avec IoT  |
|-----------------|-----------|-----------|
| **Sécurité**     | Accès non contrôlé | Authentification requise |
| **Précision**    | Mesures manuelles | Capteurs haute précision |
| **Temps de réponse** | Minutes à heures | Temps réel (< 1 s) |
| **Automatisation** | Intervention humaine | Contrôle via dashboard |
| **Surveillance**  | Visuelle/Manuelle | Visualisation web dynamique |
| **Complexité**   | Opérations manuelles | Interface simplifiée |

## Résultats et Perspectives 🚀

- **Efficacité** : Réduction des erreurs humaines et optimisation de la consommation d'eau avec des seuils dynamiques.
- **Évolutivité** : L'architecture modulaire permet d'étendre le système aux unités RO 2 et 3 pour une automatisation complète.
- **Applications futures** : Intégration de l'IA pour prédire les pannes ou ajuster les paramètres en fonction des tendances historiques.

## Conclusion 🎯

Le **Smart RO System** illustre comment l'IoT peut moderniser les infrastructures hydrauliques existantes. Grâce à des **microcontrôleurs performants**, des **protocoles de communication adaptés**, et des **interfaces utilisateur intuitives**, ce projet répond aux défis de la gestion de l'eau dans un contexte de stress hydrique.

Ce projet s'aligne sur les tendances mondiales de l'industrie 4.0, où l'**automatisation** et la **connectivité** sont des clés pour une gestion durable des ressources. 🌍💧

---

## Ressources supplémentaires 📂

Malheureusement, **le code source du projet a été perdu**. Cependant, j'ai mis à disposition des ressources alternatives pour mieux comprendre le projet :

J'ai importé donc le rapport en PDF avec des explications complètes sur le projet avec uelques captures montrant des extraits du code et de la configuration du système.

---

> **Remarque** : Ce projet est financé par le programme **TWEED** (DAAD), en partenariat avec le **CERTE**.  
