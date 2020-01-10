---
id: 587d7790367417b2b2512ab0
title: Use tabindex to Add Keyboard Focus to an Element
challengeType: 0
videoUrl: 'https://scrimba.com/c/cmzMDHW'
forumTopicId: 301027
---

## Description
<section id='description'>
Le HTML <code>tabindex</code> L'attribut a trois fonctions distinctes liées au focus clavier d'un élément. Lorsqu'il est sur une balise, cela indique que l'élément peut être focalisé. La valeur (un entier positif, négatif ou nul) détermine le comportement.
Certains éléments, tels que les liens et les contrôles de formulaire, reçoivent automatiquement le focus du clavier lorsqu'un utilisateur parcourt une page. C'est dans le même ordre que les éléments viennent dans le balisage source HTML. Cette même fonctionnalité peut être donnée à d'autres éléments, tels que comme <code>div</code>, <code>span</code>, et <code>p</code>, en plaçant a <code>tabindex="0"</code> attribuer sur eux. Voici un exemple:
<code>&lt;div tabindex=&quot;0&quot;&gt;J'ai besoin de me concentrer sur le clavier!&lt;/div&gt;</code>
<strong>Note:</strong> Un négatif <code>tabindex</code> value (typically -1) indique qu'un élément est focalisable, mais n'est pas accessible par le clavier. Cette méthode est généralement utilisée pour mettre l'accent sur le contenu par programme (comme lorsqu'un <code>div</code> utilisé pour une fenêtre pop-up est activé), et dépasse la portée de ces défis.
</section>

## Instructions
<section id='instructions'>
Camper Cat a créé une nouvelle enquête pour collecter des informations sur ses utilisateurs. Il sait que les champs de saisie obtiennent automatiquement la mise au point du clavier, mais il veut s'assurer que ses utilisateurs du clavier s'arrêtent sur les instructions tout en parcourant les éléments. Ajouter un <code>tabindex</code> attribuer au <code>p</code> et définissez sa valeur sur "0". Bonus - utilisation <code>tabindex</code> active également la pseudo-classe CSS <code>:focus</code> travailler sur le <code>p</code> tag.
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: Your code should add a <code>tabindex</code> attribute to the <code>p</code> tag that holds the form instructions.
    testString: assert($('p').attr('tabindex'));
  - text: Your code should set the <code>tabindex</code> attribute on the <code>p</code> tag to a value of 0.
    testString: assert($('p').attr('tabindex') == '0');

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='html-seed'>

```html
<head>
  <style>
  p:focus {
    background-color: yellow;
  }
  </style>
</head>
<body>
  <header>
    <h1>Ninja Survey</h1>
  </header>
  <section>
    <form>


      <p>Instructions: Remplissez TOUTES vos informations puis cliquez sur <b>Submit</b></p>


      <label for="username">Nom de l'utilisateur:</label>
      <input type="text" id="username" name="username"><br>
      <fieldset>
        <legend>De quel niveau ninja es-tu?</legend>
        <input id="newbie" type="radio" name="levels" value="newbie">
        <label for="newbie">Newbie Kitten</label><br>
        <input id="intermediate" type="radio" name="levels" value="intermediate">
        <label for="intermediate">Étudiant en développement</label><br>
        <input id="master" type="radio" name="levels" value="master">
        <label for="master">9th Life Master</label>
      </fieldset>
      <br>
      <fieldset>
      <legend>Sélectionnez vos armes préférées:</legend>
      <input id="stars" type="checkbox" name="weapons" value="stars">
      <label for="stars">Lancer des étoiles</label><br>
      <input id="nunchucks" type="checkbox" name="weapons" value="nunchucks">
      <label for="nunchucks">Nunchucks</label><br>
      <input id="sai" type="checkbox" name="weapons" value="sai">
      <label for="sai">Sai Set</label><br>
      <input id="sword" type="checkbox" name="weapons" value="sword">
      <label for="sword">Sword</label>
      </fieldset>
      <br>
      <input type="submit" name="submit" value="Submit">
    </form><br>
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
  p:focus {
    background-color: yellow;
  }
  </style>
</head>
<body>
  <header>
    <h1>Ninja Survey</h1>
  </header>
  <section>
    <form>


      <p tabindex="0">Instructions: Remplissez TOUTES vos informations puis cliquez sur <b>Submit</b></p>


      <label for="username">Nom de l'utilisateur:</label>
      <input type="text" id="username" name="username"><br>
      <fieldset>
        <legend>De quel niveau ninja es-tu?</legend>
        <input id="newbie" type="radio" name="levels" value="newbie">
        <label for="newbie">Newbie Kitten</label><br>
        <input id="intermediate" type="radio" name="levels" value="intermediate">
        <label for="intermediate">Étudiant en développement</label><br>
        <input id="master" type="radio" name="levels" value="master">
        <label for="master">9th Life Master</label>
      </fieldset>
      <br>
      <fieldset>
      <legend>Sélectionnez vos armes préférées:</legend>
      <input id="stars" type="checkbox" name="weapons" value="stars">
      <label for="stars">Lancer des étoiles</label><br>
      <input id="nunchucks" type="checkbox" name="weapons" value="nunchucks">
      <label for="nunchucks">Nunchucks</label><br>
      <input id="sai" type="checkbox" name="weapons" value="sai">
      <label for="sai">Sai Set</label><br>
      <input id="sword" type="checkbox" name="weapons" value="sword">
      <label for="sword">Sword</label>
      </fieldset>
      <br>
      <input type="submit" name="submit" value="Submit">
    </form><br>
  </section>
  <footer>&copy; 2018 Camper Cat</footer>
</body>
```

</section>
