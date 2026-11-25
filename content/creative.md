+++
title = "Creative"
+++

I enjoy photography and digital art. Below are some of my favorite pieces!

{{< gallery dir="/img/photography" >}}

<style>
.photography-gallery,
.gallery {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  grid-auto-rows: 220px;
  grid-auto-flow: dense;
  gap: 8px;
}

.photography-gallery figure,
.gallery figure,
.photography-gallery a,
.gallery a {
  height: 100%;
  margin: 0;
}

.photography-gallery figure:nth-child(5n + 1),
.gallery figure:nth-child(5n + 1) {
  grid-column: span 2;
  grid-row: span 2;
}

.photography-gallery img,
.gallery img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 0;
  cursor: zoom-in;
  transition: filter 180ms ease;
}

.photography-gallery figure,
.gallery figure {
  position: relative;
  overflow: hidden;
}

.photography-gallery figure::after,
.gallery figure::after {
  content: "Click to expand";
  position: absolute;
  inset: 0;
  display: grid;
  place-items: center;
  color: white;
  background: rgba(0, 0, 0, 0.45);
  opacity: 0;
  transition: opacity 180ms ease;
  pointer-events: none;
}

.photography-gallery figure:hover::after,
.gallery figure:hover::after {
  opacity: 1;
}

#photo-lightbox {
  position: fixed;
  inset: 0;
  z-index: 9999;
  display: none;
  align-items: center;
  justify-content: center;
  padding: 24px;
  background: rgba(0, 0, 0, 0.92);
  cursor: zoom-out;
}

#photo-lightbox.open {
  display: flex;
}

#photo-lightbox img {
  max-width: 95vw;
  max-height: 95vh;
  width: auto;
  height: auto;
  object-fit: contain;
  border-radius: 0;
}

@media (max-width: 700px) {
  .photography-gallery,
  .gallery {
    grid-template-columns: repeat(2, minmax(0, 1fr));
    grid-auto-rows: 160px;
  }
}
</style>

<script>
document.addEventListener("DOMContentLoaded", function () {
  var gallery = document.querySelector(".photography-gallery, .gallery");
  if (!gallery) return;

  var lightbox = document.createElement("div");
  lightbox.id = "photo-lightbox";
  var expanded = document.createElement("img");
  lightbox.appendChild(expanded);
  document.body.appendChild(lightbox);

  gallery.querySelectorAll("img").forEach(function (image) {
    image.addEventListener("click", function (event) {
      event.preventDefault();
      expanded.src = image.currentSrc || image.src;
      expanded.alt = image.alt;
      lightbox.classList.add("open");
    });
  });

  lightbox.addEventListener("click", function () {
    lightbox.classList.remove("open");
  });

  document.addEventListener("keydown", function (event) {
    if (event.key === "Escape") lightbox.classList.remove("open");
  });
});
</script>
