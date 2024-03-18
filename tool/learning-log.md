# Tool Learning Log

Tool: **Aframe**

---

### 2/26/24:
* I first copy and pasted code from [aframe.io](https://aframe.io/docs/1.5.0/introduction/) into my aframe.html, and then I tried to figure out how the shapes moved. I did this by adding 4 boxes and changing the positions in the code to see where and how it would move. I also used the shapes to create a square head with a face.

---

### 3/4/24:
* I wanted to learn how to use images on Aframe, so I tried to find a guide. After looking up "how to use images on aframe html" on youtube, I found this [video](https://www.youtube.com/watch?v=tzI5tu-0nm0). I first tried to find a image for the sky background and grass floor. After that I used `<a-assets>` to create an id for each image, here's the code:
    ```html
    <a-assets>
        <img id="sky" src="img/sky3.jpeg"/>
        <img id="grass" src="img/grass.jpeg"/>
      </a-assets>

    ```
    Then I applied these images on to the sky and ground:
    ```html
    <a-plane material="
         repeat: 5000 5000;
          normal-texture-repeat: 5000, 5000;
           color: FFFFFF;" src="#grass" rotation= "-90 0 0" scale= "1000 1000 1"></a-plane>

      <a-sky src="#sky"></a-sky>
    ```
    After I did all of that, this is what I ended up with: ![Alt text](image.png)

---


### 3/11/24:

 I was interested in learning how to add textures to my scene so I looked up a guide. I found this [video](https://www.youtube.com/watch?v=klnwT3vGCPw) which teaches you how to create Earth using a-frame and I followed the steps.

 * I first changed the A-frame version to match the one in the video since the code doesn’t work in the current version. `<script src="https://aframe.io/releases/1.5.0/aframe.min.js"></script>` ----> `<script src="https://aframe.io/releases/0.5.0/aframe.min.js"></script>`




<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
