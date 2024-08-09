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
