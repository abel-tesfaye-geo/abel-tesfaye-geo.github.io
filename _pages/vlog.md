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

<div class="vlog-grid">
  <div class="vlog-card" onclick="openVlogLightbox('/assets/images/vlog-1.jpg')"><img src="/assets/images/vlog-1.jpg" alt="Vlog 1"></div>
  <div class="vlog-card" onclick="openVlogLightbox('/assets/images/vlog-2.jpg')"><img src="/assets/images/vlog-2.jpg" alt="Vlog 2"></div>
  <div class="vlog-card" onclick="openVlogLightbox('/assets/images/vlog-3.jpg')"><img src="/assets/images/vlog-3.jpg" alt="Vlog 3"></div>
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
