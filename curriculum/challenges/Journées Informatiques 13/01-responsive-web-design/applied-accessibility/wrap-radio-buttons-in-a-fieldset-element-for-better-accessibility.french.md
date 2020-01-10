---
id: 587d778b367417b2b2512aa7
title: Wrap Radio Buttons in a fieldset Element for Better Accessibility
challengeType: 0
videoUrl: 'https://scrimba.com/c/cVJVefw'
forumTopicId: 301030
---

## Description
<section id='description'>
La rubrique suivante du formulaire couvre l'accessibilité des boutons radio. Chaque choix reçoit un<code>label</code> avec un <code>for</code> attribut lié à l '<code> id </code> de l'élément correspondant tel que couvert dans le dernier défi. Étant donné que les boutons radio viennent souvent dans un groupe où l'utilisateur doit en choisir un, il existe un moyen de montrer sémantiquement que les choix font partie d'un ensemble.
Le <code>fieldset</code> balise entoure l'ensemble du groupe de boutons radio pour y parvenir. Il utilise souvent un <code>legend</code> pour fournir une description du regroupement, qui est lue par les lecteurs d'écran pour chaque choix <code>fieldset</code> element.
Le <code>fieldset</code> emballage et <code>legend</code> tag ne sont pas nécessaires lorsque les choix sont explicites, comme une sélection de sexe. Utilisant un <code>label</code> avec le <code>for</code> attribut pour chaque bouton radio est suffisant.
Voici un exemple:

```html
<form>
  <fieldset>
    <legend>Choisissez l'un de ces trois éléments:</legend>
    <input id="one" type="radio" name="items" value="one">
    <label for="one">Choix Un</label><br>
    <input id="two" type="radio" name="items" value="two">
    <label for="two">Choix Deux</label><br>
    <input id="three" type="radio" name="items" value="three">
    <label for="three">Choix Trois</label>
  </fieldset>
</form>
```

</section>

## Instructions
<section id='instructions'>
Camper Cat veut des informations sur le niveau ninja de ses utilisateurs lorsqu'ils s'inscrivent à sa liste de diffusion. Il a ajouté un ensemble de boutons radio et a appris de notre dernière leçon à utiliser des étiquettes d'étiquette avec <code>for</code> attributs pour chaque choix. Allez Camper Cat! Cependant, son code a encore besoin d'aide. Changer la<code>div</code> balise entourant les boutons radio à un <code>fieldset</code> et modifiez le <code>p</code> marquer à l'intérieur d'un<code>legend</code>.
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: Your code should have a <code>fieldset</code> tag around the radio button set.
    testString: assert($('fieldset').length == 1);
  - text: The <code>fieldset</code> element should have a closing tag.
    testString: assert(code.match(/<\/fieldset>/g) && code.match(/<\/fieldset>/g).length === code.match(/<fieldset>/g).length);
  - text: Your code should have a <code>legend</code> tag around the text asking what level ninja a user is.
    testString: assert($('legend').length == 1);
  - text: Your code should not have any <code>div</code> tags.
    testString: assert($('div').length == 0);
  - text: Your code should no longer have a <code>p</code> tag around the text asking what level ninja a user is.
    testString: assert($('p').length == 4);

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
      <label for="email">Email:</label>
      <input type="text" id="email" name="email">


      <!-- Add your code below this line -->
      <div>
        <p>De quel niveau ninja es-tu?</p>
        <input id="newbie" type="radio" name="levels" value="newbie">
        <label for="newbie">Newbie Kitten</label><br>
        <input id="intermediate" type="radio" name="levels" value="intermediate">
        <label for="intermediate">Étudiant en développement</label><br>
        <input id="master" type="radio" name="levels" value="master">
        <label for="master">Maître</label>
      </div>
      <!-- Add your code above this line -->


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
    <h1>Deep Thoughts with Master Camper Cat</h1>
  </header>
  <section>
    <form>
      <p>Sign up to receive Camper Cat's blog posts by email here!</p>
      <label for="email">Email:</label>
      <input type="text" id="email" name="email">


      <!-- Add your code below this line -->
      <fieldset>
        <legend>What level ninja are you?</legend>
        <input id="newbie" type="radio" name="levels" value="newbie">
        <label for="newbie">Newbie Kitten</label><br>
        <input id="intermediate" type="radio" name="levels" value="intermediate">
        <label for="intermediate">Developing Student</label><br>
        <input id="master" type="radio" name="levels" value="master">
        <label for="master">Master</label>
      </fieldset>
      <!-- Add your code above this line -->


      <input type="submit" name="submit" value="Submit">
    </form>
  </section>
  <article>
    <h2>The Garfield Files: Lasagna as Training Fuel?</h2>
    <p>The internet is littered with varying opinions on nutritional paradigms, from catnip paleo to hairball cleanses. But let's turn our attention to an often overlooked fitness fuel, and examine the protein-carb-NOM trifecta that is lasagna...</p>
  </article>
  <img src="samuraiSwords.jpeg" alt="">
  <article>
    <h2>Defeating your Foe: the Red Dot is Ours!</h2>
    <p>Felines the world over have been waging war on the most persistent of foes. This red nemesis combines both cunning stealth and lightening speed. But chin up, fellow fighters, our time for victory may soon be near...</p>
  </article>
  <img src="samuraiSwords.jpeg" alt="">
  <article>
    <h2>Is Chuck Norris a Cat Person?</h2>
    <p>Chuck Norris is widely regarded as the premier martial artist on the planet, and it's a complete coincidence anyone who disagrees with this fact mysteriously disappears soon after. But the real question is, is he a cat person?...</p>
  </article>
  <footer>&copy; 2018 Camper Cat</footer>
</body>
```

</section>
