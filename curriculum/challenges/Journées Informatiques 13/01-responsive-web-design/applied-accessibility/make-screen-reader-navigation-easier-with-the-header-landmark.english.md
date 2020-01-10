---
id: 587d7787367417b2b2512aa1
title: Make Screen Reader Navigation Easier with the header Landmark
challengeType: 0
videoUrl: 'https://scrimba.com/c/cB76vtv'
forumTopicId: 301023
---

## Description
<section id='description'>
Le prochain élément HTML5 qui ajoute une signification sémantique et améliore l'accessibilité est le <code>header</code> étiquette. Il est utilisé pour encapsuler des informations d'introduction ou des liens de navigation pour sa balise parent et fonctionne bien autour du contenu qui est répété en haut sur plusieurs pages.
<code>header</code> partage la fonction de point de repère intégrée que vous avez vue avec <code>principal</code>, permettant aux technologies d'assistance d'accéder rapidement à ce contenu.
<strong>Note:</strong> le <code>header</code> est destiné à être utilisé dans la balise <code> body </code> de votre document HTML. Ceci est différent du<code>head</code> élément, qui contient le titre de la page, les méta-informations, etc.
</section>

## Instructions
<section id='instructions'>
Camper Cat est en train d'écrire d'excellents articles sur la formation des ninjas et souhaite ajouter une page pour eux sur son site. Changer le haut <code>div</code> qui contient actuellement le <code>h1</code> à un <code>header</code> à la place.
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: Your code should have one <code>header</code> tag.
    testString: assert($('header').length == 1);
  - text: Your <code>header</code> tags should wrap around the <code>h1</code>.
    testString: assert($('header').children('h1').length == 1);
  - text: Your code should not have any <code>div</code> tags.
    testString: assert($('div').length == 0);
  - text: Your <code>header</code> element should have a closing tag.
    testString: assert(code.match(/<\/header>/g) && code.match(/<\/header>/g).length === code.match(/<header>/g).length);

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='html-seed'>

```html
<body>

  <div>
    <h1>Formation avec Camper Cat</h1>
  </div>


  <main>
    <section id="stealth">
      <h2>Furitve &amp; Agilité d'entraînelent</h2>
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
  </header>


  <main>
    <section id="stealth">
      <h2>Furtive &amp; Agilité d'entraînement</h2>
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

</section>
