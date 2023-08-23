# Understanding_Grid

 
```
display: grid;
```

setting parent element as display grid denotes parent element is a grid container and all child element will be alocated as grid system


grid-template-columns denotes the size and distribution of columns and rows under a grid
for example if i set 

```
grid-template-columns: 700px 700px;
```

it will creates 2 columns each having size 700px

```
grid-template-rows: 50px auto 50px;
```

it will creates 3 rows having first and last rows size of 50px 
and the middle rows will allocate automatically the remaining size available
if all element cant be arranged in 3 rows or exceed 3 rows - it will arrange the rows except 1st and 3rd in the middle automatically

```
grid-template-columns: repeat(2, 1fr);
```

it will create 2 rows , and divide the column area into 2 section and allocate each having same size 

```
grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
```
 
we use auto fit rpoperties , when we want to distribute the area auto, and minmax property set minimum size 100px and max size to the remaining fraction available

```
grid-column: auto / span 2;
```

same can be written as 

```
grid-column: span 2;
grid-row: auto/span 2

```

the elloborated version of the upper code is grid-column-start: auto and grid-cxolumn-end:span 2
it denotes where the column should be start and end, auto peorperties set the element automatically in the next column available 



```
grid-area: a;
```   
```
grid-template-areas:
    "a a a a a a a a a a a a"
    "b b c c c c c c c c d d"
    "e e e e f f f g g g g g"; */
```
   we uses this property , to hardcodedly arrange elements


```
grid-gap: 5px;
```

 gap between grids


```
.container img {
  height: 100%;
  width: 100%;
  /* margin: 10px; */
  object-fit: cover;
}
object-fit: cover;
```

it helps to fit the object by resizing the element covering the content area maintaining aspect ratio

```
grid-auto-flow: dense;
```

it automatically place the item into available area even if not maintaining the order they are arranged into code
 

# UNderstandingof FlexBox

```
display : flex;
```
This will set the child elements into a flex box 

## flexBox width by default adjust the viewport's width, putting some styles may overflow the child elements oveer the width of viewport (Soln- BY putting row wrap attribute solves this problem. For Example : )

```
flex-flow: row wrap

```
*this problem are not shown in column order*

There are 2 axis in flex, Main Axis(horizontal order ->-->-->) and cross axis (vertical order)

By default , elements are arranged in horizontally i.e 
```
flex-direction: row
```
 are set
```
flex-direction:column
```
here elements are arranged in Vertically

**justify-content should be applied over child but written inside parent**

