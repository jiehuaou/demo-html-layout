# demo html layout

## Grid, 3 columns
```css
display: grid;
grid-template-columns: 1fr min(65ch, 100%) 1fr;
gap: 10px;  
```

## Grid fit vs fill
```css
.fit-cards {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
}
.fill-cards {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
}
```

`auto-fit`
CURRENTLY columns try to take up as many space as possible. the content will stretch to fill the entire row width.

`auto-fill`
Grid try to create as many columns as it can. browser will allow empty columns to occupy space in the row.

## Grid Responsive
```css
@media (min-width: 600px) {
    .cards {
        grid-template-columns: repeat(2, 1fr);
    }
}
@media (min-width: 900px) {
    .cards {
        grid-template-columns: repeat(3, 1fr);
    }
}
```
* when media width < 600px, only one column is shown.
* when media width in 600px~900px, two columns are shown.
* when media width > 900px, three columns are shown.

## Flex Item

 In the Flexbox algorithm, child width/height is more of a suggestion.
