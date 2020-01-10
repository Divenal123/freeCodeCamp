---
id: 587d774c367417b2b2512a9d
title: Know When Alt Text Should be Left Blank
challengeType: 0
videoUrl: 'https://scrimba.com/c/cM9P4t2'
forumTopicId: 301019
---

## Description
<section id='description'>
Dans le dernier défi, vous avez appris qu’inclure un <code>alt</code> attribut lors de l'utilisation <code>img</code> les balises sont obligatoires. Cependant, parfois les images sont regroupées avec une légende les décrivant déjà, ou sont utilisées uniquement pour la décoration. Dans ces cas <code>alt</code> le texte peut sembler redondant ou inutile.
Dans les situations où une image est déjà expliquée avec du contenu textuel ou n'ajoute pas de sens à une page, le <code>img</code> a encore besoin d'un <code>alt</code> , mais il peut être défini sur une chaîne vide. Voici un exemple:
<code>&lt;img src=&quot;visualDecoration.jpeg&quot; alt=&quot;&quot;&gt;</code>
Les images d'arrière-plan relèvent généralement également de l'étiquette «décorative». Cependant, ils sont généralement appliqués avec des règles CSS et ne font donc pas partie du processus des lecteurs d'écran de balisage.
<strong>Note:</strong> Pour les images avec une légende, vous pouvez toujours vouloir inclure <code>alt</code> texte, car il aide les moteurs de recherche à cataloguer le contenu de l'image.
</section>

## Instructions
<section id='instructions'>
Camper Cat a codé une page squelette pour la partie blog de son site Web. Il prévoit d'ajouter une pause visuelle entre ses deux articles avec une image décorative d'une épée de samouraï. Ajouter un <code>alt</code> attribuer au <code>img</code> et définissez-le sur une chaîne vide. (Notez que l'image <code>src</code> ne lie pas à un fichier réel - ne vous inquiétez pas qu'aucune épée ne s'affiche à l'écran.)
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: Your <code>img</code> tag should have an <code>alt</code> attribute.
    testString: assert(!($('img').attr('alt') == undefined));
  - text: The <code>alt</code> attribute should be set to an empty string.
    testString: assert($('img').attr('alt') == '');

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='html-seed'>

```html
<h1>Réflexions profondes avec Master Camper Cat</h1>
<article>
  <h2>Vaincre votre ennemi: le point rouge est à nous!</h2>
  <p>Venir...</p>
</article>

<img src="samuraiSwords.jpeg">

<article>
  <h2>Chuck Norris est-il un chat?</h2>
  <p>Venir...</p>
</article>
```

</div>



</section>

## Solution
<section id='solution'>

```html
<h1>Réflexions profondes avec Master Camper Cat</h1>
<article>
  <h2>Vaincre votre ennemi: le point rouge est à nous!</h2>
  <p>Venir...</p>
</article>

<img src="samuraiSwords.jpeg" alt="">

<article>
  <h2>Chuck Norris est-il un chat?</h2>
  <p>Venir</p>
</article>
```

</section>
