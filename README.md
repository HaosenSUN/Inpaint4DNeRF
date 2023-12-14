# Inpaint4DNeRF: Promptable Spatio-Temporal NeRF Inpainting withGenerative Diffusion Models</center>

## Updates

## Introduction
Our generative Inpaint4DNeRF proposes a text-guided approach for inpainting the relevant background after removing static foreground objects specified by a user-supplied prompt, where multiview consistency is meticulously maintained. The code will release soon.

Inpaint4DNeRF: Promptable Spatio-Temporal NeRF Inpainting with Generative Diffusion Models    MathJax.Hub.Config({tex2jax: {inlineMath: \[\['$','$'\], \['\\\\(','\\\\)'\]\]}}); \* { box-sizing: border-box; } video { width: 100%; height: auto; } p { width: 95%; padding: 10px; margin: auto; } /\* Remove the navbar's default margin-bottom and rounded borders \*/ .navbar { margin-bottom: 0; border-radius: 0; } /\* Add a gray background color and some padding to the footer \*/ footer { background-color: #f2f2f2; padding: 25px; } #ours { font-weight: bold; } .glyphicon.glyphicon-arrow-down.main\_arr { font-size: 75px; } .glyphicon.glyphicon-option-horizontal.main\_arr { top: 50px; font-size: 75px; } .glyphicon { display: block; text-align:center; } #noise { text-align:center; vertical-align: bottom; }


### Overview

This webpage contains supplementary material for paper **Inpaint4DNeRF: Promptable Spatio-Temporal NeRF Inpainting with Generative Diffusion Models** submitted to CVPR 2024. There will be free viewpoint videos of 3D inpainting examples in the paper as well as more 4D examples. There will also be a COLMAP section verifying the consistency of our pre-processed training images.

### Videos of 3D Inpainting Examples

  

Text prompt: **an Argentina soccer player**

Text prompt: **an old professor, standing**

Text prompt: **telegraph pole**

RGB, **Final Result**

Depth map, **Final Result**

RGB, **Warmup Result**

Depth map, **Warmup Result**

RGB, **Initial NeRF**

Depth map, **Initial NeRF**

  

### COLMAP reconstruction on pre-processed images

Our inpainting method relies on a set of consistent pre-proccessed multiview images. To demonstrate their consistency, besides the warmup results, we apply **COLMAP multiview stereo dense reconstruction** on the pre-processed images to obtain a point cloud for each 3D example. We also report the **mean projection error** of the examples as a quantitative measure. Results and visualizations for each example are shown in the 3 columns consistent with the above section.

  

"an Argentina soccer player"

"an old professor, standing"

"telegraph pole"

**Mean Projection Error**

1.0428

1.0562

1.0269

**Mean Track Length**

5.5851

5.1763

6.5273

**Visualization of Reconstructed Point Clouds**

![](colmap/vis/arg00.png)

![](colmap/vis/oldprof00.png)

![](colmap/vis/pole00.png)

![](colmap/vis/arg01.png)

![](colmap/vis/oldprof01.png)

![](colmap/vis/pole01.png)

![](colmap/vis/arg02.png)

![](colmap/vis/oldprof02.png)

![](colmap/vis/pole02.png)

  

### Videos of 4D Inpainting Examples

Below we show 3 dynamic NeRF inpainting examples, including the example in our paper. For each example, we show a multiview video of the final result, as well as the "seed video" generated from the first seed images along with the original video.

For the third example "the girl", instead of generating new objects, we try to recover parts of the girl and the background that is occluded by the red dinosaur balloon in the original NeRF. While our final result is not perfectly clear, we can recover the static background and approximately the girl's motion in the NeRF. This example demonstrates that our method can not only generate brand new objects, but also generate missing content that is partially occluded.

  

Text prompt: **a golden sword, side view**

Text prompt: **two storey red bus, driving towards left**

Text prompt: **the girl**

Final Render

Seed Video

Original Video

$(".nav li").on("click", function() { $(".nav li").removeClass("active"); $(this).addClass("active"); });
