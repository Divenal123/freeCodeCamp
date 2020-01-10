---
id: 587d778f367417b2b2512aac
title: Avoid Colorblindness Issues by Using Sufficient Contrast
challengeType: 0
videoUrl: 'https://scrimba.com/c/cmzMEUw'
forumTopicId: 301012
---

## Description
<section id='description'>
La couleur est une grande partie de la conception visuelle, mais son utilisation introduit deux problèmes d'accessibilité. Premièrement, la couleur seule ne doit pas être utilisée comme le seul moyen de transmettre des informations importantes car les utilisateurs de lecteurs d'écran ne les verront pas. Deuxièmement, les couleurs de premier plan et d'arrière-plan nécessitent un contraste suffisant pour que les utilisateurs daltoniens puissent les distinguer.
Les défis précédents portaient sur le fait d'avoir des alternatives de texte pour résoudre le premier problème. Le dernier défi a introduit des outils de vérification du contraste pour aider avec le second. Le rapport de contraste recommandé par les WCAG de 4,5: 1 s'applique à l'utilisation des couleurs ainsi qu'aux combinaisons de niveaux de gris.
Les utilisateurs daltoniens ont du mal à distinguer certaines couleurs des autres - généralement en teinte mais parfois aussi en légèreté. Vous vous souvenez peut-être que le rapport de contraste est calculé en utilisant les valeurs de luminance relative (ou de luminosité) des couleurs de premier plan et d'arrière-plan.
En pratique, le rapport de contraste de 4,5: 1 peut être atteint en ombrant (ajoutant du noir à) la couleur plus foncée et en teintant (ajoutant du blanc à) la couleur plus claire. Les nuances plus sombres sur la roue chromatique sont considérées comme des nuances de bleus, violettes, magentas et rouges, tandis que les couleurs plus claires sont les oranges, les jaunes, les verts et les bleu-verts.
</section>

## Instructions
<section id='instructions'>
Camper Cat expérimente l'utilisation de la couleur pour le texte et l'arrière-plan de son blog, mais sa combinaison actuelle d'un verdâtre <code>background-color</code> avec texte marron <code>color</code> a un rapport de contraste de 2,5: 1. Vous pouvez facilement ajuster la luminosité des couleurs puisqu'il les a déclarées en utilisant le CSS <code>hsl()</code> (qui signifie teinte, saturation, luminosité) en changeant le troisième argument. Augmenter le <code>background-color</code> valeur de légèreté de 35% à 55%, et diminuer la<code>couleur</code> valeur de légèreté de 20% à 15%. Cela améliore le contraste à 5,9: 1.
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: Your code should only change the lightness value for the text <code>color</code> property to a value of 15%.
    testString: assert(code.match(/color:\s*?hsl\(0,\s*?55%,\s*?15%\)/gi));
  - text: Your code should only change the lightness value for the <code>background-color</code> property to a value of 55%.
    testString: assert(code.match(/background-color:\s*?hsl\(120,\s*?25%,\s*?55%\)/gi));

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='html-seed'>

```html
<head>
  <style>
  body {
    color: hsl(0, 55%, 20%);
    background-color: hsl(120, 25%, 35%);
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

</div>



</section>

## Solution
<section id='solution'>


```html
<head>
  <style>
  body {
    color: hsl(0, 55%, 15%);
    background-color: hsl(120, 25%, 55%);
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
