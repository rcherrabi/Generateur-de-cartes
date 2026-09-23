# Générateur de cartes# 🗺️ 

> **Extension PyQGIS de production et d'automatisation cartographique pour l'instruction de permis de construire (PC1), cartes d'enjeux réglementaires (CER) ...**

---

## 📌 Enjeux métiers & Contexte

Au sein du service cartographique, la confection manuelle de pièces graphiques constitue l'un des postes les plus chronophages. Chaque dossier d'avant-projet ou d'instruction administrative impose la livraison de documents visuels rigoureusement normés :
* **Prises de vue du projet dans son environnement (pièce PC1 du permis de construire)**;
* **Cartes des Enjeux Réglementaires (CER)** croisant les zonages environnementaux et les servitudes locales ;
* **Cartes des points extrémaux (CETI)** pour figer les coordonnées géodésiques du périmètre foncier ;
* **Cartes de délimitation foncière et de localisation (communale et départementale)** pour la concertation publique.

Auparavant, la configuration manuelle du composeur d'impression (chargement des couches, calage des échelles, placement des logos, orientation, légendes dynamiques) prenait entre **20 et 30 minutes par carte** et risquait d'engendrer des disparités graphiques. 

**Le Générateur de Cartes** élimine cette tâche répétitive en pilotant l'API de mise en page de QGIS pour générer des livrables complets en **quelques secondes**, tout en garantissant le respect strict de la charte graphique d'entreprise.

---

## 🛠️ Compétences & Technologies mises en œuvre

* **Langages & Frameworks :** Python 3, PyQGIS (`QgsPrintLayout`, `QgsLayoutItemMap`, `QgsLayoutItemLegend`), PyQt5
* **Automatisation SIG :** Moteurs de rendu QGIS, génération d'atlas dynamiques, injection automatique de fonds raster (IGN, Google Satellite)
* **Bases de données spatiales :** Connexion directe et sécurisée à **PostgreSQL / PostGIS** avec filtrage par index `code_dep`
* **Traitements géométriques :** Calcul d'emprises englobantes (*bounding boxes*), intersections administratives, extraction de sommets et calcul de vecteurs d'angles de vue

---

## 🖥️ Console de pilotage PyQt

L'interface sépare les étapes d'accès aux données (connexion AWS/PostgreSQL, import KML, choix du dossier) de la composition cartographique (choix du modèle, échelles, surcharges) :

![Interface Générateur de Cartes](interface_generateur_cartes.png)


---

## 📈 Valeur ajoutée mesurable

* ⏱️ **Gain de temps :** passage de 25 minutes de montage manuel à **moins de 10 secondes** par planche cartographique.
* 🎯 **Fiabilité & Conformité graphique :** suppression totale des erreurs de manipulation, respect strict de la charte visuelle d'entreprise (polices, logos, échelles normalisées).
* 📂 **Désengorgement du pôle SIG :** autonomie accrue accordée aux chargés d'études pour la production des pièces de faisabilité.


