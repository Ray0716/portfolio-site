+++
title = "Kinematic Synthesis of Planar Leg Mechanisms"
description = "Research at Stony Brook University that led to a published paper."
weight = 2
+++
<a href="/research/" style="float: right; font-size: 0.875rem; margin:0;">← Back to Research</a>

![Simons Summer Research Program](/img/thumbnails/walking.gif)

<small>Stony Brook University, Design Intelligence Lab, Stony Brook, NY<br>Researcher / Simons Research Fellow<br>May 2025 - Feb 2026 </small>


• Developed a computational pipeline for large-scale kinematic synthesis of planar leg mechanisms, generating and evaluating 100 million candidate mechanisms with physics-based simulation <br>

• Implemented geometric filtering and optimization to produce a dataset of 23,000+ novel walking mechanisms; optimized parallel filtering code on the SeaWulf high-performance computing cluster <br>

• First-author paper in MDPI Machines (Q2).


## Links

[Paper↗](https://www.mdpi.com/2075-1702/14/3/253)
[Research Poster↗](/static/img/projects/linkages/Ray%20Tang%20LISEF%20Poster.pptx)
[Conference Slides↗](/static/img/projects/linkages/Ray%20Tang%20Research%20Presentation.pdf)


## Selected Figures

<style>
  .research-figure-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 1rem;
    margin: 1.25rem 0;
  }

  .research-figure {
    position: relative;
    aspect-ratio: 16 / 10;
    overflow: hidden;
    border: 0;
    border-radius: 0.75rem;
    padding: 0;
    background: var(--bg-secondary, #f5f5f5);
    cursor: zoom-in;
  }

  .research-figure img {
    display: block;
    width: 100%;
    height: 100%;
    object-fit: contain;
  }

  .research-figure-label {
    position: absolute;
    inset: 0;
    display: flex;
    align-items: flex-end;
    justify-content: center;
    padding: 1rem;
    color: white;
    font-weight: 700;
    text-align: center;
    background: linear-gradient(to top, rgba(0, 0, 0, 0.72), transparent 70%);
    opacity: 0;
    transition: opacity 180ms ease;
  }

  .research-figure:hover .research-figure-label,
  .research-figure:focus-visible .research-figure-label {
    opacity: 1;
  }

  .research-figure:focus-visible {
    outline: 3px solid currentColor;
    outline-offset: 3px;
  }

  .research-lightbox {
    width: min(92vw, 1400px);
    height: min(92vh, 900px);
    max-width: none;
    max-height: none;
    border: 0;
    border-radius: 0.75rem;
    padding: 0;
    background: transparent;
    overflow: hidden;
  }

  .research-lightbox::backdrop {
    background: rgba(0, 0, 0, 0.82);
  }

  .research-lightbox img {
    width: 100%;
    height: 100%;
    object-fit: contain;
  }

  .research-lightbox-close {
    position: absolute;
    top: 0.75rem;
    right: 0.75rem;
    width: 2.5rem;
    height: 2.5rem;
    border: 0;
    border-radius: 999px;
    color: white;
    background: rgba(0, 0, 0, 0.72);
    font-size: 1.5rem;
    line-height: 1;
    cursor: pointer;
  }

  @media (max-width: 640px) {
    .research-figure-grid { grid-template-columns: 1fr; }
  }
</style>

<div class="research-figure-grid">
  <button class="research-figure" type="button" data-expand="/img/projects/linkagefigure.png" aria-label="Expand linkage figure">
    <img src="/img/projects/linkagefigure.png" alt="Linkage Figure">
    <span class="research-figure-label">Click to expand</span>
  </button>
  <button class="research-figure" type="button" data-expand="/img/projects/linkagegif.gif" aria-label="Expand linkage animation">
    <img src="/img/projects/linkagegif.gif" alt="Linkage Animation">
    <span class="research-figure-label">Click to expand</span>
  </button>
  <button class="research-figure" type="button" data-expand="/img/projects/optimfigure.jpeg" aria-label="Expand optimization figure">
    <img src="/img/projects/optimfigure.jpeg" alt="Optimization Figure">
    <span class="research-figure-label">Click to expand</span>
  </button>
  <button class="research-figure" type="button" data-expand="/img/projects/filter.jpeg" aria-label="Expand filtering figure">
    <img src="/img/projects/filter.jpeg" alt="Filtering Figure">
    <span class="research-figure-label">Click to expand</span>
  </button>
</div>

<dialog class="research-lightbox" id="research-lightbox">
  <img id="research-lightbox-image" src="" alt="Expanded research figure">
  <button class="research-lightbox-close" type="button" aria-label="Close expanded figure">×</button>
</dialog>

<script>
  (() => {
    const lightbox = document.getElementById('research-lightbox');
    const lightboxImage = document.getElementById('research-lightbox-image');
    const closeButton = lightbox.querySelector('.research-lightbox-close');

    document.querySelectorAll('.research-figure').forEach((figure) => {
      figure.addEventListener('click', () => {
        const source = figure.dataset.expand;
        lightboxImage.src = source;
        lightboxImage.alt = figure.querySelector('img').alt;
        lightbox.showModal();
      });
    });

    closeButton.addEventListener('click', () => lightbox.close());
    lightbox.addEventListener('click', (event) => {
      if (event.target === lightbox) lightbox.close();
    });
  })();
</script>


