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

<script>
document.querySelectorAll("foreignObject").forEach((block) => {
            block.addEventListener("dblclick", (e) => {
                e.preventDefault();
                console.log("block ", block)
                const code = block.textContent;
                
                console.log("🚀 Evaluating code:");
                console.log("block.textContent ", code);
                try {
                    eval(code);
                } catch (err) {
                    console.error(err);
                } finally {
                    console.log("✅ Done");
                }
            });
        });
</script>

[markdown]:
  https://github.com/web-classroom/heig-vd-web-course/blob/main/docs/03-javascript/COURSE_MATERIAL.md
[pdf]:
  https://web-classroom.github.io/heig-vd-web-course/docs/03-javascript/03-javascript-course-material.pdf
[license]:
  https://github.com/web-classroom/heig-vd-web-course/blob/main/LICENSE.md

## Where to run JavaScript

```html
<!DOCTYPE html>
<!-- color -->
<html>
  <head>
    <title>My first JavaScript</title>
  </head>
  <body>
    <h1>My first JavaScript</h1>
    <p>Click the button to display the date and time.</p>
    <button onclick="document.getElementById('demo').innerHTML = Date()">
      The time is?
    </button>
    <p id="demo"></p>
  </body>
</html>
```

---

# JavaScript

<https://github.com/web-classroom/heig-vd-web-course>

[Markdown][markdown] · [PDF][pdf]

This work is licensed under the [CC BY-SA 4.0][license] license.

---

### External file

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My first JavaScript</title>
    <script src="myScript.js"></script>
  </head>
  <body>
    <h1>My first JavaScript</h1>
    <p>Click the button to display the date and time.</p>
    <button onclick="displayDate()">The time is?</button>
    <p id="demo"></p>
  </body>
</html>
```

---

```javascript
function displayDate() {
  document.getElementById("demo").innerHTML = Date();
}
```

---

### Console

```javascript
console.log("Hello, World!");
```

---

### Node.js

```javascript title="myScript.js"
console.log("Hello, World!");
```

---

```bash
node myScript.js
```
