# Les termes et concepts

Dans la première partie, nous avons [délimité le contexte métier du projet](./contextes.md). L'objectif de ce chapitre est de définir les principaux termes et concepts qui structureront le Référentiel National des Travaux de rénovation.

Pour y parvenir, nous nous référencerons autant que possible à des notions largement partagées dans le domaine de la rénovation énergétique, en particulier du fait de leur caractère réglementaire.

Commençons par une question, qu'est-ce qui compose une rénovation énergétique ?

Pendant des années, nous ne disposions pas d'une définition réglementaire. On parlait de rénovation lourde, complète ou globale, sans que les critères permettant de différencier ces rénovations d'autres ne soient unanimement partagés. Par chance, nous avons désormais à disposition une définition précise sur laquelle nous baser.

> Un bâtiment rénové performant est un bâtiment qui a traité les 6 postes de travaux (isolation des murs, des planchers bas et de la toiture, remplacement des menuiseries extérieures, ventilation et production de chauffage/eau chaude sanitaire) (...)

[La rénovation performante par étape](https://librairie.ademe.fr/batiment/4168-renovation-performante-par-etapes.html)

> L'étude des six postes de travaux de rénovation énergétique suivants : l'isolation des murs, l'isolation des planchers bas, l'isolation de la toiture, le remplacement des menuiseries extérieures, la ventilation, la production de chauffage et d'eau chaude sanitaire ainsi que les interfaces associées.

[b du 17° bis de l'article L111-1 du code de la construction et de l'habitation](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000043976954)

Un premier concept clé est ici révélé : celui du **Poste de rénovation**.

## Les Postes de rénovation

En se basant sur ces définitions, un **Poste** de travaux désigne une catégorie ou un ensemble de travaux regroupés par type d'intervention ou par zone du bâtiment. On en identifie 6 communes aux deux sources :

- Isolation des murs
- Isolation des combles et toitures
- Isolation des planchers bas
- Menuiseries extérieures
- Ventilation
- Chauffage et eau chaude sanitaire

D'autres Postes de rénovation sont frequemment employés dans la littérature de la performance énergétique, notamment dans la réglementation relative au Diagnostic de Performance Energétique :

- Refroidissement
- Protections solaires
- Régulation
- Réseau
- Production d'électricité

---

<br>
<i>Schéma descriptif d'une rénovation</i>

```mermaid
erDiagram
    direction LR
    Rénovation ||--|{ Poste : "Traitement des 6 postes de travaux"
```

<br>

---

La granularité du Poste n'est cependant pas assez fine pour être suffisante.

> La notion de « postes de travaux » n'est pas suffisante pour aborder les problématiques de conception et de mise en oeuvre. Pour chaque poste, on distingue de multiples configurations : pour les murs : (Isolation Thermique par l'Extérieur, Isolation Thermique par l'Intérieur, ou mixte ITE/ITI), pour les toitures (combles perdus, rampants, sarking, toiture-terrasse…), pour les planchers bas (sur terre-plein, sur vide-sanitaire, sur local non chauffé…), pour les menuiseries extérieures : pose en feuillure, en tunnel, en applique, « en rénovation » …), etc.

[La rénovation performante par étape](https://librairie.ademe.fr/batiment/4168-renovation-performante-par-etapes.html)

> Solution technique : un procédé constructif, un équipement, un principe ou un système mis en œuvre pour la construction ou la rénovation d'un bâtiment ;

[b du 17° bis de l'article L111-1 du code de la construction et de l'habitation](https://www.legifrance.gouv.fr/codes/article_lc/LEGIARTI000043976954)

Les sources de référence admettent toutes deux un sous ensemble du Poste de rénovation sous des termes différents : **configuration** et **solution**. Si le concept de Poste renvoit à l'idée de finalité - le quoi - cette nouvelle notion renseigne sur le moyen d'y parvenir - le comment.

Un autre terme s'est largement diffusé pour désigner cette dimension : le **Geste**.

## Les Gestes de rénovation

L'enjeu de la définition et de la comptabilisation des travaux de rénovation n'est pas né à avec ce projet. Ces dernières années, une question anime de nombreux débats : la différenciation des rénovations dites « globales » et des rénovations dites « par étapes ». C'est dans ce contexte que la notion de Geste s'est répandue, notamment dans le service public de la rénovation énergétique.

> Les principaux axes de travail de l'ONRE sont les suivants :
>
> - rénovation énergétique dans le résidentiel :
>   - suivi de l'ensemble des gestes de rénovation à partir de l'enquête Trélo sur les travaux de rénovation dans les logements (maisons individuelles, copropriétés et parc social) ;

[Observatoire national des travaux de rénovation énergétique](https://www.ecologie.gouv.fr/politiques-publiques/observatoire-national-renovation-energetique)

> MaPrimeRénov' permet de financer une rénovation par geste : le chauffage et / ou l'isolation.

[France Rénov'](https://france-renov.gouv.fr/aides/mpr)

En adaptant la définition réglementaire du code de la construction et de l'habitation, une proposition peut être ainsi formulée : Un **Geste** désigne un procédé constructif, un équipement, un principe ou un système mis en œuvre pour la rénovation énergétique d'un bâtiment.

---

<br>
<i>Schéma descriptif d'une rénovation</i>

```mermaid
erDiagram
    direction LR
    Rénovation ||--|{ Poste : "Traitement des 6 postes de travaux"
    Poste ||--|{ Geste : "Un Poste est traité par ou ou plusieurs Gestes"
```

<br>

---

Il existe plusieurs bases de données des gestes de rénovation, notamment celles utilisées dans le cadre des dispositifs de financement des travaux : Ma Prime Rénov' et les Certificats d'Economies d'Energie. En croisant leurs conventions respectives, nous sommes en mesure d'établir une première liste des gestes de rénovation.

## Rénovation globale et par étapes

Nous l'avons vu, une rénovation globale et par étapes partagent le même objectif - le traitement des 6 postes de travaux - mais se distinguent dans la temporalité de mise en oeuvre des différents gestes. Le délai entre la réalisation des gestes est par conséquent le principal discriminant d'une rénovation globale ou par étapes.

D'autres concepts interviennent dans la caractérisation d'une rénovation globale ou par étapes, comme les interfaces et les interactions entre les postes de travaux. Ces notions n'entrent cependant pas dans le périmètre de ce projet.

## En résumé

- Une rénovation énergétique désigne le traitement en une ou plusieurs **étapes** des 6 **postes** de travaux par la mise en oeuvre de tous les **gestes** nécessaires.

- Les **6 gestes** sont l'isolation des murs, l'isolation des planchers hauts, l'isolation des plancher bas, le ramplacement des menuiseries extérieures, la ventilation, la production de chauffage et d'eau chaude sanitaire.

- En croisant les gestes couverts par les dispositifs **Ma Prime Rénov'** et des **Certificats d'Economies d'Energie**, on peut compiler une première base des gestes de rénovation.

- Une **rénovation globale** peut être distinguer d'une **rénovation par étapes** sur la base des **délais** entre les gestes mis en oeuvre.

Dans le [prochain chapitre](./regles.md), nous établierons les règles qui traduisent le domaine métier du projet.
