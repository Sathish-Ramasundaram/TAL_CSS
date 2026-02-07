1. create index.html

type nul > index.html

```

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>CSS Dashboard</title>
  <link rel="stylesheet" href="style.css" />
</head>

<body>

  <header class="header">
    Dashboard Header
  </header>

  <div class="layout">

    <aside class="sidebar">
      Sidebar
    </aside>

    <main class="main">
      Main Content

      <div class="cards">
        <div class="card">Card 1</div>
        <div class="card">Card 2</div>
        <div class="card">Card 3</div>
        <div class="card">Card 4</div>
      </div>

    </main>

  </div>

</body>
</html>

```

2. 
Box Model + Basic Styling

Tiny goal: 
Add spacing, borders, background, and readable layout blocks

You will learn:
margin vs padding
borders
background colors
box sizing

Note: 
Box-Sizing and the Box Model
Default (content-box) → width/height apply only to content; padding and border add extra size.
border-box → width/height include content + padding + border; element stays fixed at the size you set.

3. create style.css

type nul > style.css

```

/* Reset + box model rule */
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  font-family: Arial, sans-serif;
}

/* Header */
.header {
  background: #1f2937;
  color: white;
  padding: 20px;
  font-size: 24px;
}

/* Layout wrapper */
.layout {
  border: 2px solid #ddd;
  margin: 20px;
}

/* Sidebar */
.sidebar {
  background: #e5e7eb;
  padding: 20px;
  border: 1px solid #ccc;
}

/* Main content */
.main {
  padding: 20px;
  border: 1px solid #ccc;
}

/* Cards */
.cards {
  margin-top: 20px;
}

.card {
  border: 1px solid #bbb;
  padding: 16px;
  margin-bottom: 12px;
  background: white;
}

```

Margin - Space between elements. outside the box
Padding - space between Content and border space. inside the box
Border - Outer box line

- Test

box-sizing: border-box;

By default (content-box) → the width and height apply only to the content area. Padding and border are added outside, so the element grows bigger than the size you set.

With border-box → the width and height apply to the entire box (content + padding + border). The content area shrinks to fit, so the element stays exactly the size you set.

For example: 

```

<!DOCTYPE html>
<html>
<head>
  <style>
    /* Default: content-box */
    .content-box {
      width: 200px;
      padding: 20px;
      border: 5px solid red;
      box-sizing: content-box; /* default */
      background-color: lightyellow;
      margin: 10px;
    }

    /* With border-box */
    .border-box {
      width: 200px;
      padding: 20px;
      border: 5px solid blue;
      box-sizing: border-box;
      background-color: lightcyan;
      margin: 10px;
    }
  </style>
</head>
<body>
  <div class="content-box">Content-box (default)
    Content-box (default)
    Content-box (default)
    Content-box (default)
    Content-box (default)
    Content-box (default)
    Content-box (default)
    Content-box (default)
  </div>
  <div class="border-box">Border-box
    Border-box
    Border-box
    Border-box
    Border-box
    Border-box
  </div>
</body>
</html>

```

---

px stands for CSS pixel, not necessarily the tiny dot on your screen.

div { width: 100px; height: 100px; background: lightblue; }
This creates a square that is 100 CSS pixels wide and tall.
On a standard screen, it looks like 100 physical pixels.
On a Retina screen, the browser uses more hardware pixels to render it, but visually it’s still the same size.

px is a fixed unit → good for precise control (like borders, icons).
Relative units (%, em, rem, vh, vw) → better for responsive design.

Example difference:
width: 200px; → always 200 CSS pixels wide.
width: 50%; → adjusts based on parent width.