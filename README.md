# Thalie — Le nuancier des fleurs suisses

## But

Ce projet est un projet exploratoire permettant de découvrir la biodiversité suisse à travers les couleurs. Les fleurs changent selon l’altitude et le moment de l’année. Notre but principal était traduire les données en paysage visuel et de transformer des données scientifiques en une expérience immersive et artistique.

## Description

Ce site est une visualisation en scrollytelling de la flore suisse organisée par altitude et par mois de floraison. Le site se compose de deux vues : un écran d'accueil avec une grille de couleurs (mode aléatoire ou organisée par altitude et mois) et une section d'exploration interactive avec trois paysages SVG illustrés (montagne, plaine, ville). En faisant défiler la page, l'altitude change progressivement et les formes du paysage se colorent avec les teintes des espèces qui fleurissent à ce niveau. Un filtre par mois permet d'affiner la sélection et de découvrir les différences florales entre les saisons. Cliquer sur une forme ou sur une couleur dominante ouvre une fiche détaillée de la fleur correspondante. La page d'accueil contient également une librairie regroupant toutes les fleurs présentes sur le site, permettant aux utilisateurs d’explorer l’ensemble des espèces indépendamment des filtres utilisés dans la partie explorative. 

## Données et leur manipulation

Les données des espèces de fleurs proviennent d'Info Flora via GBIF (téléchargement d'occurrences filtrées sur la Suisse). Les altitudes minimum et maximum ont été calculées grâce aux longitudes et latitudes des espèces de GBIF et l'aide de l'API de SwissTopo. Les images sont libres de droit et récupérées depuis Wikimedia Commons et iNaturalist. Les couleurs et floraisons viennent de Wikidata et vérifiées à la main. Claude a été utilisé pour la rédaction des descriptions et "fun facts", puis vérifiées à la main.

Avec plus de 5 millions d'entrées et 3'444 espèces, nous avons d'abord filtré les espèces les plus représentées pour n'en garder que 197 en gardant un scope réaliste pour le projet. Nous avons ensuite défini l'altitude minimale et maximale de l'apparition de ces fleurs grâce à un script Python (fourni par Claude AI) et l'aide de l'API SwissTopo pour trouver l'altitude en fonction de la latitude et de la longitude. Pour les mois de floraison, les images et les couleurs principales, nous avons utilisé les bases de données "Wikidata" et "iNaturalist". Ces données ont dû être vérifiées manuellement, car certaines espèces n'avaient pas de couleur attitrée ou des périodes de floraison trop larges.

## Biais et améliorations

Après étude des données, nous avons remarqué que les espèces les plus recensées sont parfois des espèces invasives. En effet, il est plus logique de répertorier les apparitions de ces espèces que celles de fleurs plus communes comme le pissenlit, qui, malgré leur forte présence sur le terrain, restent sous-représentées dans les relevés car elles sont perçues comme banales et donc moins signalées.

## Planches et prototype

<ul>
<li>
<a href="https://www.figma.com/design/75HxPTTM8YXUpJtecaTIjy/VisualDon---Projet?node-id=78-213&t=2Z7AEFECnkqlfLTj-1](https://www.figma.com/design/75HxPTTM8YXUpJtecaTIjy/VisualDon---Projet?node-id=0-1&t=2Z7AEFECnkqlfLTj-1)">Planches Figma</a>
</li><li>
<a href="https://www.figma.com/proto/75HxPTTM8YXUpJtecaTIjy/VisualDon---Projet?page-id=0%3A1&node-id=38-1265&viewport=-1214%2C175%2C0.31&t=fhLXxFiaLW7x77w3-1&scaling=min-zoom&content-scaling=fixed&starting-point-node-id=34%3A30">Prototype Figma</a></li>
</ul>

## Références

### Graphiques

<ul>
<li><a href="https://pudding.cool/2021/03/foundation-names/">The Naked Truth</a></li>
<li><a href="https://www.huedata.ai/#!/">Hue Data</a></li>
  <li><a href="https://movies-palettes.adriencarpentier.com/">Movies Palettes</a></li>
  <li><a href="https://pudding.cool/2024/09/courts/">Every Outdoor Basketball Court in the U.S.A.</a></li>
  <li><a href="https://plantica.net/en/">Plantica</a></li>
</ul>
<h3>Données</h3>
<ul>
<li><a href="https://www.infoflora.ch/fr/">Info Flora</a> - Crédits : GBIF.org (26 March 2026) GBIF Occurrence Download  <a href="https://doi.org/10.15468/dl.2a3ar3">https://doi.org/10.15468/dl.2a3ar3</a></li>
  <li><a href='https://entrepot.recherche.data.gouv.fr/dataset.xhtml%3Bjsessionid%3De0c12d34ff0227753206ff44a48b?fileAccess=&fileSortField=size&fileTypeGroupFacet="Other"&persistentId=doi%3A10.15454%2FADCQHT&q=&version'>FlorealData</a></li>
  <li><a href="https://commons.wikimedia.org/">Wikimedia Commons</a> - Images des fleurs</li>
  <li><a href="https://www.swisstopo.admin.ch/">Swiss Topo</a> - Altitudes</li>
  <li><a href="https://www.wikidata.org/">Wikidata</a> - Couleurs et floraisons des espèces, puis vérifiées à la main</li>
  <li><a href="https://www.inaturalist.org/">iNaturalist</a> - Images des fleurs</li>
  <li><a href="https://www.anthropic.com/claude">Claude (Anthropic)</a> - Scripts Python et rédaction des descriptions et fun facts, vérifiés à la main</li>
</ul>
