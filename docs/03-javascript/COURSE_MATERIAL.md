[markdown]:
  https://github.com/web-classroom/heig-vd-web-course/blob/main/docs/03-javascript/COURSE_MATERIAL.md
[pdf]:
  https://web-classroom.github.io/heig-vd-web-course/docs/03-javascript/03-javascript-course-material.pdf
[license]:
  https://github.com/web-classroom/heig-vd-web-course/blob/main/LICENSE.md

# JavaScript

<https://github.com/web-classroom/heig-vd-web-course>

[Markdown][markdown] · [PDF][pdf]

This work is licensed under the [CC BY-SA 4.0][license] license.

## Where to run JavaScript

### HTML tags

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My first JavaScript</title>
  </head>
  <body>
    <h1>My first JavaScript</h1>
    <p>Click the button to display the date and time.</p>
    <button onclick="document.getElementById('demo').innerHTML = Date()">The time is?</button>
    <p id="demo"></p>
  </body>
</html>
```

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

```javascript
function displayDate() {
  document.getElementById('demo').innerHTML = Date();
}
```

### Console

```javascript
console.log('Hello, World!');
```

### Node.js

```javascript title="myScript.js"
console.log('Hello, World!');
```

```bash
node myScript.js
```

