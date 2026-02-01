10. Cards Layout with CSS Grid
Tiny Goal: 
Make cards display in a responsive grid
You will learn:
display: grid
columns
gap
auto-fit behavior


11. Update .cards

To: 

.cards {
  margin-top: 20px;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 16px;
}

12. Test: 
Expected result

Cards now appear like:
Card1   Card2
Card3   Card4


13. grid-template-columns: repeat(2, 1fr)
Means:
Make 2 equal columns
Each gets 1 fraction of space

gap: 16px
Spacing between grid items
Much cleaner than margins.

14. Replace the grid line with this:
grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));


15. Test:

Expected behavior
Cards automatically wrap
Column count changes with width
No media query needed yet