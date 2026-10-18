# NutriTerra — disponibilité alimentaire et pertes

Proposer un panel de territoires à étudier, documenter la qualité des bilans et chiffrer des scénarios théoriques sans assimiler disponibilité nationale et consommation individuelle.

## Mon approche

Je contrôle la qualité des données et les clés avant de calculer les indicateurs. Je compare les résultats, explicite les hypothèses et propose des actions à vérifier avec le métier. Ce projet utilise des données synthétiques et ne correspond à aucune mission réelle.

## Méthodes

- Jointures contrôlées, journal des anomalies, grille complète pays×année et marquage de complétude.
- Interpolation rétrospective par pays/produit, indicateur d’imputation, conversions et balance des flux.
- Contributions par produit, pondérations population, dépendance aux importations et comparaisons temporelles.
- Douze scénarios, distribution des gains et discussion des biais de couverture.

## Livrables

- [Notebook Jupyter](notebooks/analyse.ipynb) : calculs exécutés, graphiques et analyse détaillée.
- [Rapport PowerPoint](presentation/soutenance.pptx) : présentation modifiable.
- [Rapport PDF](presentation/soutenance.pdf) : version de lecture.
- [Synthèse des résultats](analysis/SYNTHESE.md).
- `data/` et `analysis/` : sources, tables nettoyées et résultats au format CSV.

## Reproduire l’analyse

Installer Python 3.12 et les dépendances avec `python -m pip install -r requirements.txt`. Ouvrir le notebook dans Jupyter ou VS Code, choisir le noyau Python installé et exécuter toutes les cellules dans l’ordre. La graine de simulation est fixe. Les sources sont régénérées à l’exécution ; ne pas remplacer ces CSV par des données réelles sans adapter le chargement.

La dernière cellule recrée le PowerPoint. Pour actualiser le PDF après modification, ouvrir la présentation dans PowerPoint ou LibreOffice Impress puis l’exporter en PDF. Les graphiques sont des images et les textes restent modifiables.

Les données fictives, les méthodes et les limites sont détaillées dans le notebook. Les résultats ne constituent pas une performance démontrée en situation réelle.

## Aperçu

![Graphique de l’analyse](reports/dependance_et_disponibilite.png)

## Quelques repères

Ces valeurs décrivent le jeu synthétique utilisé dans ce projet.

| Indicateur | Valeur |
|---|---:|
| lignes valides | 48 575 |
| pays | 180 |
| pays annees incomplets | 2 |
| importations imputees | 380 |
