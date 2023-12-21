---
layout: post
title: Multimorphing (Paper@CGI2023)
date: 2023-12-21 10:10:00-0400
description: Project overview
tags: ComputerGraphics 3D-RealTimeRendering ImageBasedRendering ImageMorphing VirtualRealtiy
categories:
giscus_comments: false
related_posts: false
related_publications: 
thumbnail: assets/img/multimorphing/cgi2023.jpg
---
<hr>
<style>
table, td, th {
   border: none!important;
}
</style>

<center><h1><b>Multidimensional Image Morphing</b><br></h1><h4><b>Fast Image-based Rendering of Open 3D and VR Environments</b></h4></center>
<br>
<center><h3>CGI'2023</h3></center>
<center><h5>(Journal Track)</h5></center>
<br>
<center><h6>Simon Seibt<sup>1</sup>, Bastian Kuth<sup>2</sup>, Bartosz von Rymon Lipinski<sup>1</sup>, Thomas Chang<sup>1</sup> and Marc Erich Latoschik<sup>3</sup></h6></center>
<br>
<center><sup>1</sup> Game Tech Lab, Nuremberg Institute of Technology<br>
<sup>2</sup> Department of Computer Science, University of Applied Sciences<br>
<sup>3</sup> Human-Computer Interaction Group, University of Wuerzburg</center>
<br>
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        <div class="text-right">
            {% include figure.html path="assets/img/multimorphing/ibr_results1.jpg" class="img-fluid rounded z-depth-1"  width="200" zoomable=true %}
        </div>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <div class="text-center">
            {% include figure.html path="assets/img/multimorphing/ibr_results2.jpg" class="img-fluid rounded z-depth-1"  width="200" zoomable=true %}
        </div>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <div class="text-left">
            {% include figure.html path="assets/img/multimorphing/ibr_results3.jpg" class="img-fluid rounded z-depth-1"  width="200" zoomable=true %}
        </div>
    </div>
</div>

<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        <div class="text-right">
            {% include figure.html path="assets/img/multimorphing/ibr_results4.jpg" class="img-fluid rounded z-depth-1"  width="200" zoomable=true %}
        </div>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <div class="text-left">
            {% include figure.html path="assets/img/multimorphing/ibr_results5.jpg" class="img-fluid rounded z-depth-1"  width="200" zoomable=true %}
        </div>
    </div>
</div>
<center><p>Multi-morphing rendering results<br>(In the first row are the following real scenes: "Farmland," "Nature Walk," and "Living Room".<br>In the second row are the following synthetic scenes: "Cave" and "Bistro".)</p></center>
<br>
<center><h3><b>Abstract</b></h3></center>
<p style="text-align: justify;">The demand for interactive photorealistic 3D environments has increased in recent years and in various fields such as architecture, engineering and entertainment. Nevertheless, achieving a balance between quality and performance for high-performance 3D applications and Virtual Reality (VR) remains a challenge. This paper addresses this issue by revisiting and extending view interpolation for image-based rendering, enabling the exploration of spacious open environments in 3D and VR. Therefore, we introduce multi-morphing, a novel rendering method based on a spatial data structure of 2D image patches, called the image graph. With this approach, novel views can be rendered with up to six degrees of freedom using only a sparse set of views. The rendering process does not require 3D reconstruction of geometry, nor per-pixel depth information: All relevant data for output is extracted from local morphing cells of the image graph. Detection of parallax image regions during preprocessing reduces rendering artifacts by extrapolating image patches from adjacent cells in real-time. Additionally, a GPU-based solution to resolve exposure inconsistencies within a dataset is presented, enabling seamless transitions of brightness when moving between areas with varying light intensities. Experiments on multiple real-world and synthetic scenes demonstrate that the presented method achieves high ``VR-compatible'' frame rates, even on mid-range and legacy hardware, respectively.</p>
<br>
<center><h3><b>Paper</b></h3></center>
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        <div class="text-center">
            {% include figure.html path="assets/img/multimorphing/paper_cover.png" width="310" zoomable=false %}
        </div>
    </div>
</div>
<br>
<center><h3><b>Pipelines</b></h3></center>
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        <div class="text-center">
            {% include figure.html path="assets/img/multimorphing/preprocessing.svg" width="420" zoomable=true %}
        </div>
    </div>
</div>
<center>UML-based activity diagram of the preprocessing pipeline.</center>
<br>
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        <div class="text-center">
            {% include figure.html path="assets/img/multimorphing/rendering.svg" width="750" zoomable=true %}
        </div>
    </div>
</div>
<center>UML-based activity diagram of the rendering pipeline.</center>
<br>
<center><h3><b>Visual Results</b></h3></center>
<center><h5><b>Demo Video</b></h5></center>
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        <div class="text-center">
            <video style="margin: 0 auto" id="page-player_html5_api" class="vjs-tech" preload="auto" data-setup="{}" tabindex="-1" muted="muted" src="https://faubox.rrze.uni-erlangen.de/dl/fiLWaSiskiGU5fykMctrdK/multimorphing/multimorphing_demo.mp4" style="max-width: 720px;" controls="controls"></video>
        </div>
    </div>
</div>
<br>
<center><h5><b>Visual comparisons</b></h5></center>
<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
    <div class="text-center">
        <center><p><b>Spixelwarp [1]</b></p></center>
        {% include figure.html path="assets/img/multimorphing/Bild1.jpg" class="img-fluid rounded z-depth-1" width="170" zoomable=true %}
        {% include figure.html path="assets/img/multimorphing/Bild6.jpg" class="img-fluid rounded z-depth-1" width="170" zoomable=true %}
        {% include figure.html path="assets/img/multimorphing/Bild11.jpg" class="img-fluid rounded z-depth-1" width="170" zoomable=true %}
        {% include figure.html path="assets/img/multimorphing/Bild16.jpg" class="img-fluid rounded z-depth-1" width="170" zoomable=true %}
    </div>
    </div>
    <div class="col-sm mt-3 mt-md-0">
    <div class="text-center">
        <center><p><b>Soft3D [2]</b></p></center>
        {% include figure.html path="assets/img/multimorphing/Bild2.jpg" class="img-fluid rounded z-depth-1" width="170" zoomable=true %}
        {% include figure.html path="assets/img/multimorphing/Bild7.jpg" class="img-fluid rounded z-depth-1" width="170" zoomable=true %}
        {% include figure.html path="assets/img/multimorphing/Bild12.jpg" class="img-fluid rounded z-depth-1" width="170" zoomable=true %}
        {% include figure.html path="assets/img/multimorphing/Bild17.jpg" class="img-fluid rounded z-depth-1" width="170" zoomable=true %}
    </div>
    </div>
    <div class="col-sm mt-3 mt-md-0">
    <div class="text-center">
        <center><p><b>Instant NGP [3]</b></p></center>
        {% include figure.html path="assets/img/multimorphing/Bild3.jpg" class="img-fluid rounded z-depth-1" width="170" zoomable=true %}
        {% include figure.html path="assets/img/multimorphing/Bild8.jpg" class="img-fluid rounded z-depth-1" width="170" zoomable=true %}
        {% include figure.html path="assets/img/multimorphing/Bild13.jpg" class="img-fluid rounded z-depth-1" width="170" zoomable=true %}
        {% include figure.html path="assets/img/multimorphing/Bild18.jpg" class="img-fluid rounded z-depth-1" width="170" zoomable=true %}
    </div>
    </div>
    <div class="col-sm mt-3 mt-md-0">
    <div class="text-center">
        <center><p><b>Nerfacto [4]</b></p></center>
        {% include figure.html path="assets/img/multimorphing/Bild4.jpg" class="img-fluid rounded z-depth-1" width="170" zoomable=true %}
        {% include figure.html path="assets/img/multimorphing/Bild9.jpg" class="img-fluid rounded z-depth-1" width="170" zoomable=true %}
        {% include figure.html path="assets/img/multimorphing/Bild14.jpg" class="img-fluid rounded z-depth-1" width="170" zoomable=true %}
        {% include figure.html path="assets/img/multimorphing/Bild19.jpg" class="img-fluid rounded z-depth-1" width="170" zoomable=true %}
    </div>
    </div>
        <div class="col-sm mt-3 mt-md-0">
    <div class="text-center">
        <center><p><b>Proposed</b></p></center>
        {% include figure.html path="assets/img/multimorphing/Bild5.jpg" class="img-fluid rounded z-depth-1" width="170" zoomable=true %}
        {% include figure.html path="assets/img/multimorphing/Bild10.jpg" class="img-fluid rounded z-depth-1" width="170" zoomable=true %}
        {% include figure.html path="assets/img/multimorphing/Bild15.jpg" class="img-fluid rounded z-depth-1" width="170" zoomable=true %}
        {% include figure.html path="assets/img/multimorphing/Bild20.jpg" class="img-fluid rounded z-depth-1" width="170" zoomable=true %}
    </div>
    </div>
</div>
<center>Visual comparisons of novel view generation for scenes: Farmland, Nature Walk, Livingroom and Cave</center>
<br>
<h3><b>BibTeX</b></h3>
>##### Coming soon!
{: .block-tip }
<br>
References

| :---| :------------------------------------------------------------------------------- | 
| [1] | Chaurasia G, Duchene S, Sorkine-Hornung O, et al. Depth synthesis and local warps for plausible image-based navigation. ACM Transactions on Graphics. 2013 June;32:1–12.|
| [2] | Penner E, Zhang L. Soft 3D reconstruction for view synthesis. ACM Transactions on Graphics. 2017 November;36:1–11.|
| [3] | Müller T, Evans A, Schied C, et al. Instant neural graphics primitives with a multiresolution hash encoding. ACM Transactions on Graphics. 2022 July;41:1–15.|
| [4] | Tancik M, Weber E, Ng E, et al. Nerfstudio: A Modular Framework for Neural Radiance Field Development. ACM Transactions on Graphics. 2021;40:1–18.|