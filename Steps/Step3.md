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

14. Replace the grid line with this: ----------------------------------------------
grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));

auto-fit
Instead of a fixed number, the browser automatically fits as many columns as possible into the available space.
If there’s extra space, columns stretch to fill it.
If space is tight, fewer columns are shown.

minmax(180px, 1fr)
Defines the minimum and maximum width of each column.
180px → column can’t shrink smaller than 180px.
1fr → column can grow to take up available free space (fractional unit).


15. Test:

Expected behavior
Cards automatically wrap
Column count changes with width
No media query needed yet