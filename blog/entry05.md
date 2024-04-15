# Entry 5
##### 4/8/24


### Context
After choosing to use Aframe as my tool for my website, I now have to learn how to use it.

---

### Tinkering with Aframe:

#### Learning the shapes and how to apply text

- I first went to [Arame.io](https://aframe.io/docs/1.5.0/components/geometry.html) and put each shape on my scene. To add the shapes I had to use `<a-(name-of-shape)>`.

*code to add a box*

```html
  <a-box position="-20 0.5 -3" rotation="0 0 0" scale=" 5 5 5" color="red"></a-box>
```

- Then I added labels to each shape by using the `<a-text>` tag.

*example*

```html
 <a-text value="box" scale="10 10 5" position="-22 -7 -3"></a-text>
```

![alt text](image.png)

#### Applying images

To help me learn how to use images, I tried to look up a guide. After looking up "how to use images on aframe html" on youtube, I found this [video](https://www.youtube.com/watch?v=tzI5tu-0nm0).

-  I first tried to find a image for the sky background and grass floor. After that I used `<a-assets>` to create an id for each image, here's the code:

```html
    <a-assets>
        <img id="sky" src="img/sky3.jpeg"/>
        <img id="grass" src="img/grass.jpeg"/>
      </a-assets>
```

- Then I applied these images on to the sky and ground:


```html
    <a-plane material="
         repeat: 5000 5000;
          normal-texture-repeat: 5000, 5000;
           color: FFFFFF;" src="#grass" rotation= "-90 0 0" scale= "1000 1000 1"></a-plane>

      <a-sky src="#sky"></a-sky>
```
After I did all of that, this is what I ended up with:

![Alt text](../tool/image.png)


#### Adding textures

To learn how to add textures I also looked up a guide. This is the [video](https://www.youtube.com/watch?v=klnwT3vGCPw) I found which teaches you how to create Earth using a-frame.

- First I created a sphere by using `<a-sphere>`

- Then I added the texture of Earth to the sphere by using `src=”the-url”`. I got the Earth texture from [aframevr/sample-assets](https://github.com/aframevr/sample-assets). I also used `segments-height=""` to polish the Earth.

```html
   <a-sphere src="https://raw.githubusercontent.com/aframevr/sample-assets/master/assets/images/space/earth_atmos_2048.jpg" position="0 2 -6" radius="2" segments-height="60"> </a-sphere>
```

*Image of my A-frame*

![alt text](<../tool/Screenshot 2024-03-18 000706.png>)




---

[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
