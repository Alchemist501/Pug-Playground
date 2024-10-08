# Pug Templating Basics

This repository contains all the Pug (templating language) code examples and projects I worked on while following the "Pug Templating" playlist by Richard Stibbard Web Development Tutorials on YouTube.

## Learning Points

1. **Pug Syntax**: Learned the clean and minimal syntax of Pug, which is quite different from HTML.
2. **Variables and Mixins**: Mastered how to use variables and create reusable components with mixins.
3. **Conditionals and Loops**: Explored how to add logic using conditionals and loops within Pug templates.
4. **Inheritance**: Understood template inheritance and how to create a base template to be extended by other templates.
5. **Filters and Includes**: Learned how to include partial templates and use filters for text processing.
6. **Form Handling**: Practiced creating and handling forms in Pug, including dynamic form fields.

## How to Use

Clone the repository and navigate through the different folders to see examples of Pug code. Each folder corresponds to a video or concept from the playlist.

## Resources

- [Richard Stibbard Web Development Tutorials](https://www.youtube.com/playlist?list=PLz_6dB4PItBEYHIDnXPUI81pTQ_71eEqS)- YouTube Channel
- [Pug Documentation](https://pugjs.org/api/getting-started.html) - Official Pug Documentation

## Key Points to Ponder

- For multiline sentences in any tag, use . or | to keep the text formatting consistent.<br>

        h1
            |Hello
            |Everyone

  OR

      h1.
          Hello
          Everyone

- Adding a div element: To add a div element, simply use . followed by the class name and # followed by the id. For example: `.className#idName` creates `<div class="className" id="idName"></div>`.

- Adding a Link: To add a link, use the a() tag followed by the text.
  Example: `a(href="https://example.com") Click here` creates `<a href="https://example.com">Click here</a>`.

- Linking a Stylesheet: To link a stylesheet, use the `link()` tag with attributes as parameters.
  Example: `link(rel="stylesheet", href="styles.css")` creates `<link rel="stylesheet" href="styles.css">`.

- Adding 2 classes for the same element : Use . between the classes.
  Example: `section.section-grid.section1` creates `<section class = "section-grid section1">`.

- Emmet Abbreviations :

  - To create child elements use '>' symbol.<br>
    Example : `main.main>.div1>.div2>ul>li` creates

          main.main
            .div1
              .div2
                ul
                  li

    which is equal to html code :

        <main class="main">
          <div class="div1">
            <div class="div2">
              <ul>
                <li> </li>
              </ul>
            </div>
          </div>
        </main>

  - To create siblings element : Use '+' operator<br>
    Example : `aside.asideContent+main#main+aside` creates

        aside.asideContent
          main#main
          aside

    which is equal to the html code :

        <aside class="asideContent"> </aside>
            <main id="main"> </main>
            <aside> </aside>

  - To create more than 1 number of same type of element use '\*' operator<br>
    Example : `main.main>(ul#ul-Content>li*5)+ul.ul-Content>li*4` creates

        main.main
                ul#ul-Content
                    li
                    li
                    li
                    li
                    li
                ul.ul-Content
                    li
                    li
                    li
                    li

        <main class="main">
          <ul id="ul-Content">
            <li> </li>
            <li> </li>
            <li> </li>
            <li> </li>
            <li> </li>
          </ul>
          <ul class="ul-Content">
            <li> </li>
            <li> </li>
            <li> </li>
            <li> </li>
          </ul>
        </main>

  - To link the stylesheet : Use `link:css` which creates `
link(rel="stylesheet", href="style.css")`
  - `meta:vp` creates `meta(name="viewport", content="width=device-width, initial-scale=1.0")`

- Include another pug file in main file use `include filename.pug`<br> Example :=

      //footer.pug
      footer
        p © 2020 Acme Cleaning Services Ltd

      //To include it in index file
      body
        include footer

- Template Inheritance : works via the `block` and `extends` keywords.

      //- layout.pug
      html
        head
          title My Site - #{title}
        body
          block content
          block foot
            #footer
              p some footer content

      //- page-a.pug
      extends layout.pug
      block content
        h1= title
        - var pets = ['cat', 'dog']
        each petName in pets
          include pet.pug

  > It’s also possible to override a block to provide additional blocks, as shown in the following example. As it shows, content now exposes a sidebar and primary block for overriding. (Alternatively, the child template could override content altogether.)

- JS variables : To show value inside variable we can use several methods

      -let language = "Pug"
      p #{language}
      p= language //Buffered Code

      // HTML CODE
      <p>Pug</p>
      <p>Pug</p>

- Concatenation : We can create new strings with variables and text

        p= "Language used is "+language
        p= `Language used is ${language}`

        <p>Language used is Pug</p>
        <p>Language used is Pug</p>

- Iteration using `each` :The `each` keyword is used to define loops that iterate over data in templates. The each keyword is followed by the data to be iterated over.

  Example :

      - let names = ['Caraxes','Cannibel','Sunfyre']

      ol
        each name in names
          li= name

      //-Html code =>
      <ol>
        <li>Caraxes</li>
        <li>Cannibel</li>
        <li>Sunfyre</li>
      </ol>

- Mixins := Allows you to create reusable blocks of Pug.

      //- Declaration
      mixin list
        ul
          li foo
          li bar
          li baz
      //- Use
      +list
      +list
      //- Html
      <ul>
        <li>foo</li>
        <li>bar</li>
        <li>baz</li>
      </ul>
      <ul>
        <li>foo</li>
        <li>bar</li>
        <li>baz</li>
      </ul>

# MiniProject

## [Lovely Cars Of YesterYear](https://github.com/Alchemist501/CarsOfLovelyYear-Pug)

![image](image.png)
A static website built with Pug templates, showcasing a collection of cars from various years. Inspired by Richard Stibbard's "Pug Templating" tutorial, this project demonstrates the power and flexibility of Pug for creating dynamic and maintainable web pages.
