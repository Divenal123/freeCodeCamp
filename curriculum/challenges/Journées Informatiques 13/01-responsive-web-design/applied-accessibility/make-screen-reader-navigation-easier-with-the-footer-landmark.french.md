---
id: 587d7788367417b2b2512aa3
title: Make Screen Reader Navigation Easier with the footer Landmark
challengeType: 0
videoUrl: 'https://scrimba.com/c/crVrDh8'
forumTopicId: 301022
---

## Description
<section id='description'>
Semblable à <code>header</code> et <code>nav</code>, le <code>footer</code> L'élément possède une fonction de point de repère intégrée qui permet aux appareils et accessoires fonctionnels d'y accéder rapidement. Il est principalement utilisé pour contenir des informations sur le droit d'auteur ou des liens vers des documents connexes qui se trouvent généralement au bas d'une page.
</section>

## Instructions
<section id='instructions'>
La page de formation de Camper Cat progresse bien. Changer la <code>div</code> La page de formation de Camper Cat progresse bien. Changer la  <code>footer</code> élement.
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: Your code should have one <code>footer</code> tag.
    testString: assert($('footer').length == 1);
  - text: Your code should not have any <code>div</code> tags.
    testString: assert($('div').length == 0);
  - text: Your code should have an opening and closing <code>footer</code> tag.
    testString: assert(code.match(/<footer>\s*&copy; 2018 Camper Cat\s*<\/footer>/g));

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='html-seed'>

```html
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
  <main>
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


  <div>&copy; 2018 Camper Cat</div>


</body>
```

</div>



</section>

## Solution
<section id='solution'>

```html
<body>
  <header>
    <h1>Formation</h1>
    <nav>
      <ul>
        <li><a href="#stealth">Furtive &amp; Agilité</a></li>
        <li><a href="#combat">Combat</a></li>
        <li><a href="#weapons">Armes/a></li>
      </ul>
    </nav>
  </header>
  <main>
    <section id="stealth">
      <h2>Furtive &amp; Agilité de la formation</h2>
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
      <article><h3>Formation en largeur ou en profondeur en formation multi-armes?</h3></article>
    </section>
  </main>


  <footer>&copy; 2018 Camper Cat</footer>


</body>
```

</section>
