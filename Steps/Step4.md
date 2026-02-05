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

4. CSS Positioning — relative vs absolute

position controls how an element is placed on the page and what it is positioned relative to.

Main values:

position: static  (default) - No Movement allowed
position: relative
position: absolute
position: fixed
position: sticky


position: relative
- The element stays in normal layout
- BUT you can move it slightly from its original spot.

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

- The element is removed from normal layout
- It floats and is positioned using top/left/right/bottom.

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


6. position: fixed
Fixed = stick to the screen, not the page
It ignores scrolling
It stays at same screen position always

7. update your header

.header {
  background: #1f2937;
  color: white;
  padding: 20px;
  font-size: 24px;

  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
}

8. Add spacing because fixed removes layout space
Since fixed elements don’t keep their original space, your content will slide under the header.
So add margin to layout:

.layout {
  border: 2px solid #ddd;
  margin: 20px;
  display: flex;
  margin-top: 100px; /* add this */
}

margin-top: 100px; /* add this */
To push elements down from the top of the page or from other elements.

9. Test: 

Tricky part. Cart will go over the header. 
Why? CSS does this:

👉 Removes the header from normal layout flow
👉 It no longer occupies vertical space
👉 Other elements behave like the header is NOT there

Add z-index (best practice)

Fixed elements should usually sit above content.

.header {
  z-index: 1000;
}

Note: if you put z-index: 2000 in card, then card will go over again. 

