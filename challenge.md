# Introduction to DOM - Exercises

1. Answer the following questions:

   - How would you select from JavaScript an element `p` that has the class `text` and also the class `important`?
   ```javascript
   const textImportant = document.querySelector("p.text.important");
   console.log(textImportant);
  ```
   - How would you select from JavaScript a `button` element with class `button` and that is disabled?
    ```javascript
   const btnDisabled = document.querySelector("button.button:disabled");
   console.log(btnDisabled);
    ```

   - How would you select from JavaScript all the `li` elements that are direct children of an `ul` element with class `list`?
    ```javascript
   const listItem = document.querySelectorAll("ul.list > li");
   console.log(listItem);
   ```

   - How would you select from JavaScript all the `input` elements that are descendants of a `form` element with class `form-new-item`, and that have a `type` attribute with a value `text`?
   ```js
   const textInputElement = document.querySelectorAll('form.form-new-item input[type="text"]');
   console.log(textInputElement);

   ```

2. From the following HTML structure, create a script that selects the header "The MEAN stack". Next, change the text to "The MERN stack" and remove the "subtitle" class.

```html
<main class="main-content">
  <h1 class="app-title">Bootcamp technologies</h1>
  <section class="info">
    <h2 class="subtitle">The MEAN stack</h2>
    <p class="text">
      The MEAN stack is the set of technologies used in the bootcamp by
      FullStack Web Development.
    </p>
  </section>

  <script>
  const currentHeader = document.querySelector(".subtitle");

  if(currentHeader.textContent=="the MEAN stack"){
    currentHeader.textContent = "the MERN stack";
    currentHeader.classList.remove('.subtitle');
      
  }
  </script>

</main>
```

3. Here you have an HTML without data:

```html
<article class="student">
  <h2 class="student-name"></h2>
  <span class="student-age"></span> years
  <img class="student-photo" src="" alt="" />
  
  <script>
  var studentName= "Laura";
  var studentAge = 27;
  var studentPhotoURL= "foto.jpg";
  document.querySelector('.student-name').textContent = name;
  document.querySelector('.student-age').textContent = age;
  document.querySelector('.student-photo').src = photoURL;


  </script>
</article>
```

Create a script where you declare a variable with a student's data
(name, age and photo URL). Next, get the elements from the HTML
and fill them in with the student's information.