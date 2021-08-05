# yoon-ju-website

To add a new drawing:

1) Add `DRAWING.jpg` (400 pxl width) and `DRAWING_thumb.jpg` (200 pxl width) to `images/` directory

2) In `index.html`:

- Above `<!-- All thumbnails images go here-->`, add:

```
<figure id="DRAWING" class="zoom">
  <a class="zoom" href="#DRAWING_thumb"><img width="1908" height="982" src='imagesDRAWING.jpg' alt="DRAWING NAME" decoding="async" loading="lazy"></a>
  <figcaption>DRAWING NAME</figcaption>
</figure>
````

- In the corresponding year zone, add:

```
<figure class='container hoverable'>
  <a href='#DRAWING'>
    <img class='thumbnail' id='DRAWING_thumb' src='images/DRAWING_thumb.jpg' alt="DRAWING NAME" decoding='async' loading='lazy'>
  </a>
</figure>
```

3) In `styles.css`, add this line in the following code snippet (do not forget to add a comma at the end of the above line):

```
figure#drawing_aaa_11:target,
figure#drawing_bbb:target,
figure#drawing_bbb:target,

/* Add new line here */
figure#DRAWING:target

 {
  display: flex;
  flex-direction: column;
  top: 0;
  margin: auto;
  width: 100%;
  height: 100%;
  align-content: center;
  justify-content: center;
  align-items: center;
  min-height: max-content;
}
```

4) Test the website in incognito mode to avoid cache.
