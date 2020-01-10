---
id: 587d778b367417b2b2512aa8
title: Add an Accessible Date Picker
challengeType: 0
videoUrl: 'https://scrimba.com/c/cR3bRbCV'
forumTopicId: 301008
---

## Description
<section id='description'>
Les formulaires incluent souvent <code>input</code> , qui peut être utilisé pour créer plusieurs contrôles de formulaire différents. L'attribut <code> type </code> de cet élément indique le type d'entrée qui sera créé.
Vous avez peut-être remarqué <code>text</code> et <code>submit</code> types d'entrée dans les défis précédents, et HTML5 a introduit une option pour spécifier un <code>date</code> champ. Selon la prise en charge du navigateur, un sélecteur de date apparaît dans le <code>input</code> fquand il est au point, ce qui facilite le remplissage d'un formulaire pour tous les utilisateurs.
Pour les navigateurs plus anciens, le type sera par défaut<code>text</code>, il est donc utile de montrer aux utilisateurs le format de date attendu dans l'étiquette ou en tant que texte d'espace réservé au cas où.
Voici un exemple:

```html
<label for="input1">Enter a date:</label>
<input type="date" id="input1" name="input1">
```

</section>

## Instructions
<section id='instructions'>
Camper Cat organise un tournoi Mortal Kombat et veut demander à ses concurrents de voir quelle date fonctionne le mieux. Ajouter un <code>input</code> tag avec un <code>type</code> attribut de "date", un <code>id</code> attribut "pickdate" et un <code>name</code> attribut de "date".
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: Your code should add one <code>input</code> tag for the date selector field.
    testString: assert($('input').length == 2);
  - text: Your <code>input</code> tag should have a <code>type</code> attribute with a value of date.
    testString: assert($('input').attr('type') == 'date');
  - text: Your <code>input</code> tag should have an <code>id</code> attribute with a value of pickdate.
    testString: assert($('input').attr('id') == 'pickdate');
  - text: Your <code>input</code> tag should have a <code>name</code> attribute with a value of date.
    testString: assert($('input').attr('name') == 'date');

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='html-seed'>

```html
<body>
  <header>
    <h1>Tournois</h1>
  </header>
  <main>
    <section>
      <h2>Enquête sur le tournoi Mortal Kombat</h2>
      <form>
        <p>Dites-nous la meilleure date pour le concours</p>
        <label for="pickdate">Date de préférence:</label>

        <!-- Add your code below this line -->



        <!-- Add your code above this line -->

        <input type="submit" name="submit" value="Submit">
      </form>
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
    <h1>Tournois</h1>
  </header>
  <main>
    <section>
      <h2>Enquête sur le tournoi Mortal Kombat</h2>
      <form>
        <p>Dites-nous la meilleure date pour le concours</p>
        <label for="pickdate">Date de préférence:</label>
        <input type="date" id="pickdate" name="date">
        <input type="submit" name="submit" value="Submit">
      </form>
    </section>
  </main>
  <footer>&copy; 2018 Camper Cat</footer>
</body>
```

</section>
