# Grid Layout Guide

In order for the grid to work, follow these rules for optimal layout.

### Properties

* For `item-count`: The total amount of page entries listed in this file.

  Why: This helps all existing items have uniform styling when viewed on mobile.

  Too many, and there will be extra empty space after the last item. Too few, and items starting from the last item won't get the uniform size styling as every other item.

* For `columns-for-items`: The number of columns you want. Usually 3. If too few existing items, then less than 3.

  Why: Number of colums depends on how you want to arrange the items. Too few items might not look good when arranged in a 3-column grid.

* For `rows-for-items`: Divide `item-count` by `columns-for-items`. Then ceiling the quotient.

  Mathematical expression: ceil(`item-count` / `columns-for-items`)

  Why: This neatly fits all items on a `columns-for-items`-grid for desktop without a lot of leftover space *and* items overflowing outside of the grid and viewport.
 
  If you want the items aligned in a checkerboard-like pattern or not, decide between adding 1 to the ceiling or just sticking to the ceiling. Adding 1 will leave more empty space in the third column, however.
 
  There is no ceiling function in CSS, so finding the ceiling for the rows has to be done manually.

### Explanation

The properties `item-count`, `columns-for-items`, and `rows-for-items` are referenced in the corresponding layouts page in /_layouts/ in the \<style\> tag. Their values are then used in styles-grid.css to give the grid the optimal values to fit and style the items neatly for mobile and desktop view via CSS variables.

While in a grid-items file adding more items, you can also update those three properties at the same time for convenience. It also cuts down on file navigation, since the focus is on your content and not wrangling so much with other files.