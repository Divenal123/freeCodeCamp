---
id: 587d778f367417b2b2512aad
title: Avoid Colorblindness Issues by Carefully Choosing Colors that Convey Information
challengeType: 0
videoUrl: 'https://scrimba.com/c/c437as3'
forumTopicId: 301011
---

## Description
<section id='description'>
Il existe différentes formes de daltonisme. Celles-ci peuvent aller d'une sensibilité réduite à une certaine longueur d'onde de lumière à l'incapacité de voir la couleur. La forme la plus courante est une sensibilité réduite pour détecter les verts.
Par exemple, si deux couleurs vertes similaires sont la couleur de premier plan et d'arrière-plan de votre contenu, un utilisateur daltonien peut ne pas être en mesure de les distinguer. Les couleurs proches peuvent être considérées comme des voisins sur la roue chromatique, et ces combinaisons doivent être évitées lors de la transmission d'informations importantes.
<strong>Note:</strong> Certains outils de sélection de couleurs en ligne incluent des simulations visuelles de l'apparence des couleurs pour différents types de daltonisme. Ce sont d'excellentes ressources en plus des calculatrices de vérification de contraste en ligne.
</section>

## Instructions
<section id='instructions'>
Camper Cat teste différents styles pour un bouton important, mais le jaune (<code>#FFFF33</code>) <code>background-color</code> et le vert (<code>#33FF33</code>) texte <code>color</code> sont des teintes voisines sur la roue chromatique et pratiquement indiscernables pour certains utilisateurs daltoniens. (Leur légèreté similaire échoue également à la vérification du rapport de contraste). Changer le texte <code>color</code> à un bleu foncé (<code>#003366</code>) pour résoudre les deux problèmes.
</section>

## Tests
<section id='tests'>

```yml
tests:
  - text: Your code should change the text <code>color</code> for the <code>button</code> to the dark blue.
    testString: assert($('button').css('color') == 'rgb(0, 51, 102)');

```

</section>

## Challenge Seed
<section id='challengeSeed'>

<div id='html-seed'>

```html
<head>
  <style>
  button {
    color: #33FF33;
    background-color: #FFFF33;
    font-size: 14px;
    padding: 10px;
  }
  </style>
</head>
<body>
  <header>
    <h1>Danger!</h1>
  </header>
  <button>Supprimer Internet</button>
</body>
```

</div>



</section>

## Solution
<section id='solution'>

```html
<head>
  <style>
    button {
      color: #003366;
      background-color: #FFFF33;
      font-size: 14px;
      padding: 10px;
    }
  </style>
</head>
<body>
  <header>
    <h1>Danger!</h1>
  </header>
  <button>Supprimer Internet</button>
</body>
```

</section>
