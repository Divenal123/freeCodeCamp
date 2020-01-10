---
id: 587d778d367417b2b2512aaa
title: Make Elements Only Visible to a Screen Reader by Using Custom CSS
challengeType: 0
videoUrl: 'https://scrimba.com/c/cJ8QGkhJ'
forumTopicId: 301020
---

## Description
<section id='description'>
Avez-vous remarqué que tous les défis d'accessibilité appliqués jusqu'à présent n'ont pas utilisé de CSS? Il s'agit de montrer l'importance d'un plan de document logique et d'utiliser des balises sémantiquement significatives autour de votre contenu avant d'introduire l'aspect de la conception visuelle.
Cependant, la magie de CSS peut également améliorer l'accessibilité de votre page lorsque vous souhaitez masquer visuellement du contenu destiné uniquement aux lecteurs d'écran. Cela se produit lorsque les informations sont au format visuel (comme un graphique), mais que les utilisateurs de lecteurs d'écran ont besoin d'une présentation alternative (comme un tableau) pour accéder aux données. CSS est utilisé pour positionner les éléments de lecture d'écran uniquement hors de la zone visuelle de la fenêtre du navigateur.
Voici un exemple des règles CSS qui accomplissent cela:

```css
.sr-only {
  position: absolute;
  left: -10000px;
  width: 1px;
  height: 1px;
  top: auto;
  overflow: hidden;
}
```

<strong>Note:</strong> Les approches CSS suivantes ne feront PAS la même chose:
<ul>
<li><code>display: none;</code> or <code>visibility: hidden;</code> masque le contenu pour tout le monde, y compris les utilisateurs de lecteurs d'écran </li>
<li>Valeurs nulles pour les tailles de pixels, telles que <code>width: 0px; height: 0px;</code> supprime cet élément du flux de votre document, ce qui signifie que les lecteurs d'écran l'ignoreront</li>
</ul>
</section>

## Instructions
<section id='instructions'>
Camper Cat a créé un graphique à barres empilées vraiment cool pour sa page de formation et a mis les données dans un tableau pour ses utilisateurs malvoyants. La table a déjà un <code>sr-only</code> class, mais les règles CSS ne sont pas encore remplies. Donner la <code>position</code> une valeur absolue, la <code>left</code> a -10000px value, et le <code>width</code> le <code>height</code> les deux valeurs 1px.
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: Your code should set the <code>position</code> property of the <code>sr-only</code> class to a value of absolute.
    testString: assert($('.sr-only').css('position') == 'absolute');
  - text: Your code should set the <code>left</code> property of the <code>sr-only</code> class to a value of -10000px.
    testString: assert($('.sr-only').css('left') == '-10000px');
  - text: Your code should set the <code>width</code> property of the <code>sr-only</code> class to a value of 1 pixel.
    testString: assert(code.match(/width:\s*?1px/gi));
  - text: Your code should set the <code>height</code> property of the <code>sr-only</code> class to a value of 1 pixel.
    testString: assert(code.match(/height:\s*?1px/gi));

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='html-seed'>

```html
<head>
  <style>
  .sr-only {
    position: ;
    left: ;
    width: ;
    height: ;
    top: auto;
    overflow: hidden;
  }
  </style>
</head>
<body>
  <header>
    <h1>Entraînement</h1>
    <nav>
      <ul>
        <li><a href="#stealth">Furtive &amp; Agilité</a></li>
        <li><a href="#combat">Combat</a></li>
        <li><a href="#weapons">Armes</a></li>
      </ul>
    </nav>
  </header>
  <section>
    <h2>Programme d'entraînement de trois semaines de Master Camper Cat</h2>
    <figure>
      <!-- Stacked bar chart of weekly training-->
      <p>[Graphique à barres empilées]</p>
      <br />
      <figcaption>Répartition par semaine de temps pour passer une formation en furtivité, combat et armes.</figcaption>
    </figure>
    <table class="sr-only">
      <caption>Heures d'entraînement hebdomadaire en furtivité, combat et armes</caption>
      <thead>
        <tr>
          <th></th>
          <th scope="col">Furtive &amp; Agilité</th>
          <th scope="col">Combat</th>
          <th scope="col">Armes</th>
          <th scope="col">Total</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th scope="row">Semaine un</th>
          <td>3</td>
          <td>5</td>
          <td>2</td>
          <td>10</td>
        </tr>
        <tr>
          <th scope="row">Semaine deux</th>
          <td>4</td>
          <td>5</td>
          <td>3</td>
          <td>12</td>
        </tr>
        <tr>
          <th scope="row">Semaine trois</th>
          <td>4</td>
          <td>6</td>
          <td>3</td>
          <td>13</td>
        </tr>
      </tbody>
    </table>
  </section>
  <section id="stealth">
    <h2>Furtive &amp; Agilité de l'entraînement</h2>
    <article><h3>Grimper le feuillage rapidement en utilisant une approche d'arbre couvrant minimum</h3></article>
    <article><h3>Aucune formation n'est NP-complète sans parkour</h3></article>
  </section>
  <section id="combat">
    <h2>Entraînement au combat</h2>
    <article><h3>Envoyez plusieurs ennemis avec des tactiques multithread</h3></article>
    <article><h3>Au revoir, monde: 5 façons éprouvées d'éliminer un adversaire</h3></article>
  </section>
  <section id="weapons">
    <h2>Entraînement aux armes</h2>
    <article><h3>Épées: le meilleur outil pour diviser et conquérir littéralement</h3></article>
    <article><h3>Avant-première ou avant-première dans l'entraînement multi-armes?</h3></article>
  </section>
  <footer>&copy; 2018 Camper Cat</footer>
</body>
```

</div>



</section>

## Solution
<section id='solution'>

```html
<head>
  <style>
  .sr-only {
    position: absolute;
    left: -10000px;
    width: 1px;
    height: 1px;
    top: auto;
    overflow: hidden;
  }
  </style>
</head>
<body>
  <header>
    <h1>Training</h1>
    <nav>
      <ul>
        <li><a href="#stealth">Furtive &amp; Agilité</a></li>
        <li><a href="#combat">Combat</a></li>
        <li><a href="#weapons">Armes</a></li>
      </ul>
    </nav>
  </header>
  <section>
    <h2>Programme d'entraînement de trois semaines de Master Camper Cat</h2>
    <figure>
      <!-- Stacked bar chart of weekly training-->
      <p>[Graphique à barres empilées]</p>
      <br />
      <figcaption>Répartition par semaine de temps pour passer une formation en furtivité, combat et armes.</figcaption>
    </figure>
    <table class="sr-only">
      <caption>Heures d'entraînement hebdomadaire en furtivité, combat et armes</caption>
      <thead>
        <tr>
          <th></th>
          <th scope="col">Furtive &amp; Agilité</th>
          <th scope="col">Combat</th>
          <th scope="col">Armes</th>
          <th scope="col">Total</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th scope="row">Semaine un</th>
          <td>3</td>
          <td>5</td>
          <td>2</td>
          <td>10</td>
        </tr>
        <tr>
          <th scope="row">Semaine deux</th>
          <td>4</td>
          <td>5</td>
          <td>3</td>
          <td>12</td>
        </tr>
        <tr>
          <th scope="row">Semaine trois</th>
          <td>4</td>
          <td>6</td>
          <td>3</td>
          <td>13</td>
        </tr>
      </tbody>
    </table>
  </section>
  <section id="stealth">
    <h2>Furtive &amp; Agilité de l'entraînement</h2>
    <article><h3>Grimper le feuillage rapidement en utilisant une approche d'arbre couvrant minimum</h3></article>
    <article><h3>Aucune formation n'est NP-complète sans parkour</h3></article>
  </section>
  <section id="combat">
    <h2>Entraînement au combat</h2>
    <article><h3>Envoyez plusieurs ennemis avec des tactiques multithread</h3></article>
    <article><h3>Au revoir, monde: 5 façons éprouvées d'éliminer un adversaire</h3></article>
  </section>
  <section id="weapons">
    <h2>Entraînement aux armes</h2>
    <article><h3>Épées: le meilleur outil pour diviser et conquérir littéralement</h3></article>
    <article><h3>Avant-première ou avant-première dans l'entraînement multi-armes?</h3></article>
  </section>
  <footer>&copy; 2018 Camper Cat</footer>
</body>
```

</section>
