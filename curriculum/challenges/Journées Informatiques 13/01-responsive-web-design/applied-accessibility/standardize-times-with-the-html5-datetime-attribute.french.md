---
id: 587d778c367417b2b2512aa9
title: Standardize Times with the HTML5 datetime Attribute
challengeType: 0
videoUrl: 'https://scrimba.com/c/cmzMgtz'
forumTopicId: 301025
---

## Description
<section id='description'>
Poursuivant avec le thème de la date, HTML5 a également introduit le <code>temps</code> élément avec un <code>datetime</code> attribut pour normaliser les temps. Il s'agit d'un élément en ligne qui peut encapsuler une date ou une heure sur une page. Un format valide de cette date est détenu par le <code>datetime</code> attribut. Il s'agit de la valeur accessible par les appareils et accessoires fonctionnels. Il aide à éviter toute confusion en énonçant une version standardisée d'une heure, même si elle est écrite de manière informelle ou familière dans le texte.
Voici un exemple:
<code>&lt;p&gt;Master Camper Cat a officié le match de cage entre Goro et Scorpion &lt;time datetime=&quot;2013-02-13&quot;&gt;last Wednesday&lt;/time&gt;, qui s'est terminé par un match nul.&lt;/p&gt;</code>
</section>

## Instructions
<section id='instructions'>
Les résultats de l'enquête Mortal Kombat de Camper Cat sont arrivés! Envelopper un<code>time</code> tag autour du texte "jeudi, septembre 15&lt;sup&gt;th&lt;/sup&gt;" et ajoutez un <code>datetime</code> attribuez-lui la valeur "2016-09-15".
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: Your code should have a <code>p</code> element which includes the text "Thank you to everyone for responding to Master Camper Cat's survey." and include a <code>time</code> element.
    testString: assert(timeElement.length);
  - text: Your added <code>time</code> tags should wrap around the text "Thursday, September 15&lt;sup&gt;th&lt;/sup&gt;".
    testString: assert(timeElement.length && $(timeElement).html().trim() === "Thursday, September 15<sup>th</sup>");
  - text: Your added <code>time</code> tag should have a <code>datetime</code> attribute that is not empty.
    testString: assert(datetimeAttr && datetimeAttr.length);
  - text: Your added <code>datetime</code> attribute should be set to a value of 2016-09-15.
    testString: assert(datetimeAttr === "2016-09-15");
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
  <article>
    <h2>Résultat de l'enquête sur le tournoi Mortal Kombats</h2>

    <!-- Add your code below this line -->

    <p>Merci à tous d'avoir répondu au sondage de Master Camper Cat. Le meilleur jour pour accueillir le tournoi tant convoité de Mortal Kombat est le jeudi septembre 15<sup>th</sup>. Que le meilleur ninja gagne!</p>

    <!-- Add your code above this line -->

    <section>
      <h3>Commentaires</h3>
      <article>
        <p>Posté par: Sub-Zero on <time datetime="2016-08-13T20:01Z">août 13<sup>th</sup></time></p>
        <p>Johnny Cage ferait mieux d'être là, je vais le finir!</p>
      </article>
      <article>
        <p>Posté par: Doge on <time datetime="2016-08-15T08:12Z">août 15<sup>th</sup></time></p>
        <p>Wow, beaucoup de combat, donc mortel.</p>
      </article>
      <article>
        <p>Posté par: The Grim Reaper on <time datetime="2016-08-16T00:00Z">août  16<sup>th</sup></time></p>
        <p>On dirait que je serai occupé ce jour-là.</p>
      </article>
    </section>
  </article>
  <footer>&copy; 2018 Camper Cat</footer>
</body>
```

</div>

<div id='html-teardown'>

```html
<script>
const pElement = $("article > p")
  .filter((_, elem) => $(elem).text().includes("Thank you to everyone for responding to Master Camper Cat's survey."));
const timeElement = pElement[0] ? $(pElement[0]).find("time") : null;
const datetimeAttr = $(timeElement).attr("datetime");
</script>
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
  <article>
    <h2>Résultats de l'enquête sur le tournoi Mortal Kombat</h2>
    
    <!-- Add your code below this line -->
    
    <p>Merci à tous d'avoir répondu au sondage de Master Camper Cat. Le meilleur jour pour accueillir le vanté tournoi Mortal Kombat est<time datetime="2016-09-15">Jeudi 15 septembre<sup>th</sup></time>. Que le meilleur ninja gagne!</p>
    
    <!-- Add your code above this line -->
    
    <section>
      <h3>Commentaires:</h3>
      <article>
        <p>Posté par: Sub-Zero on <time datetime="2016-08-13T20:01Z">août 13<sup>th</sup></time></p>
        <p>Johnny Cage ferait mieux d'être là, je vais le finir!</p>
      </article>
      <article>
        <p>Posté par: Doge on <time datetime="2016-08-15T08:12Z">août15<sup>th</sup></time></p>
        <p>Wow, beaucoup de combat, donc mortel.</p>
      </article>
      <article>
        <p>Posté par: The Grim Reaper on <time datetime="2016-08-16T00:00Z">août 16<sup>th</sup></time></p>
        <p>On dirait que je serai occupé ce jour-là.</p>
      </article>
    </section>
  </article>
  <footer>&copy; 2018 Camper Cat</footer>
</body>
```

</section>
