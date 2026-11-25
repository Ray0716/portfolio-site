+++
title = "Uninav"
description = "College and University matcher with automatic Common Data Set data aggregation and weighing algorithms"
weight = 10
+++
<a href="/projects/" style="float: right; font-size: 0.875rem; margin:0;">← Back to Projects</a>
![Uninav](/img/projects/uninav/cover.png)


<small>In collaboration with Max Peng, Enya Chen and Connie Huang<br>Jan 2024</small>

• Developed Uninav, a website that scrapes Common Data Set data from universities and uses it to help students find appropriate colleges 
• Many existing sites like Naviance and Schoolinks do not take CDS data into account
• UniNav aggregates data like SAT percentile, AP Scores, first gen consideration etc;, weighs them, and reccomends colleges
• Peaceful flower-themes User Interface

<style>
.uninav-gallery {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 1rem;
  margin-top: 1.5rem;
}
.uninav-gallery button {
  position: relative;
  padding: 0;
  border: 0;
  background: none;
  cursor: zoom-in;
  overflow: hidden;
}
.uninav-gallery img {
  width: 100%;
  aspect-ratio: 16 / 10;
  object-fit: cover;
  display: block;
}
.uninav-gallery button::after {
  content: "Click to expand";
  position: absolute;
  inset: 0;
  display: grid;
  place-items: center;
  color: white;
  background: rgba(0, 0, 0, 0.55);
  opacity: 0;
  transition: opacity 0.2s ease;
}
.uninav-gallery button:hover::after,
.uninav-gallery button:focus-visible::after { opacity: 1; }
.uninav-lightbox {
  position: fixed;
  inset: 0;
  z-index: 1000;
  display: none;
  place-items: center;
  padding: 2rem;
  background: rgba(0, 0, 0, 0.85);
  cursor: zoom-out;
}
.uninav-lightbox.open { display: grid; }
.uninav-lightbox img {
  max-width: 95vw;
  max-height: 90vh;
  object-fit: contain;
}
@media (max-width: 700px) {
  .uninav-gallery { grid-template-columns: 1fr; }
}
</style>

<div class="uninav-gallery">
  <button type="button" data-full="/img/projects/uninav/data.png"><img src="/img/projects/uninav/data.png" alt="Uninav data"></button>
  <button type="button" data-full="/img/projects/uninav/results.png"><img src="/img/projects/uninav/results.png" alt="Uninav results"></button>
  <button type="button" data-full="/img/projects/uninav/ui1.png"><img src="/img/projects/uninav/ui1.png" alt="Uninav interface one"></button>
  <button type="button" data-full="/img/projects/uninav/ui2.png"><img src="/img/projects/uninav/ui2.png" alt="Uninav interface two"></button>
</div>

<div class="uninav-lightbox" id="uninav-lightbox" role="dialog" aria-modal="true" aria-label="Expanded project image">
  <img src="" alt="Expanded Uninav screenshot">
</div>

<script>
(function () {
  const lightbox = document.getElementById("uninav-lightbox");
  const lightboxImage = lightbox.querySelector("img");

  document.querySelectorAll(".uninav-gallery button").forEach(function (button) {
    button.addEventListener("click", function () {
      lightboxImage.src = button.dataset.full;
      lightbox.classList.add("open");
    });
  });

  lightbox.addEventListener("click", function () {
    lightbox.classList.remove("open");
    lightboxImage.src = "";
  });

  document.addEventListener("keydown", function (event) {
    if (event.key === "Escape") {
      lightbox.classList.remove("open");
      lightboxImage.src = "";
    }
  });
})();
</script>

