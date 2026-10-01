---
title: "Vlog"
permalink: /vlog/
classes: wide
---

<style>
.vlog-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2em;
  margin-bottom: 2em;
}
.vlog-card {
  background: #fff;
  border-radius: 10px;
  padding: 0.8em;
  box-shadow: 0 2px 10px rgba(0,0,0,0.1);
  cursor: zoom-in;
}
.vlog-card img {
  width: 100%;
  border-radius: 6px;
  display: block;
}
#vlog-lightbox {
  display: none;
  position: fixed;
  top: 0; left: 0; right: 0; bottom: 0;
  background: rgba(0,0,0,0.9);
  z-index: 9999;
  align-items: center;
  justify-content: center;
  cursor: zoom-out;
}
#vlog-lightbox img {
  max-width: 92%;
  max-height: 92%;
  border-radius: 6px;
}
@media (max-width: 800px) {
  .vlog-grid { grid-template-columns: 1fr; }
}
</style>
## Building a Digital Twin, Behind the Screens

My workstation is two screens side by side. On one I run the photogrammetry software, and on the other I check the model in 3D. A 3D mouse and 3D glasses let me move through the data instead of just looking at it. The input is Mavic 3E drone imagery from a site in Sululta, Addis Ababa, Ethiopia.

Hours of flight lines become a dense point cloud, then a georeferenced 3D model and orthophoto. In the end it becomes something anyone can open and explore: a live, interactive digital twin of the site.

[Explore the interactive 3D model →](/projects/uav-3d-terrain-reconstruction/)
<div class="vlog-grid">
  <div class="vlog-card" onclick="openVlogLightbox('/assets/images/vlog-1.jpg.png')"><img src="/assets/images/vlog-1.jpg.png" alt="Vlog 1"></div>
  <div class="vlog-card" onclick="openVlogLightbox('/assets/images/vlog-2.jpg.png')"><img src="/assets/images/vlog-2.jpg.png" alt="Vlog 2"></div>
  <div class="vlog-card" onclick="openVlogLightbox('/assets/images/vlog-3.jpg.jpg')"><img src="/assets/images/vlog-3.jpg.jpg" alt="Vlog 3"></div>
</div>

<div id="vlog-lightbox" onclick="this.style.display='none'">
  <img id="vlog-lightbox-img" src="">
</div>

<script>
function openVlogLightbox(src) {
  document.getElementById('vlog-lightbox-img').src = src;
  document.getElementById('vlog-lightbox').style.display = 'flex';
}
</script>
