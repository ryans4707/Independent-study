# Entry 4:  Loops 
 
Loops are just more complex functions. There are both Each and For loops.

The Each Loop is used by starting off with `@each` and then based on a list o that
is already created, the loop works based off of that. For example:
```css
$list: (orange, purple, teal);

@each $item in $list { 
  .#{$item} {
    background: $item;
  }
}
```



Based on this, for each item in the list, the loop will go through and add the color
of each item to the background of each specific item.

The For loops are used to style different elements. The way you start a for loop is by
typing `@for` and then from there you can start your loop.

```css
@for $i from $begin through $end {
   
}
```
For this, `$i` is just a variable for the index, or position of the element 
in the list. `$begin` and `$end` are placeholders for the start and end points 
of the loop.The keywords `through` and `to` are interchangeable in Sass.

# Takeaways

Actually trying out different things on your own is a great way to better understand
 what you are learning.




