---
id: 587d7788367417b2b2512aa2
title: Make Screen Reader Navigation Easier with the nav Landmark
challengeType: 0
videoUrl: 'https://scrimba.com/c/czVwWSv'
forumTopicId: 301024
---

## Description
<section id='description'>
Le <code>nav</code> L'élément est un autre élément HTML5 avec la fonction de point de repère intégré pour une navigation facile avec le lecteur d'écran. Cette balise est destinée à entourer les principaux liens de navigation de votre page.
S'il y a des liens de sites répétés au bas de la page, il n'est pas nécessaire de baliser ceux avec un <code>nav</code> tag aussi. Utilisant un<code>footer</code> (couvert dans le prochain défi) est suffisant.
</section>

## Instructions
<section id='instructions'>
Camper Cat a inclus des liens de navigation en haut de sa page de formation, mais les a enveloppés dans un<code>div</code>. Changer la <code>div</code> to a <code>nav</code> pour améliorer l'accessibilité de sa page.
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: Your code should have one <code>nav</code> tag.
    testString: assert($('nav').length == 1);
  - text: Your <code>nav</code> tags should wrap around the <code>ul</code> and its list items.
    testString: assert($('nav').children('ul').length == 1);
  - text: Your code should not have any <code>div</code> tags.
    testString: assert($('div').length == 0);
  - text: Your <code>nav</code> element should have a closing tag.
    testString: assert(code.match(/<\/nav>/g) && code.match(/<\/nav>/g).length === code.match(/<nav>/g).length);

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='html-seed'>

```html
<body>
  <header>
    <h1>Formation avec Camper Cat</h1>

    <div>
      <ul>
        <li><a href="#stealth">Furtive &amp; Agilité</a></li>
        <li><a href="#combat">Combat</a></li>
        <li><a href="#weapons">Armes</a></li>
      </ul>
    </div>

  </header>
  <main>
    <section id="stealth">
      <h2>Furtive &amp; Agilité de l'entraînement</h2>
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
</body>
```

</div>



</section>

## Solution
<section id='solution'>

```html
<body>
  <header>
    <h1>Formation avec Camper Cat</h1>

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
      <h2>Furitve &amp; Agilité d'entraînement</h2>
      <article><h3>Grimper le feuillage rapidement en utilisant une approche d'arbre couvrant minimum</h3></article>
      <article><h3>Aucune formation n'est NP-complète sans parkour</h3></article>
    </section>
    <section id="combat">
      <h2>Entraînement au combat</h2>
      <article><h3>Envoyez plusieurs ennemis avec des tactiques multithread</h3></article>
      <article><h3>Au revoir: 5 façons éprouvées d'éliminer un adversairet</h3></article>
    </section>
    <section id="weapons">
      <h2>Entraînement aux armesg</h2>
      <article><h3>Épées: le meilleur outil pour diviser et conquérir littéralement</h3></article>
      <article><h3>Avant-première ou avant-première dans l'entraînement multi-armes?</h3></article>
    </section>
  </main>
</body>
```

</section>
