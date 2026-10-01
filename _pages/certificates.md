---
title: "Certificates"
permalink: /certificates/
classes: wide
---

<style>
.cert-section-title {
  font-size: 2em;
  font-weight: 700;
  border-bottom: 2px solid #ddd;
  padding-bottom: 0.3em;
  margin-top: 1.5em;
  margin-bottom: 1em;
}
.cert-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2em;
  margin-bottom: 2em;
}
.cert-card {
  background: #fff;
  border-radius: 10px;
  padding: 0.8em;
  box-shadow: 0 2px 10px rgba(0,0,0,0.1);
  cursor: zoom-in;
}
.cert-card img,
.cert-card canvas {
  width: 100%;
  border-radius: 6px;
  display: block;
}
#cert-lightbox {
  display: none;
  position: fixed;
  top: 0; left: 0; right: 0; bottom: 0;
  background: rgba(0,0,0,0.9);
  z-index: 9999;
  align-items: center;
  justify-content: center;
  cursor: zoom-out;
}
#cert-lightbox img,
#cert-lightbox canvas {
  max-width: 92%;
  max-height: 92%;
  border-radius: 6px;
  background: #fff;
}
@media (max-width: 800px) {
  .cert-grid { grid-template-columns: 1fr; }
}
</style>

<div class="cert-section-title">Esri Training</div>
<div class="cert-grid">
  <div class="cert-card" onclick="openCertLightbox('/assets/images/esri-arcgis-online-basics.png')"><img src="/assets/images/esri-arcgis-online-basics.png"></div>
  <div class="cert-card" onclick="openCertLightbox('/assets/images/esri-data-management.png')"><img src="/assets/images/esri-data-management.png"></div>
  <div class="cert-card" onclick="openCertLightbox('/assets/images/esri-storytelling-gis-maps.png')"><img src="/assets/images/esri-storytelling-gis-maps.png"></div>
  <div class="cert-card" onclick="openCertLightbox('/assets/images/esri-storymaps-briefing.png')"><img src="/assets/images/esri-storymaps-briefing.png"></div>
  <div class="cert-card" onclick="openCertLightbox('/assets/images/esri-mapping-visualization.png')"><img src="/assets/images/esri-mapping-visualization.png"></div>
  <div class="cert-card" data-pdf="/assets/images/esri-dividing-parcels-parcel-fabric.png.pdf"><canvas></canvas></div>
  <div class="cert-card" data-pdf="/assets/images/esri-imagery-mooc.png.pdf"><canvas></canvas></div>
  <div class="cert-card" data-pdf="/assets/images/esri-getting-started-imagery-rs.png.pdf"><canvas></canvas></div>
</div>

<div class="cert-section-title">NASA</div>
<div class="cert-grid">
  <div class="cert-card" onclick="openCertLightbox('/assets/images/nasa-fundamentals-remote-sensing.png')"><img src="/assets/images/nasa-fundamentals-remote-sensing.png"></div>
  <div class="cert-card" onclick="openCertLightbox('/assets/images/nasa-earth-science-applications.png')"><img src="/assets/images/nasa-earth-science-applications.png"></div>
  <div class="cert-card" onclick="openCertLightbox('/assets/images/nasa-hyperspectral-data.png')"><img src="/assets/images/nasa-hyperspectral-data.png"></div>
</div>

<div class="cert-section-title">ITC / Geoversity</div>
<div class="cert-grid">
  <div class="cert-card" onclick="openCertLightbox('/assets/images/itc-do-no-harm-drone-ethics.png')"><img src="/assets/images/itc-do-no-harm-drone-ethics.png"></div>
  <div class="cert-card" onclick="openCertLightbox('/assets/images/itc-copernicus-sentinel-data.png')"><img src="/assets/images/itc-copernicus-sentinel-data.png"></div>
</div>

<div class="cert-section-title">ESA EO College</div>
<div class="cert-grid">
  <div class="cert-card" onclick="openCertLightbox('/assets/images/eo-college-machine-learning.png')"><img src="/assets/images/eo-college-machine-learning.png"></div>
</div>

<div class="cert-section-title">Others</div>
<div class="cert-grid">
  <div class="cert-card" onclick="openCertLightbox('/assets/images/other-geo-university-opencv-python.jpg')"><img src="/assets/images/other-geo-university-opencv-python.jpg"></div>
  <div class="cert-card" onclick="openCertLightbox('/assets/images/other-3is-gis-humanitarian.png')"><img src="/assets/images/other-3is-gis-humanitarian.png"></div>
  <div class="cert-card" onclick="openCertLightbox('/assets/images/other-bdu-best-scorer-award.jpg')"><img src="/assets/images/other-bdu-best-scorer-award.jpg"></div>
  <div class="cert-card" onclick="openCertLightbox('/assets/images/other-bdu-best-exam-scorer-award.jpg')"><img src="/assets/images/other-bdu-best-exam-scorer-award.jpg"></div>
  <div class="cert-card" onclick="openCertLightbox('/assets/images/other-bdu-food-affairs-recognition.jpg')"><img src="/assets/images/other-bdu-food-affairs-recognition.jpg"></div>
  <div class="cert-card" onclick="openCertLightbox('/assets/images/other-british-council-peace-education.jpg')"><img src="/assets/images/other-british-council-peace-education.jpg"></div>
  <div class="cert-card" data-pdf="/assets/images/other-ilasa.jpg.pdf"><canvas></canvas></div>
  <div class="cert-card" data-pdf="/assets/images/other-class-representative.jpg.pdf"><canvas></canvas></div>
</div>

<div id="cert-lightbox" onclick="this.style.display='none'">
  <img id="cert-lightbox-img" src="">
  <canvas id="cert-lightbox-canvas" style="display:none"></canvas>
</div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.11.174/pdf.min.js"></script>
<script>
pdfjsLib.GlobalWorkerOptions.workerSrc = 'https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.11.174/pdf.worker.min.js';
function openCertLightbox(src) {
  document.getElementById('cert-lightbox-canvas').style.display = 'none';
  var img = document.getElementById('cert-lightbox-img');
  img.src = src;
  img.style.display = 'block';
  document.getElementById('cert-lightbox').style.display = 'flex';
}
async function renderPdfPage(canvas, url, width) {
  var pdf = await pdfjsLib.getDocument(url).promise;
  var page = await pdf.getPage(1);
  var base = page.getViewport({ scale: 1 });
  var viewport = page.getViewport({ scale: width / base.width });
  canvas.width = viewport.width;
  canvas.height = viewport.height;
  await page.render({ canvasContext: canvas.getContext('2d'), viewport: viewport }).promise;
}
async function openCertPdf(url) {
  var canvas = document.getElementById('cert-lightbox-canvas');
  document.getElementById('cert-lightbox-img').style.display = 'none';
  canvas.style.display = 'block';
  document.getElementById('cert-lightbox').style.display = 'flex';
  await renderPdfPage(canvas, url, 1800);
}
document.querySelectorAll('.cert-card[data-pdf]').forEach(function (card) {
  var url = card.getAttribute('data-pdf');
  renderPdfPage(card.querySelector('canvas'), url, 900);
  card.addEventListener('click', function () { openCertPdf(url); });
});
</script>
