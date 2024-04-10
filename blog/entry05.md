# Entry 5
##### 4/8/24

### Context
After choosing to use Aframe as my tool, I now have to learn how to use it.

---

### Tinkering with Aframe:

- #### Applying images

I wanted to learn how to use images on Aframe, so I tried to find a guide. After looking up "how to use images on aframe html" on youtube, I found this [video](https://www.youtube.com/watch?v=tzI5tu-0nm0). I first tried to find a image for the sky background and grass floor. After that I used `<a-assets>` to create an id for each image, here's the code:

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
After I did all of that, this is what I ended up with:

![Alt text](image.png)

---


---


[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
