---
id: 587d774d367417b2b2512a9e
title: Use Headings to Show Hierarchical Relationships of Content
challengeType: 0
videoUrl: 'https://scrimba.com/c/cqVEktm'
forumTopicId: 301026
---

## Description
<section id='description'>
Rubriques (<code>h1</code> par <code>h6</code> éléments) sont des balises puissantes qui aident à structurer et à étiqueter votre contenu. Les lecteurs d'écran peuvent être configurés pour lire uniquement les en-têtes d'une page afin que l'utilisateur obtienne un résumé. Cela signifie qu'il est important que les balises de titre de votre balisage aient une signification sémantique et soient liées les unes aux autres, et non pas simplement choisies pour leurs valeurs de taille.
<em>Signification sémantique</em> signifie que la balise que vous utilisez autour du contenu indique le type d'informations qu'il contient.
Si vous écriviez un article avec une introduction, un corps et une conclusion, cela n'aurait pas beaucoup de sens de mettre la conclusion en tant que sous-section du corps dans votre plan. Ce devrait être sa propre section. De même, les balises de titre dans une page Web doivent aller dans l'ordre et indiquer les relations hiérarchiques de votre contenu.
Les en-têtes de rang égal (ou supérieur) commencent de nouvelles sections implicites, les en-têtes dont le rang est inférieur à ceux de la précédente.
Par exemple, une page avec un <code>h2</code> élément suivi de plusieurs sous-sections étiquetées avec <code>h4</code> les balises dérouteraient un utilisateur de lecteur d'écran. Avec six choix, il est tentant d'utiliser une balise car elle est plus belle dans un navigateur, mais vous pouvez utiliser CSS pour modifier le dimensionnement relatif.
Un dernier point, chaque page doit toujours en avoir un (et un seul) <code>h1</code> , qui est le sujet principal de votre contenu. Ceci et les autres titres sont utilisés en partie par les moteurs de recherche pour comprendre le sujet de la page.
</section>

## Instructions
<section id='instructions'>
Camper Cat veut une page sur son site dédiée à devenir un ninja. Aidez-le à corriger les titres afin que son balisage donne un sens sémantique au contenu et montre les relations parent-enfant appropriées de ses sections. Changer tous les <code>h5</code> balises au niveau de titre approprié pour indiquer qu'il s'agit de sous-sections du <code>h2</code> ceux. Utilisation<code>h3</code> balises à des fins.
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: Your code should have 6 <code>h3</code> tags.
    testString: assert($("h3").length === 6);
  - text: Your code should have 6 <code>h3</code> closing tags.
    testString: assert((code.match(/\/h3/g) || []).length===6);
  - text: Your code should not have any <code>h5</code> tags.
    testString: assert($("h5").length === 0);
  - text: Your code should not have any <code>h5</code> closing tags.
    testString: assert(/\/h5/.test(code)===false);
```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='html-seed'>

```html
<h1>Comment devenir un ninja</h1>
<main>
  <h2>Apprenez l'art de bouger furtivement</h2>
  <h5>Comment se cacher en clair</h5>
  <h5>Comment escalader un mur</h5>

  <h2>Apprenez l'art de la bataille</h2>
  <h5>Comment renforcer votre corps</h5>
  <h5>Comment se battre comme un ninja</h5>

  <h2>Apprenez l'art de vivre avec honneur</h2>
  <h5>Comment respirer correctement</h5>
  <h5>Comment respirer correctement</h5>
</main>
```

</div>



</section>

## Solution
<section id='solution'>

```html
<h1>Comment devenir un ninja</h1>
<main>
  <h2>Apprenez l'art de bouger furtivement</h2>
  <h3>Comment se cacher en clair</h3>
  <h3>Comment escalader un mur</h3>

  <h2>Apprenez l'art de la bataille</h2>
  <h3>Comment renforcer votre corps</h3>
  <h3>Comment se battre comme un ninja</h3>

  <h2>Learn the Art of Living with Honor</h2>
  <h3>Comment respirer correctement</h3>
  <h3>Comment simplifier votre vie</h3>
</main>
```

</section>
