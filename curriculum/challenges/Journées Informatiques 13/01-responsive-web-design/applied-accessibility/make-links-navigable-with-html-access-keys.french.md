---
id: 587d7790367417b2b2512aaf
title: Make Links Navigable with HTML Access Keys
challengeType: 0
videoUrl: 'https://scrimba.com/c/cQvmaTp'
forumTopicId: 301021
---

## Description
<section id='description'>
HTML propose l'attribut <code> accesskey </code> pour spécifier une touche de raccourci pour activer ou mettre en évidence un élément. Cela peut rendre la navigation plus efficace pour les utilisateurs utilisant uniquement le clavier.
HTML5 permet à cet attribut d'être utilisé sur n'importe quel élément, mais il est particulièrement utile lorsqu'il est utilisé avec des éléments interactifs. Cela inclut les liens, les boutons et les contrôles de formulaire.
Voici un exemple:
<code>&lt;touche accesskey =&quot;b&quot;&gt;Bouton important&lt;/button&gt;</code>
</section>

## Instructions
<section id='instructions'>
Camper Cat veut que les liens autour des deux titres d'articles de blog aient des raccourcis clavier afin que les utilisateurs de son site puissent accéder rapidement à l'histoire complète. Ajouter un <code>clef d'accès</code> attribuez aux deux liens et réglez le premier sur "g" (pour Garfield) et le second sur "c" (pour Chuck Norris).
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: Your code should add an <code>accesskey</code> attribute to the <code>a</code> tag with the <code>id</code> of "first".
    testString: assert($('#first').attr('accesskey'));
  - text: Your code should add an <code>accesskey</code> attribute to the <code>a</code> tag with the <code>id</code> of "second".
    testString: assert($('#second').attr('accesskey'));
  - text: Your code should set the <code>accesskey</code> attribute on the <code>a</code> tag with the <code>id</code> of "first" to "g". Note that case matters.
    testString: assert($('#first').attr('accesskey') == 'g');
  - text: Your code should set the <code>accesskey</code> attribute on the <code>a</code> tag with the <code>id</code> of "second" to "c". Note that case matters.
    testString: assert($('#second').attr('accesskey') == 'c');

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='html-seed'>

```html
<body>
  <header>
    <h1>Réflexions profondes avec Master Camper Cat</h1>
  </header>
  <article>


    <h2><a id="first" href="#">Les fichiers Garfield: la lasagne comme carburant d'entraînement?</a></h2>


    <p>Internet regorge d'opinions différentes sur les paradigmes nutritionnels, de la paléo de l'herbe à chat aux nettoyages des boules de poils. Mais tournons notre attention vers un carburant de fitness souvent négligé, et examinons le trifecta protéine-carb-NOM qu'est la lasagne ...</p>
  </article>
  <article>


    <h2><a id="second" href="#">Chuck Norris est-il un chat?</a></h2>


    <p>Chuck Norris est largement considéré comme le premier artiste martial de la planète, et c'est une coïncidence complète quiconque en désaccord avec ce fait disparaît mystérieusement peu de temps après. Mais la vraie question est, est-il un chat? ...</p>
  </article>
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
    <h1>Réflexions profondes avec Master Camper Cat</h1>
  </header>
  <article>


    <h2><a id="first" accesskey="g" href="#">Les fichiers Garfield: la lasagne comme carburant d'entraînement?</a></h2>


    <p>Internet regorge d'opinions différentes sur les paradigmes nutritionnels, de la paléo de l'herbe à chat aux nettoyages des boules de poils. Mais tournons notre attention vers un carburant de fitness souvent négligé, et examinons le trifecta protéine-carb-NOM qu'est la lasagne ...</p>
  </article>
  <article>


    <h2><a id="second" accesskey="c" href="#">Is Chuck Norris une personne chat?</a></h2>


    <p>Chuck Norris est largement considéré comme le premier artiste martial de la planète, et c'est une coïncidence complète quiconque en désaccord avec ce fait disparaît mystérieusement peu de temps après. Mais la vraie question est, est-il un chat? ...</p>
  </article>
  <footer>&copy; 2018 Camper Cat</footer>
</body>
```

</section>
