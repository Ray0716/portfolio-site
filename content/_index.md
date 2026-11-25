+++
title = "Home"
+++


<div class="bento-grid">
  <a href="/piano/" class="bento-item">
    <img src="/img/photography/IMG_5003.jpg" alt="Gallery">
    <span>Creative</span>
  </a>

  <a href="/projects/" class="bento-item">
    <img src="/img/thumbnails/walking.gif" alt="Projects">
    <span>Research</span>
  </a>

  <a href="/about/" class="bento-item">
    <img src="/img/photography/IMG_9832.jpg" alt="Blog">
    <span>About</span>
  </a>

  <a href="/projects/" class="bento-item">
    <img src="/img/thumbnails/zrDemo.gif" alt="Contact">
    <span></span>
  </a>

  

  <a href="/about/" class="bento-item">
    <img src="/img/thumbnails/aircontrol.gif" alt="About">
    <span></span>
  </a>

  <a href="/projects/" class="bento-item">
    <img src="/img/thumbnails/walkbot.png" alt="Gallery">
    <span>Projects</span>
  </a>


  <a href="/contact/" class="bento-item">
    <img src="/img/photography/IMG_3592.jpg" alt="Gallery">
    <span>Contact</span>
  </a>

  <a href="/piano/" class="bento-item">
    <img src="/img/thumbnails/piano.png" alt="Gallery">
    <span>Piano</span>
  </a>

</div>

<style>
.bento-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-auto-rows: 180px;
  gap: 12px;
  max-width: 1200px;
  margin: 0 auto;
}

.bento-item {
  position: relative;
  display: block;
  overflow: hidden;
  border-radius: 0px;
  text-decoration: none;
}

.bento-item:nth-child(1) {
  grid-column: span 2;
  grid-row: span 2;
}

.bento-item:nth-child(2) {
  grid-column: span 2;
}

.bento-item:nth-child(3) {
  grid-column: span 1;
}

.bento-item:nth-child(4) {
  grid-column: span 1;
}

.bento-item:nth-child(5) {
  grid-column: span 2;
  grid-row: span 2;
}

.bento-item:nth-child(6) {
  grid-column: span 1;
}
.bento-item:nth-child(7) {
  grid-column: span 1;
}
.bento-item:nth-child(8) {
  grid-column: span 2;
}

.bento-item img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
  transition: transform 0.3s ease;
}

.bento-item:nth-child(5) img {
  object-fit: cover;
  object-position: 25% 50%;
  background: #000;
}

.bento-item:hover img {
  transform: scale(1.05);
}

.bento-item span {
  position: absolute;
  bottom: 16px;
  left: 16px;
  color: white;
  font-size: 1.2rem;
  font-weight: 600;
  text-shadow: 0 2px 8px rgba(0,0,0,0.7);
}

@media (max-width: 600px) {
  .bento-grid {
    grid-template-columns: repeat(2, 1fr);
    grid-auto-rows: 140px;
  }
}
</style>