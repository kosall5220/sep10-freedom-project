# Entry 4
##### 2/12/24

### Context
I finsihed brainstorming the content for my website, I now have to decide on what tools to use for my website.

---

### Planning
The 4th step of the Engineering Design Process (EDP) is planning. If I want to make my website look as good as possible, I have to figure out which tools to use. After looking through the [list of tools](https://docs.google.com/document/d/1rk-z-5FvFE3qHRHJ9q609wqwi3cQ9AKDW4H-CPG3WYA/edit) I could use, I planned on using these three tools for my project:


* ### [A-Frame](https://aframe.io/)
    **A-Frame** is a web framework that allows web designers to make 3D scenes using HTML. I chose to use A-Frame in my website because I want to make it easier for people to visualize my ideas. I tinkered with Aframe by first copy and pasting code from [aframe.io](https://aframe.io/docs/1.5.0/introduction/) into a [repl(code)](https://replit.com/@kosallour/test-aframe) on replit and then moving the shapes around in an attempt to create a face. If I ever decide to not use Aframe or if it gets too complicated I will use [CSS flexbox](https://www.w3schools.com/css/css3_flexbox.asp) as my backup.

    [My A-frame repl](https://1021ffaf-62a1-4a78-816e-7a9967fa92c5-00-3ocmxt0o8r26t.riker.replit.dev/)

    ![Alt text](<Screenshot 2024-02-25 023327.png>)

* ### [AnimateCSS](https://animate.style/)
    **Animate.css** is a library of animations that you can use on your web projects. For my website, I plan on having animations for my text as you scroll, this will hopefully make my website more appealing to viewers. I tinkered with Animate.css by making my heading bounce up when you open the page. Here is the code that I used to create this animation:

    ```html
   <head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width">
  <title>replit</title>
  <link href="style.css" rel="stylesheet" type="text/css" />
  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.1.1/animate.min.css"
  />
    </head>

    <body>

     <h1 class="animate__animated animate__bounce">An animated element</h1>

    </body>
    ```
    If I decide to not use Animate.css, my backup will be [WowJS](https://wowjs.uk/) since they are very similar.


* ### [SASS](https://sass-lang.com/)
    **SASS (Syntactically Awesome Style Sheets)** is a CSS preprocessor that reduces the repetition of CSS. I used SASS to make variables for different colors and it seems like it would save me a lot of time since I wouldn’t have to keep typing the values of the colors every time.  If SASS doesn’t work out, my backup will be to use [CSS variables](https://www.w3schools.com/css/css3_variables.asp).

    My SASS code:
    ```SCSS
    $bluebg: darkblue;
    $purpletext: purple;
    $smallfont: 10px;

    body {
      background-color: $bluebg;
      color: $purpletext;
     font-size: $smallfont;
    }
    ```

---
### Skills
The skills that I learned while planning were **how to learn**, and **embracing failure**.

 #### How to learn
For my project I have to use new tools that I’m unfamiliar with, so I have to learn how to use them. Instead of just watching a video or reading a website about each tool, I tinkered and tested them out. I also followed guides on how to use each tool, but I still haven’t mastered them yet. Having the skill to learn effectively will help me fully understand A-Frame, AnimateCSS, and SASS, and it will help me learn about other things in the future.

 #### Embracing failure



[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
