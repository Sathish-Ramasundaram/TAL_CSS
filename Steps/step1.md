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

