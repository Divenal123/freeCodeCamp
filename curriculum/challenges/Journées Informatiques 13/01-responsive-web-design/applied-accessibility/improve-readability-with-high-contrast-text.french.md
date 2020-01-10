---
id: 587d778e367417b2b2512aab
title: Improve Readability with High Contrast Text
challengeType: 0
videoUrl: 'https://scrimba.com/c/cKb3nCq'
forumTopicId: 301017
---

## Description
<section id='description'>
Un faible contraste entre les couleurs de premier plan et d'arrière-plan peut rendre la lecture du texte difficile. Un contraste suffisant améliore la lisibilité de votre contenu, mais que signifie exactement "suffisant"?
Les directives d'accessibilité du contenu Web (WCAG) recommandent au moins un rapport de contraste de 4,5 à 1 pour le texte normal. Le rapport est calculé en comparant les valeurs de luminance relative de deux couleurs. Cela va de 1: 1 pour la même couleur, ou pas de contraste, à 21: 1 pour le blanc contre le noir, le contraste le plus fort. Il existe de nombreux outils de vérification du contraste disponibles en ligne qui calculent ce ratio pour vous.
</section>

## Instructions
<section id='instructions'>
Le choix de texte gris clair de Camper Cat sur fond blanc pour son récent article de blog a un rapport de contraste de 1,5: 1, ce qui le rend difficile à lire. Changer la<code>color</code> du texte du gris actuel (<code>#D3D3D3</code>) à un gris plus foncé (<code>#636363</code>) pour améliorer le rapport de contraste à 6: 1.
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: Your code should change the text <code>color</code> for the <code>body</code> to the darker gray.
    testString: assert($('body').css('color') == 'rgb(99, 99, 99)');
  - text: Your code should not change the <code>background-color</code> for the <code>body</code>.
    testString: assert($('body').css('background-color') == 'rgb(255, 255, 255)');

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='html-seed'>

```html
<head>
  <style>
  body {
    color: #D3D3D3;
    background-color: #FFF;
  }
  </style>
</head>
<body>
  <header>
    <h1>Réflexions profondes avec Master Camper Cat</h1>
  </header>
  <article>
    <h2>Réflexions profondes avec Master Camper Cat</h2>
    <p>L'influence de l'herbe à chat sur le comportement des félins est bien documentée et son utilisation comme complément à base de plantes dans les cercles de ninja compétitifs reste controversée. Une fois de plus, le débat sur l'interdiction de la substance est porté à l'attention du public après la victoire de haut niveau de Kittytron, un partisan de longue date et utilisateur de la substance verte, lors du tournoi Claw of Fury.</p>
    <p>Comme je l'ai dit dans le passé, je crois fermement que les véritables compétences d'un ninja doivent venir de l'intérieur, sans influences externes. Ma propre utilisation de cataire continuera comme purement récréative.</p>
  </article>
</body>
```

</div>



</section>

## Solution
<section id='solution'>

```html
<head>
  <style>
  body {
    color: #636363;
    background-color: #FFF;
  }
  </style>
</head>
<body>
  <header>
    <h1>Réflexions profondes avec Master Camper Cat</h1>
  </header>
  <article>
    <h2>Un mot sur le récent scandale du dopage de l'herbe à chat</h2>
    <p>L'influence de l'herbe à chat sur le comportement des félins est bien documentée et son utilisation comme complément à base de plantes dans les cercles de ninja compétitifs reste controversée. Une fois de plus, le débat sur l'interdiction de la substance est porté à l'attention du public après la victoire de haut niveau de Kittytron, un partisan de longue date et utilisateur de la substance verte, lors du tournoi Claw of Fury.</p>
    <p>Comme je l'ai dit dans le passé, je crois fermement que les véritables compétences d'un ninja doivent venir de l'intérieur, sans influences externes. Ma propre utilisation de cataire continuera comme purement récréative.</p>
  </article>
</body>
```

</section>
