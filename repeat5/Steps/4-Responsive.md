1. Responsive Layout (Media Query)

On small screens:
Sidebar moves above main content
Layout becomes vertical
Cards still work

You will learn:
media queries
flex-direction switch
responsive thinking

2. open style.css

paste this at the bottom:

```

/* Responsive — mobile layout */
@media (max-width: 768px) {
  .layout {
    flex-direction: column;
  }

  .sidebar {
    width: 100%;
  }
}

```

(max-width: 768px) → The condition: it targets screens that are 768px wide or smaller.

update index.html
inside head

<meta name="viewport" content="width=device-width, initial-scale=1.0">

3. Test:

Mobile view:

Header
Sidebar
Main
Cards grid
Stacked vertically.

Desktop view:
Header
Sidebar | Main

Side-by-side.
