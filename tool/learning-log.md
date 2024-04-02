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

 I was interested in learning how to add textures to my scene so I looked up a video that demonstrates how to use textures. This is the [video](https://www.youtube.com/watch?v=klnwT3vGCPw) I found which teaches you how to create Earth using a-frame.

 * I first changed the A-frame version to match the one in the video since the code doesn’t work in the current version. `<script src="https://aframe.io/releases/1.5.0/aframe.min.js"></script>` ----> `<script src="https://aframe.io/releases/0.5.0/aframe.min.js"></script>`


* Then I created a sphere that has the texture of Earth using `src=”the-url”`. I got the Earth texture from [aframevr/sample-assets](https://github.com/aframevr/sample-assets). I also used `segments-height=""` to polish the Earth.


```html
   <a-sphere src="https://raw.githubusercontent.com/aframevr/sample-assets/master/assets/images/space/earth_atmos_2048.jpg" position="0 2 -6" radius="2" segments-height="60"> </a-sphere>
```

* Even though I wanted to learn textures, I also learned how to make animations. This is the code I used to make the Earth spin:
```html
 <a-animation attribute= "rotation"
        dur="10000"
        to= "0 360 0"
        ease="linear"
        repeat="indefinite">
      </a-animation>
```
 `dur="10000` makes the animation cycle last for 10000 milliseconds

 `to= "0 360 0"` changes the value of the sphere at the end of the animation

 `ease="linear"` makes the speed of the animation constant

 `repeat="indefinite"` makes the animation repeat infinitely

 * After making the Earth, I wanted to put the Earth in space so I found an image of space and put it as the sky.

```html
  <a-assets>
    <img id="space" src="https://cdn.mos.cms.futurecdn.net/HuGGeENt6kGyixe3hT9tnY-1200-80.jpg" />
  </a-assets>

      <a-sky src="#space"></a-sky>
```

*Image of my A-frame*

![alt text](<Screenshot 2024-03-18 000706.png>)

---

### 3/18/24:

I tried to test my knowledge on A-frame by creating the solar system without a guide.

* I first created a sphere with a spinning animation for each planet.

```html
<a-sphere src="" position="0 0 0" radius="" segments-height="">
        <a-animation attribute= "rotation"
        dur="10000"
        to= "0 360 0"
        ease="linear"
        repeat="indefinite">
      </a-animation>
</a-sphere>
```

* Then with this code I created each planet.

*example: code for jupiter:*
```html
   <a-sphere src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSYGgcSkctf7ozuiPEh4bb3Ea-tjREZPKViqg&usqp=CAU" position="46 2 -18" radius="9" segments-height="60" >
      <a-animation attribute= "rotation"
        dur="10000"
        to= "0 360 0"
        ease="linear"
        repeat="indefinite">
      </a-animation>
    </a-sphere>
```

The planet that was the most challenging for me was Saturn because of its rings. To create the rings I used `<a-ring>` and then changed the position, and rotation of it to make with go around Saturn.

*rings code:*
```html
<a-ring
        src="https://lh3.googleusercontent.com/proxy/vLa1XrbfnTgwwJCDIYJajJ0u1v_hKeXkj1RLTDu6F4tL2U8Hf524R1FlXPC8IY1ez7E7Z89Kvi0iDkgwI1LW31cz6ArcGlxrQeManeFxi-PNdOtMdmI-QdEB"
        radius-inner="10"
        radius-outer="13"
        position="70 2 -20"
        rotation="-80 0 0">
      </a-ring>
```

*image of my Saturn:*

![alt text](<Screenshot 2024-03-25 013948.png>)

* The last thing I did was put the space background by using the code `<a-sky src="">`
```html
 <a-sky src="https://media.istockphoto.com/id/1363878760/photo/360-degree-space-nebula-panorama-equirectangular-projection-environment-map-hdri-spherical.jpg?s=170667a&w=0&k=20&c=WgPIQSMonMcIZ9fujRYi1UijKlkEioI1uWbffSaPY8Q=">
 </a-sky>
 ```

*Image of my Aframe:*

![alt text](<Screenshot 2024-03-25 011528.png>)

---

### 3/25/24:

I wanted to see what shapes I could use so I went to [Arame.io](https://aframe.io/docs/1.5.0/components/geometry.html) and put each shape on my scene.

*code for shapes:*
```html
  <a-box position="-20 0.5 -3" rotation="0 0 0" scale=" 5 5 5" color="red"></a-box>

  <a-circle position="-30 0 -3" rotation="0 0 0" scale=" 3 3 3" color="orange"></a-circle>

  <a-ring position="-30 10 -3" rotation="0 0 0" scale=" 3 3 3" color="red"></a-ring>

  <a-cone position="-42 0 -3" rotation="0 0 0" scale=" 5 5 5" color="yellow"></a-cone>

  <a-sphere src="https://raw.githubusercontent.com/aframevr/sample-assets/master/assets/images/space/earth_atmos_2048.jpg" position="-42 10 -3" rotation="0 0 0" scale=" 4 4 4" ></a-sphere>

  <a-plane src="img/grass.jpeg" position="-20 10 -3" rotation="0 0 0" scale=" 5 5 5" ></a-plane>

  <a-cylinder position="-55 0 -3" rotation="0 0 0" scale="4 8 5" color="green"></a-cylinder>

  <a-tetrahedron position="-55 10 -3" rotation="0 0 0" scale="5 5 5" color="skyblue"></a-tetrahedron>

  <a-dodecahedron position="-67 0 -3" rotation="0 0 0" scale=" 5 5 5" color="blue"></a-dodecahedron>

  <a-torus src="https://www.shutterstock.com/image-vector/cake-glaze-colorful-seamless-pattern-600nw-277068518.jpg" position="-67 10 -3" rotation="0 0 0" scale=" 3 3 3" ></a-torus>

  <a-octahedron position="-80 0 -3" rotation="0 0 0" scale=" 5 5 5" color="purple"></a-octahedron>

  <a-torus-knot src="https://media.istockphoto.com/id/493788392/photo/old-rope-background.jpg?s=612x612&w=0&k=20&c=86XXhIfL21VmMqtqjs0XwfhM5zNwwKL5NVsOgHCL43g=" position="-80 10 -3"  rotation="0 0 0" radius="2" ></a-torus-knot>

  <a-icosahedron position="-92 0 -3" rotation="0 0 0" scale=" 4 4 4" color="pink"></a-icosahedron>

  <a-triangle src="https://t3.ftcdn.net/jpg/01/71/84/50/360_F_171845099_HX3VakW5hyUBjGU7uoo7QwcqQg6JBJwI.jpg" position="-92 10 -3" rotation="0 0 0" scale="5 5 5" ></a-triangle>
```

Then I tried testing the `<a-text>` code to add text to my scene. I first added it as a label to all of my shapes, and then I also created a curved image of a forest and added text in front of it.

*code for curved image with text*
```html
  <a-text value="This is a forest" scale="13 20 20" position="-6 1 -14"></a-text>

      <a-curvedimage
      src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRHQbz1f5y-avz11zs5ol2SWXMVWaGX7zMpRw&s"
      position="5 1 -20"
      radius="14"
      height="20"
      rotation="0 30 0"
      >
     </a-curvedimage>
```

![alt text](<Screenshot 2024-04-02 022853.png>)


<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
