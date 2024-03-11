# Tool Learning Log

Tool: **Aframe**

---

2/26/24:
* I first copy and pasted code from [aframe.io](https://aframe.io/docs/1.5.0/introduction/) into my aframe.html, and then I tried to figure out how the shapes moved. I did this by adding 4 boxes and changing the positions in the code to see where and how it would move. I also used the shapes to create a square head with a face.


3/4/24:
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

<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
