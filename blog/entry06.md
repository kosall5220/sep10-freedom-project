# Entry 6
##### 5/1/24

### Context

Now that I have finished learning [aframe](https://aframe.io/), I now have to complete the next step in the [Engineering Design Process (EDP)](https://hstatsep.github.io/students/#edp), which is creating a prototype.

### Creating the Website layout

Before I started making the website, I made a layout of it by using [wireframe.cc](https://wireframe.cc). I created two different layouts, one for mobile and one for desktop.

* [Mobile layout](https://wireframe.cc/aMMiUN)
* [Desktop layout](https://wireframe.cc/U17GwI)

### Creating the Minimum Viable Product (MVP)

#### Bootstrap template
For my website I used a bootstrap template. The template I chose was the [“One Page Wonder”](https://startbootstrap.com/theme/one-page-wonder) template because I liked the transparent navbar and the background circles in the header. I also liked how simple it was, and it was a template that I could easily change and add on to.

![alt text](image-2.png)

#### Navbar and Title

Since I already had a transparent navbar and title from the template all I had to do was change the information on the navbar and the color of the title.

![alt text](image-3.png)

#### Carousel

In my layout I wanted to create a slide show for the portable devices.

First I created a `<div>` element with the class `".carousel"` and a unique ID called `"#port"`.

```html
 <div id="port" class="carousel carousel-dark slide" data-bs-ride="false">
```

Then I created the slides. For the each slide I used `class="carousel-item active"`to make a slide. In each slide I put the code:
```html
 <div class="card text-bg-dark mb-5">
    <div class="card-body">
```
This code created a [card](https://getbootstrap.com/docs/5.2/components/card/) inside the carousel. In the card, I put details about each device and an image of it.

This is the code I used for the arrows and indicaters.

```html

<!-- Indicaters -->
  <div class="carousel-indicators">
   <button type="button" data-bs-target="#port" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
  <button type="button" data-bs-target="#port" data-bs-slide-to="1" aria-label="Slide 2"></button>
  <button type="button" data-bs-target="#port" data-bs-slide-to="2" aria-label="Slide 3"></button>
  </div>

  <!-- Arrows -->
 <button class="carousel-control-prev" type="button" data-bs-target="#port" data-bs-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Previous</span>
    </button>
    <button class="carousel-control-next" type="button" data-bs-target="#port" data-bs-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Next</span>
</button>

```
![alt text](image-4.png)

#### Cards
For some sections I used the bootstrap component cards. First I used `<div class="card-group">` to put all the cards in one group with equal width and height columns.

Then to create a card I used this code:
```html
<div class="card text-bg-dark">
    <div class="card-body text-bg-dark">
    <h5 class="card-title"> Title </h5>
    Card content
</div>
```
![alt text](image-5.png)

### Adding my Aframe
To add my aframe to the website I had to use `<iframe>`.

`<iframes>` is an element that loads another HTML page into a different HTML page.

```html
<!-- iframe in my code -->
 <iframe src="tool/fp-aframe.html" title="description" height="100%" width="90%"> </iframe>
 ```

### Challenge (Columns and Bootstrap grids)

Something that was challenging for me was making my website responsive. This was a challenge for me because my website looked fine on larger screen sizes but when I went on a smaller screen some parts of my site would become really tight together. To fix this I used [columns](https://getbootstrap.com/docs/5.2/layout/columns/) and [bootstrap grids](https://getbootstrap.com/docs/5.2/layout/grid/).

For example in my website I wanted to make the future technology ideas side by side when on bigger screens and on top of each other when on smaller screens. I did this by creating `.rows` so I can have equal-width columns. Then I created columns that would take up a specific amound of space on the grid at different [breakpoints](https://getbootstrap.com/docs/5.2/layout/breakpoints/) or screen sizes.

```html
<div class="col-md-6 col-sm-8 col-xs-8">
    content
</div>
```
This means that at medium or bigger screen sizes the columns would take up less space and they would be side by side.
![alt text](image-6.png)

And on smaller screen sizes, the columns would take up more space and they will stack on top of each other.
![alt text](image-7.png)




### Skills

Some of the skills that I learned while creating my MVP was **organization** and **attention to details**.


#### Organization
While completing the MVP I had to do a lot of organization. For example, when I created my wireframes I added labels to show where my content will be and which components to use.

![alt text](image-1.png)

I also organized my code by adding titles to help me know what part of my website it was for.

```html

<!-- Navigation  -->
<nav> code for navbar </nav>

<!-- Header -->
<header> Code for my heading/title </header>

```

#### Attention to detail
Another skill that I learned was attention to detail. When I was making my website I wanted to get rid of any errors or problems that it had. To do this I had to pay attention to all the little things in my code to make sure there weren't any errors. For example, there was one time where my heading wasn’t working.

```html
<!-- code with the errors -->
 <header class="masthead text-center text-white>
          <div class="masthead-content">
              <div class="container px-5">
                  <h1 class="masthead-heading">Mental health Care</h1>

              </div>
          </div>
          <div class="bg-circle-1 bg-circle"></div>
          <div class="bg-circle-2 bg-circle"></div>
          <div class="bg-circle-3 bg-circle"></div>
          <div class="bg-circle-4 bg-circle"></div>
      <header>

```
After analyzing my code I realized that my code wasn’t working because I forgot to put a quotation mark at the end of the class in the `<header>` element. Also, I forgot to put the slash in the `</header>` at the end of the code.

### Takeaways
Creating my MVP has shown me the importance of being organized and observant. Without these skills completing this website will be way more difficult. I am excited to use these skills to complete the next step in completing my project.


[Previous](entry05.md) | [Next](entry07.md)

[Home](../README.md)
