---
id: 587d7790367417b2b2512ab1
title: Use tabindex to Specify the Order of Keyboard Focus for Several Elements
challengeType: 0
videoUrl: 'https://scrimba.com/c/cmzRRcb'
forumTopicId: 301028
---

## Description
<section id='description'>
Le <code>tabindex</code> L'attribut spécifie également l'ordre de tabulation exact des éléments. Ceci est réalisé lorsque la valeur de l'attribut est définie sur un nombre positif de 1 ou supérieur.
La définition d'un tabindex = "1" amènera d'abord le focus clavier à cet élément. Ensuite, il parcourt la séquence de spécifiés <code>tabindex</code> values (2, 3, etc.), avant de passer à la valeur par défaut et <code>tabindex="0"</code> articles.
Il est important de noter que lorsque l'ordre de tabulation est défini de cette façon, il remplace l'ordre par défaut (qui utilise la source HTML). Cela peut dérouter les utilisateurs qui s'attendent à démarrer la navigation depuis le haut de la page. Cette technique peut être nécessaire dans certaines circonstances, mais en termes d'accessibilité, faites attention avant de l'appliquer.
Voici un exemple:
<code>&lt;div tabindex=&quot;1&quot;&gt;Je reçois le focus du clavier, et je l'obtiens en premier!&lt;/div&gt;</code>
<code>&lt;div tabindex=&quot;2&quot;&gt;Je reçois le focus du clavier et je le reçois en second!&lt;/div&gt;</code>
</section>

## Instructions
<section id='instructions'>
Camper Cat a un champ de recherche sur sa page Inspirational Quotes qu'il prévoit de positionner dans le coin supérieur droit avec CSS. Il veut la recherche <code>input</code> et soumettre<code>input</code> contrôles de formulaire pour être les deux premiers éléments dans l'ordre de tabulation. Ajouter un <code>tabindex</code> attribut défini sur "1" pour la recherche<code>input</code>, et un <code>tabindex</code> attribut défini sur "2" pour la soumission <code>input</code>.
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: Your code should add a <code>tabindex</code> attribute to the search <code>input</code> tag.
    testString: assert($('#search').attr('tabindex'));
  - text: Your code should add a <code>tabindex</code> attribute to the submit <code>input</code> tag.
    testString: assert($('#submit').attr('tabindex'));
  - text: Your code should set the <code>tabindex</code> attribute on the search <code>input</code> tag to a value of 1.
    testString: assert($('#search').attr('tabindex') == '1');
  - text: Your code should set the <code>tabindex</code> attribute on the submit <code>input</code> tag to a value of 2.
    testString: assert($('#submit').attr('tabindex') == '2');

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='html-seed'>

```html
<body>
  <header>
    <h1>Des pensées encore plus profondes avec Master Camper Cat</h1>
    <nav>
      <ul>
        <li><a href="">Home</a></li>
        <li><a href="">Blog</a></li>
        <li><a href="">Training</a></li>
      </ul>
    </nav>
  </header>
  <form>
    <label for="search">Search:</label>


    <input type="search" name="search" id="search">
    <input type="submit" name="submit" value="Submit" id="submit">


  </form>
  <h2>Citations inspirantes</h2>
  <blockquote>
    <p>&ldquo;Il n'y a pas de théorie de l'évolution, juste une liste de créatures que j'ai autorisées à vivre.&rdquo;<br>
    - Chuck Norris</p>
  </blockquote>
  <blockquote>
    <p>&ldquo;Les sages disent que le pardon est divin, mais ne payez jamais le prix fort pour une pizza tardive.&rdquo;<br>
    - TMNT</p>
  </blockquote>
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
    <h1>Des pensées encore plus profondes avec Master Camper Cat</h1>
    <nav>
      <ul>
        <li><a href="">Home</a></li>
        <li><a href="">Blog</a></li>
        <li><a href="">Training</a></li>
      </ul>
    </nav>
  </header>
  <form>
    <label for="search">Search:</label>


    <input tabindex="1" type="search" name="search" id="search">
    <input tabindex="2" type="submit" name="submit" value="Submit" id="submit">


  </form>
  <h2>Citations inspirantes</h2>
  <blockquote>
    <p>&ldquo;Il n'y a pas de théorie de l'évolution, juste une liste de créatures que j'ai autorisées à vivre.&rdquo;<br>
    - Chuck Norris</p>
  </blockquote>
  <blockquote>
    <p>&ldquo;Les sages disent que le pardon est divin, mais ne payez jamais le prix fort pour une pizza tardive.&rdquo;<br>
    - TMNT</p>
  </blockquote>
  <footer>&copy; 2018 Camper Cat</footer>
</body>
```

</section>
