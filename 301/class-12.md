# EJS Partials

Partials come in handy when you want to reuse the same HTML across multiple pages. Embedded JS can be used to template the reusable code. 

```js
<section>
  <ul>
    <li class="book-item" data-id="<%=book.id %>">
      <img src="<%= book.image_url %>" alt="<%= book.title %>" style="max-height: 400px; width: 300px;">
      <h2>Title:  <%= book.title %></h2>
      <h4>Author:  <%= book.author %></h4>
      <h5>ISBN:  <%= book.isbn %></h5>
      <p>Description:  <%= book.description %></p>
      <p>Bookshelf:  <%= book.bookshelf %></p>
    </li>
  </ul>
</section>
```
The page above `detail.ejs` includes multiple templates to copy into. You can also use the page as a template.

```js
<%- include('detail.ejs') %>
```

This allows you to call the same template across pages.

```js
require('ejs');
app.set('view engine', 'ejs');

response.status(200).render('pages/books/show', {book: theChosenBook});
```
This code will get you started in your server file. Don't forget to install the ejs package! `npm install ejs`.
