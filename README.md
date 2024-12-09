# ElectricityDemandForecast
Prédiction de la consommation d'électricité en France pour une entreprise spécialisée dans les énergies renouvelables. Le projet utilise des séries temporelles corrigées des effets de température et désaisonnalisées (méthodes SARIMA et Holt-Winters)

## Description
Ce projet a pour objectif de prédire la consommation d'électricité en France pour une entreprise spécialisée dans les énergies renouvelables. Les prévisions prennent en compte l'effet de la température (DJU), la désaisonnalisation et les tendances pour proposer une estimation précise de la demande future.

## Contenu du projet
1. **Données** :  
   - **Source** : [ODRE Open Data Soft](https://odre.opendatasoft.com/).  
   - Données de consommation électrique mensuelle en France, combinées aux DJU (degrés jours unifiés) pour mesurer l’impact des variations de température.  

2. **Prétraitement** :  
   - Correction des données de consommation par régression linéaire pour isoler l'effet température.  
   - Désaisonnalisation par moyennes mobiles et décomposition des séries temporelles.  

3. **Modélisation** :  
   - **Méthode Holt-Winters** : Lissage exponentiel prenant en compte tendance et saisonnalité.  
   - **Méthode SARIMA** : Modèle ARIMA saisonnier optimisé pour séries présentant une saisonnalité forte.  

4. **Évaluation** :  
   - Analyse à posteriori des prédictions sur 12 mois (2020-2021).  
   - Comparaison des performances entre Holt-Winters et SARIMA.  

## Résultats
- **Modèle retenu :** SARIMA, offrant de meilleures performances et une meilleure précision sur les pics de consommation.  
- **Prédictions :** Consommation électrique pour les 12 prochains mois (2021-2022) en adéquation avec les tendances passées.  

## Technologies utilisées
- **Python** : pandas, NumPy, statsmodels, matplotlib, seaborn.  
- **Modèles de séries temporelles** : Holt-Winters, SARIMA.  

## Prochaines étapes
- Intégrer d’autres facteurs influençant la consommation (luminosité, précipitations).  
- Étendre les prédictions à des périodes plus longues (au-delà de 12 mois).  

## Lien vers les données  
- Consommation électrique : [ODRE Open Data Soft](https://odre.opendatasoft.com/).  
- DJU : [Cegibat GRDF](https://cegibat.grdf.fr/simulateur/calcul-dju).  

