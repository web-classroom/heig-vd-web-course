---
marp: true
---

<!--
theme: gaia
size: 16:9
paginate: true
author: B. Chapuis, O. Lemer, O. Tischauser, V. Guidoux, with the help of ChatGPT.
url: https://web-classroom.github.io/
footer: '**HEIG-VD** - WEB Course 2023-2024 - AGPL-3.0 license'
style: |
    :root {
        --color-background: #fff;
        --color-foreground: #333;
        --color-highlight: #f96;
        --color-dimmed: #888;
        --color-headings: #7d8ca3;
    }
    blockquote {
        font-style: italic;
    }
    table {
        width: 100%;
    }
    th:first-child {
        width: 15%;
    }
    h1, h2, h3, h4, h5, h6 {
        color: var(--color-headings);
    }
    h2, h3, h4, h5, h6 {
        font-size: 1.5rem;
    }
    h1 a:link, h2 a:link, h3 a:link, h4 a:link, h5 a:link, h6 a:link {
        text-decoration: none;
    }
    section:not([class=lead]) > p, blockquote {
        text-align: justify;
    }
    ul {
        margin-top: 0.5rem;
    }
    section::after {
      content: attr(data-marpit-pagination-) '/' attr(data-marpit-pagination-total);
    }
-->

[web]:
  https://web-classroom.github.io/heig-vd-web-course/docs/04-lab-1-html-css/index.html
[pdf]:
  https://web-classroom.github.io/heig-vd-web-course/docs/04-lab-1-html-css/04-lab-1-html-css-presentation.pdf
[license]:
  https://github.com/web-classroom/heig-vd-web-course/blob/main/LICENSE.md
[illustration]:
  https://images.unsplash.com/photo-1594434533760-02e0f3faaa68?q=80&w=1938&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D
[source]:
  https://github.com/web-classroom/heig-vd-web-course/blob/main/docs/04-lab-1-html-css/PRESENTATION.md

# Web Technologies

## Lab 1: HTML & CSS

<!--
_class: lead
_paginate: false
-->

<https://github.com/web-classroom/heig-vd-web-course>

[Web][web] · [PDF][pdf] · [Source][source]

<small>This work is licensed under the [CC BY-SA 4.0][license] license.</small>

![bg opacity:0.1][illustration]

---

## Bad practice

---

<!-- - Est-ce qu'une personne qui tombe sur mon code va le comprendre ? Pensez à enlever le code qui ne sert à rien pour aider à la compréhension
- séparé en plusieurs fichiers CSS
- Nested CSS (avez-vous utilisé ChatGPT ? Avez-vous conscience de ce que vous avez fait ?)
- Cohérence dans l'utilisation de soit Grid soit flex. Mais nous avons de très bons exemples avec du grid pour définir la structure principale et après du flex pour les détails.
- Texte dans p, span, h1, h2, h3
- div uniquement pour séparer
- Utilisation des variables CSS au lieu de créer une classe pour une couleur.
- Utilisation de calc()
- Bien joué pour les personnes qui ont ajouté un petit hover par dessus certains élèments
- utilisation de l'attribut font :

  /* font-size/line height font-family */
  font: 1.2em/2 "Fira Sans", sans-serif;

- Nommage des classes/ids, éviter :
   - gif1, gif2, gif3, gifn...
   - right-zone-left-top (Peut-être aviez-vous l'habitude de travailler avec bootstrap -->

---

## Good practice

Will someone who comes across my code understand it? Remove unnecessary code to
help with understanding.

---

- Separated into multiple CSS files

---

- Nested CSS (Did you use ChatGPT? Are you aware of what you did?)

```css
/* Before */
#header {
  color: red;
}
#header .title {
  font-size: 2em;
}

/* After */
#header {
  color: red;
  .title {
    font-size: 2em;
  }
}
```

## Sources

<!-- homme-en-sweat-a-capuche-nike-noir-portant-des-ecouteurs-noirs -->

- [Homme en sweat à capuche Nike noir portant des écouteurs noirs](https://images.unsplash.com/photo-1594434533760-02e0f3faaa68?q=80&w=1938&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D)
