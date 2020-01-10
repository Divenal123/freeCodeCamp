---
id: 587d774c367417b2b2512a9c
title: Add a Text Alternative to Images for Visually Impaired Accessibility
challengeType: 0
videoUrl: 'https://scrimba.com/c/cPp7VfD'
forumTopicId: 16628
---

## Description
<section id='description'>
Il est probable que vous ayez vu un <code>alt</code> attribut sur un <code>img</code> tag dans d'autres défis. <code>Alt</code> le texte décrit le contenu de l'image et lui fournit une alternative textuelle. Cela aide dans les cas où l'image ne se charge pas ou ne peut pas être vue par un utilisateur. Il est également utilisé par les moteurs de recherche pour comprendre ce qu'une image contient pour l'inclure dans les résultats de recherche. Voici un exemple:
<code>&lt;img src=&quot;importantLogo.jpeg&quot; alt=&quot;Company logo&quot;&gt;</code>
Les personnes ayant une déficience visuelle comptent sur les lecteurs d'écran pour convertir le contenu Web en une interface audio. Ils n'obtiendront pas d'informations si elles ne sont présentées que visuellement. Pour les images, les lecteurs d'écran peuvent accéder au <code>alt</code> attribuer et lire son contenu pour fournir des informations clés.
Bien <code>alt</code> le texte fournit au lecteur une brève description de l'image. Vous devez toujours inclure un <code>alt</code> attribut sur votre image. Selon la spécification HTML5, cela est désormais considéré comme obligatoire.
</section>

## Instructions
<section id='instructions'>

Camper Cat se trouve être à la fois un ninja codeur et un vrai ninja, qui construit un site Web pour partager ses connaissances. La photo de profil qu'il souhaite utiliser montre ses compétences et doit être appréciée par tous les visiteurs du site. Ajouter un <code>alt</code> attribut dans le <code>img</code> tag, ce qui explique que Camper Cat fait du karaté. (L'image <code>src</code> ne lie pas à un fichier réel, vous devriez donc voir le <code>alt</code> texte à l'écran.)

</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: Your <code>img</code> tag should have an <code>alt</code> attribute and it should not be empty.
    testString: assert($('img').attr('alt'));

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='html-seed'>

```html
<img src="doingKarateWow.jpeg">
```

</div>



</section>

## Solution
<section id='solution'>

```html
<img src="doingKarateWow.jpeg" alt="Someone doing karate">
```

</section>
