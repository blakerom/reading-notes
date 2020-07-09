# 04 CSS Grid
Grid allows true 2D formatting with rows and columns.
To initiate a grid you use the `<display>` tag.

```css
.container {
  display: grid | inline-grid;
}
```
Initiate the rows and columns giving them a size.

```css
.container {
  grid-template-columns:  100px 100px 100px;
  grid-template-rows:  100px 100px 100px;
}
```

This sets the size and amount of rows and lengths. The sizes can vary within the rows and columns.

Set the gap in between the grids for better visuals.

```CSS
.container {
  grid-template-columns: 100px 50px 100px;
  grid-template-rows: 80px auto 80px; 
  column-gap: 10px;
  row-gap: 15px;
}
```
You can justify items within the containers using...

```css
.item-a {
  justify-self: center;
}
```
