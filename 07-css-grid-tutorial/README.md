#### 302. [CSS Grid - Intro](#302)

#### 303. [Setup](#303)

#### 304. [Basic Syntax - grid-template-columns](#304)

#### 305. [Implicit Grid](#305)

#### 306. [General CSS Setup](#306)

#### 307. [Units - auto](#307)

#### 308. [grid-template-rows](#308)

#### 309. [fr units](#309)

#### 310. [gap property](#310)

#### 311. [Gap - New Syntax!](#311)

#### 312. [fr vs %](#312)

#### 313. [Firefox Developer Tools](#313)

#### 314. [grid-lines](#314)

#### 315. [Naming Grid Lines](#315)

#### 316. [Grid Template Areas](#316)

#### 317. [Order Property](#317)

#### 318. [Repeat Function](#318)

#### 319. [justify-content](#319)

#### 320. [align-content](#320)

#### 321. [align-items, jusitfy-items, align-self,justify-self](#321)

#### 322. [minmax()](#322)

#### 323. [auto-fit and auto-fill](#323)

<br>

### 302. CSS Grid - Intro<a id="302"></a>

<br>

### 303. Setup<a id="303"></a>

> **_Business Objective: Layout_**

<img src="notes/setup.png" width="900">

---

- In index.html

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Grid Tutorial</title>
    <link rel="stylesheet" href="styles.css" />

    <style></style>
  </head>
  <body>
    <div class="container">
      <div class="cell">cell 1</div>
      <div class="cell">cell 2</div>
    </div>
  </body>
</html>
```

---

- In style.css

```js
// reset window by overriding default css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  color: #222;
}
.container {
  border: 5px solid black;
}
.cell {
  padding: 2rem;
  background: #dedede;
  text-transform: uppercase;
  font-weight: bold;
  text-align: center;
  border: 3px solid red;
  color: #fff;
}


```

<br>

### 304. Basic Syntax - grid-template-columns<a id="304"></a>

> **_Business Objective: Layout_**

<img src="notes/02-implicit-grid.png" width="900">

---

- In index.html

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Grid Tutorial</title>
    <link rel="stylesheet" href="styles.css" />

    <style>
      /* How to setup grid layout */
      .container {
        display: grid;
        grid-template-columns: 200px 300px;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="cell">cell 1</div>
      <div class="cell">cell 2</div>
    </div>
  </body>
</html>
```

---

- In styles.css

```css
/* reset window */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  color: #222;
}
.container {
  border: 5px solid black;
}
.cell {
  padding: 2rem;
  background: #dedede;
  text-transform: uppercase;
  font-weight: bold;
  text-align: center;
  border: 3px solid red;
  color: #fff;
}
.cell-1 {
  background: #581f18;
}
.cell-2 {
  background: #f0a202;
}
.cell-3 {
  background: #d95d39;
}
.cell-4 {
  background: #202c59;
}
.cell-5 {
  background: #51cb20;
}
```

<br>

### 305. Implicit Grid<a id="305"></a>

> **_Business Objective: Layout_**

<img src="notes/03-color-values.png" width="900">

---

- In index.html

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Grid Tutorial</title>
    <link rel="stylesheet" href="styles.css" />

    <style>
      .container {
        display: grid;
        /* 3 column layout */
        grid-template-columns: 200px 300px 200px;
      }
    </style>
  </head>
  <body>
    <!-- color values -->
    <div class="container">
      <div class="cell cell-1">cell 1</div>
      <div class="cell cell-2">cell 2</div>
      <div class="cell cell-3">cell 3</div>
      <div class="cell cell-4">cell 4</div>
      <div class="cell cell-5">cell 5</div>
      <div class="cell">cell 6</div>
      <div class="cell">cell 7</div>
    </div>
  </body>
</html>
```

---

- In styles.css

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  color: #222;
}
.container {
  border: 5px solid black;
}
.cell {
  padding: 2rem;
  background: #dedede;
  text-transform: uppercase;
  font-weight: bold;
  text-align: center;
  border: 3px solid red;
  color: #fff;
}
.cell-1 {
  background: #581f18;
}
.cell-2 {
  background: #f0a202;
}
.cell-3 {
  background: #d95d39;
}
.cell-4 {
  background: #202c59;
}
.cell-5 {
  background: #51cb20;
}
```

<br>

### 306. General CSS Setup<a id="306"></a>

> **_Business Objective: Layout_**

<img src="notes/04-units-auto.png" width="900">

---

- In index.html

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Grid Tutorial</title>
    <link rel="stylesheet" href="styles.css" />
    <style>
      .container {
        display: grid;
        grid-template-columns: 200px 300px 200px;
      }
    </style>
  </head>
  <body>
    <!-- color values -->
    <div class="container">
      <div class="cell cell-1">cell 1</div>
      <div class="cell cell-2">cell 2</div>
      <div class="cell cell-3">cell 3</div>
      <div class="cell cell-4">cell 4</div>
      <div class="cell cell-5">cell 5</div>
      <div class="cell">cell 6</div>
      <div class="cell">cell 7</div>
    </div>
  </body>
</html>
```

---

- In styles.css

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  color: #222;
}
.container {
  border: 5px solid black;
}
.cell {
  padding: 2rem;
  background: #dedede;
  text-transform: uppercase;
  font-weight: bold;
  text-align: center;
  border: 3px solid red;
  color: #fff;
}
.cell-1 {
  background: #581f18;
}
.cell-2 {
  background: #f0a202;
}
.cell-3 {
  background: #d95d39;
}
.cell-4 {
  background: #202c59;
}
.cell-5 {
  background: #51cb20;
}
```

<br>

### 307. Units - auto<a id="307"></a>

> **_Business Objective: Layout_**

<img src="notes/05-grid-rows.png" width="900">

---

- In index.html

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Grid Tutorial</title>
    <link rel="stylesheet" href="styles.css" />
    <style>
      /* units - rows as well */
      /* px rem em % auto fr  */
      .container {
        display: grid;
        grid-template-columns: 200px 7rem auto;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="cell cell-1">cell 1</div>
      <div class="cell cell-2">cell 2</div>
      <div class="cell cell-3">cell 3</div>
      <div class="cell cell-4">cell 4</div>
      <div class="cell cell-5">cell 5</div>
      <div class="cell">cell 6</div>
      <div class="cell">cell 7</div>
    </div>
  </body>
</html>
```

---

- In styles.css

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  color: #222;
}
.container {
  border: 5px solid black;
}
.cell {
  padding: 2rem;
  background: #dedede;
  text-transform: uppercase;
  font-weight: bold;
  text-align: center;
  border: 3px solid red;
  color: #fff;
}
.cell-1 {
  background: #581f18;
}
.cell-2 {
  background: #f0a202;
}
.cell-3 {
  background: #d95d39;
}
.cell-4 {
  background: #202c59;
}
.cell-5 {
  background: #51cb20;
}
```

<br>

### 308. grid-template-rows<a id="308"></a>

> **_Business Objective: Layout_**

<img src="notes/app.png" width="900">

---

- In index.html

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Grid Tutorial</title>
    <link rel="stylesheet" href="styles.css" />
    <style>
      /* rows */
      .container {
        min-height: 100vh;
        display: grid;

        /* expand column horizontally */
        grid-template-columns: 200px auto 10rem;

        /* expand row vertically */
        grid-template-rows: auto 5rem;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="cell cell-1">cell 1</div>
      <div class="cell cell-2">cell 2</div>
      <div class="cell cell-3">cell 3</div>
      <div class="cell cell-4">cell 4</div>
      <div class="cell cell-5">cell 5</div>
      <div class="cell">cell 6</div>
      <div class="cell">cell 7</div>
    </div>
  </body>
</html>
```

---

- In styles.css

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  color: #222;
}
.container {
  border: 5px solid black;
}
.cell {
  padding: 2rem;
  background: #dedede;
  text-transform: uppercase;
  font-weight: bold;
  text-align: center;
  border: 3px solid red;
  color: #fff;
}
.cell-1 {
  background: #581f18;
}
.cell-2 {
  background: #f0a202;
}
.cell-3 {
  background: #d95d39;
}
.cell-4 {
  background: #202c59;
}
.cell-5 {
  background: #51cb20;
}
```

<br>

### 309. fr units<a id="309"></a>

> **_Business Objective: Layout_**

<img src="notes/06-fr-unit.png" width="900">

---

- In index.html

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Grid Tutorial</title>
    <link rel="stylesheet" href="styles.css" />
    <style>
      /* fr units - fraction of available space */
      .container {
        min-height: 100vh;
        display: grid;

        /* How to use fraction unit for available space*/
        grid-template-columns: 1fr 5fr 3fr 1fr;
        grid-template-rows: 1fr 1fr 1fr;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="cell cell-1">cell 1</div>
      <div class="cell cell-2">cell 2</div>
      <div class="cell cell-3">cell 3</div>
      <div class="cell cell-4">cell 4</div>
      <div class="cell cell-5">cell 5</div>
      <div class="cell">cell 6</div>
      <div class="cell">cell 7</div>
    </div>
  </body>
</html>
```

---

- In styles.css

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  color: #222;
}
.container {
  border: 5px solid black;
}
.cell {
  padding: 2rem;
  background: #dedede;
  text-transform: uppercase;
  font-weight: bold;
  text-align: center;
  border: 3px solid red;
  color: #fff;
}
.cell-1 {
  background: #581f18;
}
.cell-2 {
  background: #f0a202;
}
.cell-3 {
  background: #d95d39;
}
.cell-4 {
  background: #202c59;
}
.cell-5 {
  background: #51cb20;
}
```

<br>

### 310. gap property<a id="310"></a>

> **_Business Objective: Layout_**

<img src="notes/07-gap.png" width="900">

---

- In index.html

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Grid Tutorial</title>
    <link rel="stylesheet" href="styles.css" />
    <style>
      /* gap */
      .container {
        min-height: 100vh;
        display: grid;
        grid-template-columns: 1fr 5fr 3fr 1fr;
        grid-template-rows: 1fr 1fr 1fr;

        /* How to put gat b/w column */
        grid-column-gap: 20px;

        /* How to put gat b/w row */
        grid-row-gap: 20px;

        /* shorthand for column and row in one-line */
        grid-gap: 50px 100px;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="cell cell-1">cell 1</div>
      <div class="cell cell-2">cell 2</div>
      <div class="cell cell-3">cell 3</div>
      <div class="cell cell-4">cell 4</div>
      <div class="cell cell-5">cell 5</div>
      <div class="cell">cell 6</div>
      <div class="cell">cell 7</div>
    </div>
  </body>
</html>
```

---

- In styles.css

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  color: #222;
}
.container {
  border: 5px solid black;
}
.cell {
  padding: 2rem;
  background: #dedede;
  text-transform: uppercase;
  font-weight: bold;
  text-align: center;
  border: 3px solid red;
  color: #fff;
}
.cell-1 {
  background: #581f18;
}
.cell-2 {
  background: #f0a202;
}
.cell-3 {
  background: #d95d39;
}
.cell-4 {
  background: #202c59;
}
.cell-5 {
  background: #51cb20;
}
```

<br>

### 311. Gap - New Syntax!<a id="311"></a>

> **_Business Objective: Layout_**

<img src="notes/08-gap-new-syntax.png" width="900">

---

- In index.html

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Grid Tutorial</title>
    <link rel="stylesheet" href="styles.css" />
    <style>
      /* grid-gap - absolete */
      /* gap */
      .container {
        min-height: 100vh;
        display: grid;
        grid-template-columns: 1fr 5fr 3fr 1fr;
        grid-template-rows: 1fr 1fr 1fr;
        /* grid-column-gap: 20px;
        grid-row-gap: 20px;
        grid-gap: 50px 100px; */

        /* New syntax for the same functionality */
        column-gap: 50px;
        row-gap: 50px;
        gap: 100px 25px;
        gap: 10px;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="cell cell-1">cell 1</div>
      <div class="cell cell-2">cell 2</div>
      <div class="cell cell-3">cell 3</div>
      <div class="cell cell-4">cell 4</div>
      <div class="cell cell-5">cell 5</div>
      <div class="cell">cell 6</div>
      <div class="cell">cell 7</div>
    </div>
  </body>
</html>
```

---

- In styles.css

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  color: #222;
}
.container {
  border: 5px solid black;
}
.cell {
  padding: 2rem;
  background: #dedede;
  text-transform: uppercase;
  font-weight: bold;
  text-align: center;
  border: 3px solid red;
  color: #fff;
}
.cell-1 {
  background: #581f18;
}
.cell-2 {
  background: #f0a202;
}
.cell-3 {
  background: #d95d39;
}
.cell-4 {
  background: #202c59;
}
.cell-5 {
  background: #51cb20;
}
```

<br>

### 312. fr vs %<a id="312"></a>

> **_Business Objective: Layout_**

<img src="notes/09-fr-vs.png" width="900">

---

- In index.html

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Grid Tutorial</title>
    <link rel="stylesheet" href="styles.css" />
    <style>
      /*  */
      .container {
        min-height: 100vh;
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-template-rows: 1fr 1fr 1fr;
        grid-column-gap: 20px;
        grid-row-gap: 20px;
        grid-gap: 50px 100px;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="cell cell-1">cell 1</div>
      <div class="cell cell-2">cell 2</div>
      <div class="cell cell-3">cell 3</div>
      <div class="cell cell-4">cell 4</div>
      <div class="cell cell-5">cell 5</div>
      <div class="cell">cell 6</div>
      <div class="cell">cell 7</div>
    </div>
  </body>
</html>
```

---

- In styles.css

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  color: #222;
}
.container {
  border: 5px solid black;
}
.cell {
  padding: 2rem;
  background: #dedede;
  text-transform: uppercase;
  font-weight: bold;
  text-align: center;
  border: 3px solid red;
  color: #fff;
}
.cell-1 {
  background: #581f18;
}
.cell-2 {
  background: #f0a202;
}
.cell-3 {
  background: #d95d39;
}
.cell-4 {
  background: #202c59;
}
.cell-5 {
  background: #51cb20;
}
```

<br>

### 313. Firefox Developer Tools<a id="313"></a>

> **_Business Objective: Layout_**

<img src="notes/app.png" width="900">

---

- In index.html

```html

```

---

- In styles.css

```css

```

<br>

### 314. grid-lines<a id="314"></a>

> **_Business Objective: Layout_**

<img src="notes/10-grid-lines.png" width="900">

---

- In index.html

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Grid Tutorial</title>
    <link rel="stylesheet" href="styles.css" />
    <style>
      /* grid lines - column lines, row lines  */
      .container {
        margin: 7rem;
        min-height: 100vh;
        display: grid;
        grid-template-columns: 100px 100px 100px;
        grid-template-rows: 100px 100px 100px;
        grid-gap: 1rem;
      }

      /* How to use grid line like python UI module */
      /* create: calculator. keyboard, matrix, window 8 Start, any layout */
      .cell-1 {
        /* grid-column-start: 1;
        grid-column-end: 3; */
        /* grid-row-start: 1;
        grid-row-end: 3; */

        /* shorthand: where cell start and where cell end*/
        grid-column: 1/3;
        grid-row: 1/3;
      }

      .cell-4 {
        grid-column: 1/-1;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="cell cell-1">cell 1</div>
      <div class="cell cell-2">cell 2</div>
      <div class="cell cell-3">cell 3</div>
      <div class="cell cell-4">cell 4</div>
      <div class="cell cell-5">cell 5</div>
      <div class="cell">cell 6</div>
      <div class="cell">cell 7</div>
    </div>
  </body>
</html>
```

---

- In styles.css

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  color: #222;
}
.container {
  border: 5px solid black;
}
.cell {
  padding: 2rem;
  background: #dedede;
  text-transform: uppercase;
  font-weight: bold;
  text-align: center;
  border: 3px solid red;
  color: #fff;
}
.cell-1 {
  background: #581f18;
}
.cell-2 {
  background: #f0a202;
}
.cell-3 {
  background: #d95d39;
}
.cell-4 {
  background: #202c59;
}
.cell-5 {
  background: #51cb20;
}
```

<br>

### 315. Naming Grid Lines<a id="315"></a>

> **_Business Objective: Layout_**

<img src="notes/11-naming-grid-lines.png" width="900">

---

- In index.html

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Grid Tutorial</title>
    <link rel="stylesheet" href="styles.css" />
    <style>
      /* naming grid lines  */
      .container {
        margin: 7rem;
        min-height: 100vh;
        display: grid;
        grid-template-columns: [start] 100px [col-1-end] 100px [col-2-end] 100px [end];
        grid-template-rows: [start] 100px [row-1-end] 100px [row-2-end] 100px [end];
        grid-gap: 1rem;
      }
      .cell-1 {
        grid-column: start/col-2-end;
        grid-row: start/row-2-end;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="cell cell-1">cell 1</div>
      <div class="cell cell-2">cell 2</div>
      <div class="cell cell-3">cell 3</div>
      <div class="cell cell-4">cell 4</div>
      <div class="cell cell-5">cell 5</div>
      <div class="cell">cell 6</div>
      <div class="cell">cell 7</div>
    </div>
  </body>
</html>
```

---

- In styles.css

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  color: #222;
}
.container {
  border: 5px solid black;
}
.cell {
  padding: 2rem;
  background: #dedede;
  text-transform: uppercase;
  font-weight: bold;
  text-align: center;
  border: 3px solid red;
  color: #fff;
}
.cell-1 {
  background: #581f18;
}
.cell-2 {
  background: #f0a202;
}
.cell-3 {
  background: #d95d39;
}
.cell-4 {
  background: #202c59;
}
.cell-5 {
  background: #51cb20;
}
```

<br>

### 316. Grid Template Areas<a id="316"></a>

> **_Business Objective: Layout_**

<img src="notes/12-grid-template-areas.png" width="900">

---

- In index.html

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Grid Tutorial</title>
    <link rel="stylesheet" href="styles.css" />
    <style>
      /* grid template areas  */
      .container {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        grid-template-rows: 100px 100px 100px 100px 100px;
        grid-template-areas:
          "a a b"
          "a a b"
          "c c b"
          "d d d"
          "e f f";
      }
      .cell-1 {
        grid-area: a;
      }
      .cell-2 {
        grid-area: b;
      }
      .cell-3 {
        grid-area: c;
      }
      .cell-4 {
        grid-area: d;
      }
      .cell-5 {
        grid-area: e;
      }
      .cell-6 {
        grid-area: f;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="cell cell-1">cell 1</div>
      <div class="cell cell-2">cell 2</div>
      <div class="cell cell-3">cell 3</div>
      <div class="cell cell-4">cell 4</div>
      <div class="cell cell-5">cell 5</div>
      <div class="cell cell-6">cell 6</div>
    </div>
  </body>
</html>
```

---

- In areas.html

```js
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <link rel="stylesheet" href="styles.css" />
    <title>Document</title>
    <style>
      .container {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        grid-template-rows: 100px 100px 100px 100px 100px;
        grid-template-areas:
          "a a b"
          "a a b"
          "c c b"
          "d d d"
          "e f f";
      }
      .cell-1 {
        grid-area: a;
      }
      .cell-2 {
        grid-area: b;
      }
      .cell-3 {
        grid-area: c;
      }
      .cell-4 {
        grid-area: d;
      }
      .cell-5 {
        grid-area: e;
      }
      .cell-6 {
        grid-area: f;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="cell cell-1">cell 1</div>
      <div class="cell cell-2">cell 2</div>
      <div class="cell cell-3">cell 3</div>
      <div class="cell cell-4">cell 4</div>
      <div class="cell cell-5">cell 5</div>
      <div class="cell cell-6">cell 6</div>
    </div>
  </body>
</html>

```

---

- In styles.css

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  color: #222;
}
.container {
  border: 5px solid black;
}
.cell {
  padding: 2rem;
  background: #dedede;
  text-transform: uppercase;
  font-weight: bold;
  text-align: center;
  border: 3px solid red;
  color: #fff;
}
.cell-1 {
  background: #581f18;
}
.cell-2 {
  background: #f0a202;
}
.cell-3 {
  background: #d95d39;
}
.cell-4 {
  background: #202c59;
}
.cell-5 {
  background: #51cb20;
}
```

<br>

### 317. Order Property<a id="317"></a>

> **_Business Objective: Layout_**

<img src="notes/13-order-property.png" width="900">

---

- In index.html

```html

```

---

- In styles.css

```css

```

<br>

### 318. Repeat Function<a id="318"></a>

> **_Business Objective: Layout_**

<img src="notes/14-repeat-function.png" width="900">

---

- In index.html

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Grid Tutorial</title>
    <link rel="stylesheet" href="styles.css" />
    <style>
      /* order  */
      .container {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        grid-template-rows: 100px 100px;
      }
      .cell-1 {
        order: 2;
      }
      .cell-6 {
        order: -1;
      }
      .cell-5 {
        order: 3;
      }
      .cell-3 {
        order: 4;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="cell cell-1">cell 1</div>
      <div class="cell cell-2">cell 2</div>
      <div class="cell cell-3">cell 3</div>
      <div class="cell cell-4">cell 4</div>
      <div class="cell cell-5">cell 5</div>
      <div class="cell cell-6">cell 6</div>
    </div>
  </body>
</html>
```

---

- In areas.html

```js

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <link rel="stylesheet" href="styles.css" />
    <title>Document</title>
    <style>
      .container {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        grid-template-rows: 100px 100px 100px 100px 100px;
        grid-template-areas:
          "a a b"
          "a a b"
          "c c b"
          "d d d"
          "e f f";
      }
      .cell-1 {
        grid-area: a;
      }
      .cell-2 {
        grid-area: b;
      }
      .cell-3 {
        grid-area: c;
      }
      .cell-4 {
        grid-area: d;
      }
      .cell-5 {
        grid-area: e;
      }
      .cell-6 {
        grid-area: f;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="cell cell-1">cell 1</div>
      <div class="cell cell-2">cell 2</div>
      <div class="cell cell-3">cell 3</div>
      <div class="cell cell-4">cell 4</div>
      <div class="cell cell-5">cell 5</div>
      <div class="cell cell-6">cell 6</div>
    </div>
  </body>
</html>

```

---

- In styles.css

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  color: #222;
}
.container {
  border: 5px solid black;
}
.cell {
  padding: 2rem;
  background: #dedede;
  text-transform: uppercase;
  font-weight: bold;
  text-align: center;
  border: 3px solid red;
  color: #fff;
}
.cell-1 {
  background: #581f18;
}
.cell-2 {
  background: #f0a202;
}
.cell-3 {
  background: #d95d39;
}
.cell-4 {
  background: #202c59;
}
.cell-5 {
  background: #51cb20;
}
```

<br>

### 319. justify-content<a id="319"></a>

> **_Business Objective: Layout_**

<img src="notes/app.png" width="900">

---

- In index.html

```html

```

---

- In styles.css

```css

```

<br>

### 320. align-content<a id="320"></a>

> **_Business Objective: Layout_**

<img src="notes/app.png" width="900">

---

- In index.html

```html

```

---

- In styles.css

```css

```

<br>

### 321. align-items, jusitfy-items, align-self,justify-self<a id="321"></a>

> **_Business Objective: Layout_**

<img src="notes/16-item-content.png" width="900">

---

- In index.html

```html

```

---

- In styles.css

```css

```

<br>

### 322. minmax()<a id="322"></a>

> **_Business Objective: Layout_**

<img src="notes/17-minmax.png" width="900">

---

- In index.html

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Grid Tutorial</title>
    <link rel="stylesheet" href="styles.css" />
    <style>
      /* minmax()*/
      .container {
        min-height: 100vh;
        display: grid;
        grid-template-columns: 1fr minmax(400px, 1fr) 1fr;
        grid-template-rows: repeat(2, 1fr);
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="cell cell-1">cell 1</div>
      <div class="cell cell-2">cell 2</div>
      <div class="cell cell-3">cell 3</div>
      <div class="cell cell-4">cell 4</div>
      <div class="cell cell-5">cell 5</div>
      <div class="cell cell-6">cell 6</div>
    </div>
  </body>
</html>
```

---

- In areas.html

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <link rel="stylesheet" href="styles.css" />
    <title>Document</title>
    <style>
      .container {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        grid-template-rows: 100px 100px 100px 100px 100px;
        grid-template-areas:
          "a a b"
          "a a b"
          "c c b"
          "d d d"
          "e f f";
      }
      .cell-1 {
        grid-area: a;
      }
      .cell-2 {
        grid-area: b;
      }
      .cell-3 {
        grid-area: c;
      }
      .cell-4 {
        grid-area: d;
      }
      .cell-5 {
        grid-area: e;
      }
      .cell-6 {
        grid-area: f;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="cell cell-1">cell 1</div>
      <div class="cell cell-2">cell 2</div>
      <div class="cell cell-3">cell 3</div>
      <div class="cell cell-4">cell 4</div>
      <div class="cell cell-5">cell 5</div>
      <div class="cell cell-6">cell 6</div>
    </div>
  </body>
</html>
```

---

- In styles.css

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  color: #222;
}
.container {
  border: 5px solid black;
}
.cell {
  padding: 2rem;
  background: #dedede;
  text-transform: uppercase;
  font-weight: bold;
  text-align: center;
  border: 3px solid red;
  color: #fff;
}
.cell-1 {
  background: #581f18;
}
.cell-2 {
  background: #f0a202;
}
.cell-3 {
  background: #d95d39;
}
.cell-4 {
  background: #202c59;
}
.cell-5 {
  background: #51cb20;
}
```

<br>

### 323. auto-fit and auto-fill<a id="323"></a>

> **_Business Objective: Layout_**

<img src="notes/18-auto-fit-auto-fill.png" width="900">

---

- In index.html

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <link rel="stylesheet" href="styles.css" />
    <title>Document</title>
    <style>
      .container {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        grid-template-rows: 100px 100px 100px 100px 100px;
        grid-template-areas:
          "a a b"
          "a a b"
          "c c b"
          "d d d"
          "e f f";
      }
      .cell-1 {
        grid-area: a;
      }
      .cell-2 {
        grid-area: b;
      }
      .cell-3 {
        grid-area: c;
      }
      .cell-4 {
        grid-area: d;
      }
      .cell-5 {
        grid-area: e;
      }
      .cell-6 {
        grid-area: f;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="cell cell-1">cell 1</div>
      <div class="cell cell-2">cell 2</div>
      <div class="cell cell-3">cell 3</div>
      <div class="cell cell-4">cell 4</div>
      <div class="cell cell-5">cell 5</div>
      <div class="cell cell-6">cell 6</div>
    </div>
  </body>
</html>
```

---

- In areas.html

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <link rel="stylesheet" href="styles.css" />
    <title>Document</title>
    <style>
      .container {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        grid-template-rows: 100px 100px 100px 100px 100px;
        grid-template-areas:
          "a a b"
          "a a b"
          "c c b"
          "d d d"
          "e f f";
      }
      .cell-1 {
        grid-area: a;
      }
      .cell-2 {
        grid-area: b;
      }
      .cell-3 {
        grid-area: c;
      }
      .cell-4 {
        grid-area: d;
      }
      .cell-5 {
        grid-area: e;
      }
      .cell-6 {
        grid-area: f;
      }
    </style>
  </head>
  <body>
    <div class="container">
      <div class="cell cell-1">cell 1</div>
      <div class="cell cell-2">cell 2</div>
      <div class="cell cell-3">cell 3</div>
      <div class="cell cell-4">cell 4</div>
      <div class="cell cell-5">cell 5</div>
      <div class="cell cell-6">cell 6</div>
    </div>
  </body>
</html>
```

---

- In styles.css

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  color: #222;
}
.container {
  border: 5px solid black;
}
.cell {
  padding: 2rem;
  background: #dedede;
  text-transform: uppercase;
  font-weight: bold;
  text-align: center;
  border: 3px solid red;
  color: #fff;
}
.cell-1 {
  background: #581f18;
}
.cell-2 {
  background: #f0a202;
}
.cell-3 {
  background: #d95d39;
}
.cell-4 {
  background: #202c59;
}
.cell-5 {
  background: #51cb20;
}
```

<br>
