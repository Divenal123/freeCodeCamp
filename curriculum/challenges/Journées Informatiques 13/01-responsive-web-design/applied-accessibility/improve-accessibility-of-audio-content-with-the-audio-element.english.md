---
id: 587d7789367417b2b2512aa4
title: Improve Accessibility of Audio Content with the audio Element
challengeType: 0
videoUrl: 'https://scrimba.com/c/cVJVkcZ'
forumTopicId: 301014
---

## Description
<section id='description'>
HTML5's <code>audio</code> L'élément donne un sens sémantique lorsqu'il enveloppe le contenu du flux audio ou audio dans votre balisage. Le contenu audio a également besoin d'une alternative textuelle pour être accessible aux personnes sourdes ou malentendantes. Cela peut être fait avec du texte à proximité sur la page ou un lien vers une transcription.
Le <code>audio</code> balise prend en charge la <code>contrôles</code> attribut. Cela montre la lecture par défaut du navigateur, la pause et d'autres commandes, et prend en charge la fonctionnalité du clavier. Il s'agit d'un attribut booléen, ce qui signifie qu'il n'a pas besoin de valeur, sa présence sur la balise active le paramètre.
Voici un exemple:

```html
<audio id="meowClip" controls>
  <source src="audio/meow.mp3" type="audio/mpeg" />
  <source src="audio/meow.ogg" type="audio/ogg" />
</audio>
```

<strong>Note:</strong> Le contenu multimédia comporte généralement des composants visuels et auditifs. Il a besoin de sous-titres synchronisés et d'une transcription pour que les utilisateurs ayant des déficiences visuelles et / ou auditives puissent y accéder. En règle générale, un développeur Web n'est pas responsable de la création des légendes ou de la transcription, mais doit savoir les inclure.
</section>

## Instructions
<section id='instructions'>
Il est temps de prendre une pause avec Camper Cat et de rencontrer son camarade Zersiax (@zersiax), un champion de l'accessibilité et un utilisateur de lecteur d'écran. Pour entendre un extrait de son lecteur d'écran en action, ajoutez un<code>audio</code> élément après le <code>p</code>. Inclure le <code>contôle</code> attribut. Placez ensuite un <code>source</code> tag à l'intérieur du <code>audio</code> tags with the <code>src</code> attribut défini sur "https://s3.amazonaws.com/freecodecamp/screen-reader.mp3" and <code>type</code> attribut défini sur "audio/mpeg".
<strong>Note:</strong> Le clip audio peut sembler rapide et difficile à comprendre, mais il s'agit d'une vitesse normale pour les utilisateurs de lecteurs d'écran.
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: Your code should have one <code>audio</code> tag.
    testString: assert($('audio').length === 1);
  - text: Your <code>audio</code> element should have a closing tag.
    testString: assert(code.match(/<\/audio>/g).length === 1 && code.match(/<audio.*>[\s\S]*<\/audio>/g));
  - text: The <code>audio</code> tag should have the <code>controls</code> attribute.
    testString: assert($('audio').attr('controls'));
  - text: Your code should have one <code>source</code> tag.
    testString: assert($('source').length === 1);
  - text: Your <code>source</code> tag should be inside the <code>audio</code> tags.
    testString: assert($('audio').children('source').length === 1);
  - text: The value for the <code>src</code> attribute on the <code>source</code> tag should match the link in the instructions exactly.
    testString: assert($('source').attr('src') === 'https://s3.amazonaws.com/freecodecamp/screen-reader.mp3');
  - text: Your code should include a <code>type</code> attribute on the <code>source</code> tag with a value of audio/mpeg.
    testString: assert($('source').attr('type') === 'audio/mpeg');

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='html-seed'>

```html
<body>
  <header>
    <h1>Véritables ninjas de codage</h1>
  </header>
  <main>
    <p>Un extrait sonore du lecteur d'écran de Zersiax en action.</p>



  </main>
</body>
```

</div>



</section>

## Solution
<section id='solution'>

```html
<body>
  <header>
    <h1>Real Coding Ninjas</h1>
  </header>
  <main>
    <p>A sound clip of Zersiax's screen reader in action.</p>
    <audio controls>
      <source src="https://s3.amazonaws.com/freecodecamp/screen-reader.mp3" type="audio/mpeg"/>
    </audio>
  </main>
</body>
```

</section>
