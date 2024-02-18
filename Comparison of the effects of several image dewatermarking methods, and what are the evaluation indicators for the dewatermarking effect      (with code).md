WeChat 394467238 

 The previous article tried to write a way to remove watermarks from images, but later found that there were still some problems when processing videos. 

 The article link is: lonlon ago: Python code for video dewatermarking 

 The method of this article is to get the watermark mask first, and then randomly select nearby points to replace the points inside the mask. The problem is that some parts will appear white noise-like areas, so I have tried some other methods later. This article compares the effect of these methods. 

 1 randomly select nearby points to replace the watermark 

 2 OpenCV inpaint method 

 3 randomly select nearby areas to replace the watermark 

 4 Replace the watermark by interpolation 

 5 Black Box Magic 

 The original image is as follows: 

 ![avatar]( e117934d86d378112fee9ed660430f98.png) 

 The multiple synthesized mask images are as follows, and so far this step has been very successful: 

 ![avatar]( 6012a29cc70b82dca595e1b18f7e4d5c.png) 

 For areas with poor magnification, the watermark in the red box is replaced with a point like white noise, losing the outline of the object: 

 ![avatar]( 1d4d1f138f784ecdb238d9747559e1c5.png) 

 2. The effect of OpenCV's inpaint method is that the watermark part becomes transparent as a whole, but the watermark traces can still be seen: 

 ![avatar]( 1ff1885d4892f6d168bb62091599c1d3.png) 

 Zoom in to see the effect: 

 ![avatar]( 2cbe76e5c6815fb61c8f8ee081b64e9b.png) 

 3. The method of randomly selecting nearby areas to replace the watermark, the initial idea is that random points will cause the same effect as white noise, and there is no outline, so randomly selecting areas to replace should be better, but in fact the effect is not good, there is another problem, there will be a mosaic-like effect: 

 Zoom in to see the areas that are not working well: 

 ![avatar]( 86d172bd128d0f7714d7d59a4c457ddc.png) 

 4. By interpolating and replacing the watermark, in theory, the result he obtained should be the smoothest and most ideal, but in fact it is not satisfactory 

 Zoom in to see the effect, it feels like a watermark that has been evenly smeared, and the effect is not good. The problem may be that the interpolation range is too large, resulting in the inability to perform effective interpolation: 

 ![avatar]( 17f1d4d53295446cc6a615aa4efc8051.png) 

 5. Black box magic, the effect is perfect. Try it above. 

 It's okay to zoom in. 

 ![avatar]( 0617b86d90a6911b08abeae7fb09e6cb.png) 

