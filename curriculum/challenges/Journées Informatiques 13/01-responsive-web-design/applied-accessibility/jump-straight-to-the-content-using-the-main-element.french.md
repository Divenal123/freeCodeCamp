---
id: 587d774e367417b2b2512a9f
title: Jump Straight to the Content Using the main Element
challengeType: 0
videoUrl: 'https://scrimba.com/c/cPp7zuE'
forumTopicId: 301018
---

## Description
<section id='description'>
HTML5 a introduit un certain nombre de nouveaux éléments qui offrent aux développeurs plus d'options tout en incorporant également des fonctionnalités d'accessibilité. Ces balises incluent <code>main</code>, <code>header</code>, <code>footer</code>, <code>nav</code>, <code>article</code>, and <code>section</code>, entre autres.
Par défaut, un navigateur rend ces éléments de la même manière que l'humble <code>div</code>. Cependant, leur utilisation le cas échéant donne un sens supplémentaire à votre balisage. Le nom de la balise à lui seul peut indiquer le type d'informations qu'il contient, ce qui ajoute une signification sémantique à ce contenu. Les technologies d'assistance peuvent accéder à ces informations pour fournir un meilleur résumé de page ou de meilleures options de navigation à leurs utilisateurs.
Le <code>principal</code> L'élément est utilisé pour envelopper (vous l'avez deviné) le contenu principal, et il ne devrait y en avoir qu'un par page. Il est destiné à entourer les informations liées au sujet central de votre page. Il n'est pas destiné à inclure des éléments qui se répètent sur plusieurs pages, comme des liens de navigation ou des bannières.
Le <code>principal</code> La balise a également une fonction de point de repère intégrée que la technologie d'assistance peut utiliser pour naviguer rapidement vers le contenu principal. Si vous avez déjà vu un lien "Aller au contenu principal" en haut d'une page, l'utilisation d'une balise principale donne automatiquement cette fonctionnalité aux appareils et accessoires fonctionnels.
</section>

## Instructions
<section id='instructions'>
Camper Cat a de grandes idées pour sa page d'armes ninja. Aidez-le à configurer son balisage en ajoutant l'ouverture et la fermeture <code>principale</code> des balises entre les <code>header</code> et <code>footer</code> (couvert par d'autres défis). Garder les <code>principales</code> balises vides pour l'instant.
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: Your code should have one <code>main</code> tag.
    testString: assert($('main').length == 1);
  - text: The <code>main</code> tags should be between the closing <code>header</code> tag and the opening <code>footer</code> tag.
    testString: assert(code.match(/<\/header>\s*?<main>\s*?<\/main>/gi));

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='html-seed'>

```html
<header>
  <h1>Les armes de Ninja</h1>
</header>



<footer></footer>
```

</div>



</section>

## Solution
<section id='solution'>

```html
<header>
  <h1>Les armes de Ninja</h1>
</header>
<main>

</main>
<footer></footer>
```

</section>
