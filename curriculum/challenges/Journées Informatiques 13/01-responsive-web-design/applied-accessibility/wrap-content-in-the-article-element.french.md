---
id: 587d774e367417b2b2512aa0
title: Wrap Content in the article Element
challengeType: 0
videoUrl: 'https://scrimba.com/c/cPp79S3'
forumTopicId: 301029
---

## Description
<section id='description'>
<code>article</code> est un autre des nouveaux éléments HTML5 qui ajoute une signification sémantique à votre balisage. <code>article</code> est un élément de sectionnement et est utilisé pour encapsuler du contenu indépendant et autonome. La balise fonctionne bien avec les entrées de blog, les messages du forum ou les articles de presse.
Déterminer si le contenu peut être autonome est généralement un jugement, mais il existe quelques tests simples que vous pouvez utiliser. Demandez-vous si vous avez supprimé tout le contexte environnant, ce contenu aurait-il toujours un sens? De même pour le texte, le contenu tiendrait-il s'il était dans un flux RSS?
N'oubliez pas que les personnes utilisant des technologies d'assistance s'appuient sur un balisage organisé et sémantiquement significatif pour mieux comprendre votre travail.
<strong>Note d'à propos <code>section</code> et <code>div</code></strong><br>The <code>section</code> L'élément est également nouveau avec HTML5 et a une signification sémantique légèrement différente de <code>article</code>. Un <code>article</code> est pour le contenu autonome, et un <code>section</code> sert à regrouper des contenus thématiques. Ils peuvent être utilisés les uns dans les autres, selon les besoins. Par exemple, si un livre est le <code>article</code>, alors chaque chapitre est un <code>section</code>. Lorsqu'il n'y a pas de relation entre les groupes de contenu, utilisez un <code>div</code>.

```html
<div> - contenu des groupes
<section> - groupes de contenu connexe
<article> - regroupe des contenus indépendants et autonomes
```

</section>

## Instructions
<section id='instructions'>
Camper Cat d'occasion <code>article</code> balises pour envelopper les messages sur sa page de blog, mais il a oublié de les utiliser autour de celui du haut. Changer la <code>div</code> tag pour utiliser un <code>article</code> tag instead.
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: Your code should have three <code>article</code> tags.
    testString: assert($('article').length == 3);
  - text: Your code should not have any <code>div</code> tags.
    testString: assert($('div').length == 0);

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='html-seed'>

```html
<h1>Réflexions profondes avec Master Camper Cat</h1>
<main>
  <div>
    <h2>Les fichiers Garfield: la lasagne comme carburant d'entraînement?</h2>
    <p>Internet regorge d'opinions différentes sur les paradigmes nutritionnels, de la paléo de l'herbe à chat aux nettoyages des boules de poils. Mais tournons notre attention vers un carburant de fitness souvent négligé, et examinons le trifecta protéine-carb-NOM qu'est la lasagne ...</p>
  </div>

  <img src="samuraiSwords.jpeg" alt="">

  <article>
    <h2>Vaincre votre ennemi: le point rouge est à nous!</h2>
    <p>Les félins du monde entier ont fait la guerre aux ennemis les plus persistants. Ce Némésis rouge combine à la fois une furtivité rusée et une vitesse d'éclair. Mais bon sang, chers combattants, notre heure de victoire pourrait bientôt approcher ... </p>
  </article>

  <img src="samuraiSwords.jpeg" alt="">

  <article>
    <h2>Chuck Norris est-il un chat?</h2>
    <p>Chuck Norris est largement considéré comme le premier artiste martial de la planète, et c'est une coïncidence complète quiconque en désaccord avec ce fait disparaît mystérieusement peu de temps après. Mais la vraie question est, est-il un chat? ...</p>
  </article>
</main>
```

</div>



</section>

## Solution
<section id='solution'>

```html
<h1>Réflexions profondes avec Master Camper Cat</h1>
<main>
  <article>
    <h2>Les fichiers Garfield: la lasagne comme carburant d'entraînement?</h2>
    <p>Internet regorge d'opinions différentes sur les paradigmes nutritionnels, de la paléo de l'herbe à chat aux nettoyages des boules de poils. Mais tournons notre attention vers un carburant de fitness souvent négligé, et examinons le trifecta protéine-carb-NOM qu'est la lasagne ...</p>
  </article>

  <img src="samuraiSwords.jpeg" alt="">

  <article>
    <h2>Vaincre votre ennemi: le point rouge est à nous!</h2>
    <p>Les félins du monde entier ont fait la guerre aux ennemis les plus persistants. Ce Némésis rouge combine à la fois une furtivité rusée et une vitesse d'éclair. Mais bon sang, chers combattants, notre heure de victoire pourrait bientôt approcher ...</p>
  </article>

  <img src="samuraiSwords.jpeg" alt="">

  <article>
    <h2>Chuck Norris est-il un chat?</h2>
    <p>Chuck Norris est largement considéré comme le premier artiste martial de la planète, et c'est une coïncidence complète quiconque en désaccord avec ce fait disparaît mystérieusement peu de temps après. Mais la vraie question est, est-il un chat? ...</p>
  </article>
</main>
```

</section>
