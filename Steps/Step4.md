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

4. CSS Positioning — relative vs absolute

position controls how an element is placed on the page and what it is positioned relative to.

Main values:

position: static  (default)
position: relative
position: absolute
position: fixed
position: sticky



position: relative
✅ Meaning (simple words)

The element stays in normal layout
BUT you can move it slightly from its original spot.

It still keeps its original space.

Example: 

.card {
  position: relative;
  top: 10px;
  left: 20px;
}


Result:

Card moves down 10px
Moves right 20px

But its original space is still reserved

Think:

👉 “Move me a bit — but I still belong here”


position: absolute
✅ Meaning (simple words)

The element is removed from normal layout
It floats and is positioned using top/left/right/bottom.

It does NOT keep its original space.

Example: 

.card {
  position: absolute;
  top: 10px;
  right: 10px;
}



Now the card:

Floats

Other elements ignore it

Positioned exactly by coordinates

Think:

👉 “Take me out — I will float exactly here”

5. Let’s apply this to your dashboard cards.

Goal:

Show a small red badge on a card corner.

Make card relative: 

.card {
  position: relative;
}

Why?

👉 So absolute children use the card as reference.

Add badge HTML
Inside one card:

<div class="card">
  Card 1
  <span class="badge">New</span>
</div>

Badge CSS (absolute)

.badge {
  position: absolute;
  top: 8px;
  right: 8px;
  background: red;
  color: white;
  padding: 4px 8px;
  font-size: 12px;
}


Result
Badge sticks to card corner
Moves with the card
Does not affect layout

Because:
.card → relative
.badge → absolute

This is the most common real-world usage.


position: relative
I stay in the line
but can shift slightly

position: absolute
I float freely
anchored to nearest relative parent


⚠️ Common Beginner Mistake

Using absolute without setting parent to relative.
Then element jumps to page corner — confusing 😄


6. 
7. 
8. 
9. 
10. 
11. 
12. 
13. 
14. 
15. 
16. 
17. 
18. 
19. 
20. 
21. 
22. 
23. 
24.  
25. 
26. 
27. 
28. 
29. 
30. 
31. 
32. 
33. 
34. 
35. 
36. 
37. 
38. 
39. 
40. 
41. 
42. 
43. 
44. 
45. 
46. 
47. 
48. 
49. 
50.  
51. 
52. 

