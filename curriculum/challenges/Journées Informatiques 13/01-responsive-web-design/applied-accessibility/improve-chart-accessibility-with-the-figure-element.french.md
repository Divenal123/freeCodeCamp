---
id: 587d778a367417b2b2512aa5
title: Improve Chart Accessibility with the figure Element
challengeType: 0
videoUrl: 'https://scrimba.com/c/cGJMqtE'
forumTopicId: 301015
---

## Description
<section id='description'>
HTML5 introduit le <code>figure</code> élément, ainsi que les éléments <code>figcaption</code>. Utilisés ensemble, ces éléments enveloppent une représentation visuelle (comme une image, un diagramme ou un graphique) avec sa légende. Cela donne une double accessibilité à la fois en regroupant sémantiquement le contenu lié et en fournissant une alternative textuelle qui explique la <code>figure</code>.
Pour les visualisations de données comme les graphiques, la légende peut être utilisée pour noter brièvement les tendances ou les conclusions pour les utilisateurs ayant une déficience visuelle. Un autre défi consiste à déplacer une version tableau des données du graphique hors écran (à l'aide de CSS) pour les utilisateurs de lecteurs d'écran.
Voici un exemple - notez que le <code>figcaption</code> va à l'intérieur du <code>figure</code> tags et peut être combiné avec d'autres éléments:

```html
<figure>
  <img src="roundhouseDestruction.jpeg" alt="Photo of Camper Cat executing a roundhouse kick">
  <br>
  <figcaption>
    Master Camper Cat démontre la forme appropriée d'un coup de pied circulaire.
  </figcaption>
</figure>
```

</section>

## Instructions
<section id='instructions'>
Camper Cat travaille dur pour créer un graphique à barres empilées indiquant le temps par semaine pour passer une formation en furtivité, en combat et en armes. Aidez-le à mieux structurer sa page en changeant le<code>div</code> tag qu'il a utilisé pour un <code>figure</code> et la balise<code>p</code> balise qui entoure la légende d'un <code>figcaption</code> étiquette.
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: Your code should have one <code>figure</code> tag.
    testString: assert($('figure').length == 1);
  - text: Your code should have one <code>figcaption</code> tag.
    testString: assert($('figcaption').length == 1);
  - text: Your code should not have any <code>div</code> tags.
    testString: assert($('div').length == 0);
  - text: Your code should not have any <code>p</code> tags.
    testString: assert($('p').length == 0);
  - text: The <code>figcaption</code> should be a child of the <code>figure</code> tag.
    testString: assert($('figure').children('figcaption').length == 1);
  - text: Your <code>figure</code> element should have a closing tag.
    testString: assert(code.match(/<\/figure>/g) && code.match(/<\/figure>/g).length === code.match(/<figure>/g).length);

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='html-seed'>

```html
<body>
  <header>
    <h1>Formation</h1>
    <nav>
      <ul>
        <li><a href="#stealth">Furtif &amp; Agilité</a></li>
        <li><a href="#combat">Combat</a></li>
        <li><a href="#weapons">Armes</a></li>
      </ul>
    </nav>
  </header>
  <main>
    <section>

      <!-- Add your code below this line -->
      <div>
        <!-- Stacked bar chart will go here -->
        <br>
        <p>Répartition par semaine de temps pour passer une formation en furtivité, combat et armes.</p>
      </div>
      <!-- Add your code above this line -->

    </section>
    <section id="stealth">
      <h2>Furtive &amp; Entraînement d'agilité</h2>
      <article><h3>Grimper le feuillage rapidement en utilisant une approche d'arbre couvrant minimum</h3></article>
      <article><h3>Aucune formation n'est NP-complète sans parkour</h3></article>
    </section>
    <section id="combat">
      <h2>Entraînement au combat</h2>
      <article><h3>Envoyez plusieurs ennemis avec des tactiques multithread</h3></article>
      <article><h3>Au revoir: 5 façons éprouvées d'éliminer un adversaire</h3></article>
    </section>
    <section id="weapons">
      <h2>Entraînement aux armes</h2>
      <article><h3>Épées: le meilleur outil pour diviser et conquérir littéralement</h3></article>
      <article><h3>Avant-première ou avant-première dans l'entraînement multi-armes?</h3></article>
    </section>
  </main>
  <footer>&copy; 2018 Camper Cat</footer>
</body>
```

</div>



</section>

## Solution
<section id='solution'>

```html
<body>
  <header>
    <h1>Training</h1>
    <nav>
      <ul>
        <li><a href="#stealth">Furtive &amp; Agility</a></li>
        <li><a href="#combat">Combat</a></li>
        <li><a href="#weapons">Armes</a></li>
      </ul>
    </nav>
  </header>
  <main>
    <section>

      <!-- Add your code below this line -->
      <figure>
        <!-- Stacked bar chart will go here -->
        <br>
        <figcaption>Répartition par semaine de temps pour passer une formation en furtivité, combat et armes.</figcaption>
      </figure>
      <!-- Add your code above this line -->

    </section>
    <section id="stealth">
      <h2>Furtive &amp; Entraînement d'agilité</h2>
      <article><h3>Grimper le feuillage rapidement en utilisant une approche d'arbre couvrant minimum</h3></article>
      <article><h3>Aucune formation n'est NP-complète sans parkour</h3></article>
    </section>
    <section id="combat">
      <h2>Entraînement au combat</h2>
      <article><h3>Envoyez plusieurs ennemis avec des tactiques multithread</h3></article>
      <article><h3>Au revoir: 5 façons éprouvées d'éliminer un adversaire</h3></article>
    </section>
    <section id="weapons">
      <h2>Entraînement aux armes</h2>
      <article><h3>Épées: le meilleur outil pour diviser et conquérir littéralement</h3></article>
      <article><h3>Avant-première ou avant-première dans l'entraînement multi-armes?</h3></article>
    </section>
  </main>
  <footer>&copy; 2018 Camper Cat</footer>
</body>
```

</section>
