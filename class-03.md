# Class-03

## HTML Lists, CSS Boxes, and JS Control Flow

### HTML Lists

```html
<ol>
  
  <li></li>
  <li></li>
  <li></li>
  
</ol>
```
```html
<ul>
  
  <li></li>
  <li></li>
  <li></li>
  
</ul>
```

There are three different types of ***Lists*** in HTML. ***Ordered Lists*** with the **\<ol>** tag, ***Unordered Lists*** with the **\<ul>** tag, and the ***Definition Lists*** marked with the **\<dl>** tag. Each list uses the ***item*** tag marked **\<li>** to list items within the list. ***Ordered Lists*** will display in numbers while ***Unordered Lists*** will display in bullets.

```html
<dl>
  
  <dt>
    <dd></dd>
  </dt>
  <dt>
    <dd></dd>
  </dt>
  <dt>
    <dd></dd>
  </dt>
  
</dl>
```

***Definition Lists*** contain two different lists items called the **\<dt>** tag or ***term*** tag which gives the term within the list, and the **\<dd>** tag or ***definition*** tag whcih is used to define the term.

### CSS Box Model
![Box model](box-model.png) 
> https://www.rithmschool.com/courses/html-css-fundamentals/box-model
CSS follows the box model for all of its styling. Each section of code is contained within the box. The image above shows which term affects which part of the box.

### JS Control Flow
Comparison and Logical Operators help evaluate variables. 
```javascript
< less than
> greater than
```

Conditional statements help you code decisions into your program and assist in functioning approriately. The different types of decision making statements are ***If/Else*** statements, and ***Switch*** statements.
```javascript
if (blue == blue)
{
  alert("It is blue!");
 }
else
  alert("Is not blue!");
```
