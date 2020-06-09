# JS Objects and the DOM

In Javascript you can maniuplate HTML using the Document Object Model or DOM. By using ***objects*** and ***methods*** you can create an organized document model for any object with *properties*.

```js
var potato = {
  name : 'Russett',
  weightInKilograms : 15,
  ageInDays : 2,
  color : 'brown',
  };
```

Above is an example of an object with its properties. Along with properties you can implement methods to maniuplate the data around the objects.

```js
var potato = {
  name : 'Russett',
  weightInKilograms : 15,
  ageInDays : 2,
  color : 'brown',
  potatoDescription : function() {
    document.write(this.name + ' potatos weight approximately ' + this.weightInKilograms + ' and are ' + this.color + ' in color when they are just ' + this.ageInDays + ' days old.');
  }
  };
```

You call this object with `potato.potatoDescription();`.


```js
var potato = getElementById('potato-attribute'); 
```
Here is an example of Using getElementById() built in method to target an attribute with the "potato-attribute".

```js
var displayPotatoDescription = document.createElement('');
displayPotatoDescription.textContent = this.potatoDescription;
elementIdName.appendChild(displayPotatoDescription);
```
In order to create text in your HTML document you need to first identify your ID. Create an element `var displayPotatoDescription = document.createElement('');`. Choose the textContent to replace `displayPotatoDescription.textContent = this.potatoDescription;`. Finally append to the HTML document `elementIdName.appendChild(displayPotatoDescription);`.
