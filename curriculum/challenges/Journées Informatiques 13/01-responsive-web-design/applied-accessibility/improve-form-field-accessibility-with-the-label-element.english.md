---
id: 587d778a367417b2b2512aa6
title: Improve Form Field Accessibility with the label Element
challengeType: 0
videoUrl: 'https://scrimba.com/c/cGJMMAN'
forumTopicId: 301016
---

## Description
<section id='description'>
L'amélioration de l'accessibilité avec le balisage HTML sémantique s'applique à l'utilisation à la fois des noms de balise appropriés et des attributs. Les prochains défis couvrent certains scénarios importants utilisant des attributs dans les formulaires.
Le <code>label</code> balise le texte d'un élément de contrôle de formulaire spécifique, généralement le nom ou l'étiquette d'un choix. Cela lie le sens à l'élément et rend le formulaire plus lisible. le <code>for</code> attribut sur un <code>label</code> tag associe explicitement <code>label</code> avec le contrôle de formulaire et est utilisé par les lecteurs d'écran.
Vous avez découvert les boutons radio et leurs étiquettes dans une leçon de la section HTML de base. Dans cette leçon, nous avons enveloppé l'élément d'entrée du bouton radio dans un<code>label</code> avec le texte de l'étiquette afin de rendre le texte cliquable. Une autre façon d'y parvenir est d'utiliser le <code>for</code> comme expliqué dans cette leçon.
La valeur du <code>for</code> L'attribut doit être identique à la valeur de l'attribut <code>id</code> attribut du contrôle de formulaire. Voici un exemple:

```html
<form>
  <label for="name">Nom:</label>
  <input type="text" id="name" name="name">
</form>
```

</section>

## Instructions
<section id='instructions'>
Camper Cat attend beaucoup d'intérêt pour ses articles de blog réfléchis et souhaite inclure un formulaire d'inscription par e-mail. Ajouter un <code>for</code> attribut sur l'e-mail <code>label</code> qui correspond à la <code>id</code> sur son <code>input</code> champ.
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: Your code should have a <code>for</code> attribute on the <code>label</code> tag that is not empty.
    testString: assert($('label').attr('for'));
  - text: Your <code>for</code> attribute value should match the <code>id</code> value on the email <code>input</code>.
    testString: assert($('label').attr('for') == 'email');

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
  <section>
    <form>
      <p>Inscrivez-vous pour recevoir les articles du blog de Camper Cat par e-mail ici!</p>


      <label>Email:</label>
      <input type="text" id="email" name="email">


      <input type="submit" name="submit" value="Submit">
    </form>
  </section>
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
  <section>
    <form>
      <p>Inscrivez-vous pour recevoir les articles du blog de Camper Cat par e-mail ici!</p>


      <label for="email">Email:</label>
      <input type="text" id="email" name="email">


      <input type="submit" name="submit" value="Submit">
    </form>
  </section>
  <article>
    <h2>Les fichiers Garfield: la lasagne comme carburant d'entraînement?</h2>
    <p>Internet regorge d'opinions différentes sur les paradigmes nutritionnels, de la paléo de l'herbe à chat aux nettoyages des boules de poils. Mais tournons notre attention vers un carburant de fitness souvent négligé et examinons le trifecta protéine-carb-NOM qu'est la lasagne..</p>
  </article>
  <img src="samuraiSwords.jpeg" alt="">
  <article>
    <h2>Vaincre votre ennemi: le point rouge est à nous!</h2>
    <p>Les félins du monde entier ont fait la guerre aux ennemis les plus persistants. Ce Némésis rouge combine à la fois une furtivité rusée et une vitesse d'éclair. Mais bon sang, camarades combattants, notre heure de victoire pourrait bientôt approcher..</p>
  </article>
  <img src="samuraiSwords.jpeg" alt="">
  <article>
    <h2>Chuck Norris est-il un chat?</h2>
    <p>Chuck Norris est largement considéré comme le premier artiste martial de la planète, et c'est une coïncidence complète quiconque en désaccord avec ce fait disparaît mystérieusement peu de temps après. Mais la vraie question est, est-il un chat? ...</p>
  </article>
  <footer>&copy; 2018 Camper Cat</footer>
</body>
```

</section>
