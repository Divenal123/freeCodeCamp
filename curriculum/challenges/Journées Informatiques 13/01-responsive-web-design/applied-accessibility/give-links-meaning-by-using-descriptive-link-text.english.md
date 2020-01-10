---
id: 587d778f367417b2b2512aae
title: Give Links Meaning by Using Descriptive Link Text
challengeType: 0
videoUrl: 'https://scrimba.com/c/c437DcV'
forumTopicId: 301013
---

## Description
<section id='description'>
Les utilisateurs de lecteurs d'écran ont différentes options pour le type de contenu que leur appareil lit. Cela inclut le saut vers (ou sur) des éléments de repère, le saut vers le contenu principal ou l'obtention d'un résumé de page à partir des titres. Une autre option consiste à n'entendre que les liens disponibles sur une page.
Les lecteurs d'écran le font en lisant le texte du lien ou ce qu'il y a entre l'ancre (<code>a</code>) Mots clés. Il n'est pas utile d'avoir une liste de liens "cliquez ici" ou "en savoir plus". Au lieu de cela, vous devez utiliser un texte bref mais descriptif dans le <code>a</code> tags pour donner plus de sens à ces utilisateurs.
</section>

## Instructions
<section id='instructions'>
Le texte du lien que Camper Cat utilise n'est pas très descriptif sans le contexte environnant. Déplacez l'ancre (<code>a</code>) des balises pour envelopper le texte "informations sur les batteries" au lieu de "Cliquez ici".
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: Your code should move the anchor <code>a</code> tags from around the words "Click here" to wrap around the words "information about batteries".
    testString: assert($('a').text().match(/^(information about batteries)$/g));
  - text: The <code>a</code> element should have an <code>href</code> attribute with a value of an empty string <code>""</code>.
    testString: assert($('a').attr('href') === '');
  - text: The <code>a</code> element should have a closing tag.
    testString: assert(code.match(/<\/a>/g) && code.match(/<\/a>/g).length === code.match(/<a href=(''|"")>/g).length);

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
    <h2>Vaincre votre ennemi: le point rouge est à nous!</h2>
    <p>Les félins du monde entier ont fait la guerre aux ennemis les plus persistants. Ce Némésis rouge combine à la fois une furtivité rusée et une vitesse d'éclair. Mais bon sang, chers combattants, notre heure de victoire pourrait bientôt approcher. <a href="">Click here</a> pour plus d'informations sur les batteries</p>
  </article>
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
    <h2>Vaincre votre ennemi: le point rouge est à nous!</h2>
    <p>Les félins du monde entier ont fait la guerre aux ennemis les plus persistants. Ce Némésis rouge combine à la fois une furtivité rusée et une vitesse d'éclair. Mais bon sang, chers combattants, notre heure de victoire pourrait bientôt approcher. Cliquez ici pour <a href="">informations sur les batteries</a></p>
  </article>
</body>
```

</section>
