# Generate Point Cloud from RGB and Depth Images

You can view it online: [Online View](https://kongpeter.github.io/Child-of-Now/Phase%201/)


The question is: How to generate point clouds from RGB and Depth images?

To solve this question, we need to upload two images, RGB and Depth. Make a **grid of points**, for each point set the **Z position to the depth** and the **color** to the color of the image.

As shown in following RGB and Depth Images:

![color](https://i.imgur.com/fkzq62l.png)

![depth](https://i.imgur.com/1VLLIgC.png)

Then, we can generate point clouds:

![PC](https://i.imgur.com/XsUT6uG.png)


The following function shows that how to get a single pixel out and return the colors in the 0 to 1 range. 

```js
// return the pixel at UV coordinates (0 to 1) in 0 to 1 values
function getPixel(imageData, u, v) {
  const x = u * (imageData.width  - 1) | 0;
  const y = v * (imageData.height - 1) | 0;
  if (x < 0 || x >= imageData.width || y < 0 || y >= imageData.height) {
    return [0, 0, 0, 0];
  } else {
    const offset = (y * imageData.width + x) * 4;
    return Array.from(imageData.data.slice(offset, offset + 4)).map(v => v / 255);
  }
}
```