# Entry 2: Using Variables,  `&` Selectors and Mixins In SCSS

## Variables
In order to add a variable, you have to start off with `$` in order to define s variable.
After assigning this variable you may use it any where in your code that you want!

## `&`Selector

The `&` character will be used when you know that a parent selector will be used. For example,
<br>
<br>
SCSS
```
.notecard{ 
  &:hover{ 
      @include transform (rotatey(-180deg));  
    }
  } 
  ```
  <br>
  Represents this CSS:
  ```
  .notecard:hover {
  transform: rotatey(-180deg);
}
```

## What are Mixins!?
In SASS ,there are groups of CSS declarations that can be used throughout 
the rest of your code, that are called mixins. The way to use a mixin is to start off
the code with `@mixin` and then after creating your mixin, you can use the name that you 
called it inside other selectors throughout your code. This will prevent you from having to
retype the same groups of code over an over again in your selectors.<br>
An example of this is:<br>
<br>
SASS
```
@mixin backface-visibility {
  backface-visibility: hidden;
  -webkit-backface-visibility: hidden;
  -moz-backface-visibility: hidden;
  -ms-backface-visibility: hidden;
  -o-backface-visibility: hidden;
}

.front, .back {
  width: 100%;
  height: 100%;
  position: absolute;
  @include backface-visibility;
}
```
<br>
CSS 
```
.notecard .front, .notecard .back {
  width: 100%;
  height: 100%;
  position: absolute;

   backface-visibility: hidden;
  -webkit-backface-visibility: hidden; 
  -moz-backface-visibility: hidden;
  -ms-backface-visibility: hidden;
  -o-backface-visibility: hidden;
}
```

Mixins can also take in arguments. For example
```
@mixin transform($transformation) {
  transform: $transformation;
  -webkit-transform: $transformation;
  -moz-transform: $transformation;
  -ms-transform: $transformation;
  -o-transform: $transformation;  
}
```

# Takeaways
1) Stay organized and do not get distracted because anything that 
you miss may be important

2) If you do not understand a specific term, make sure you Google it
 and learn what it means so that you don't go on learning without knowing what 
 that term means.





