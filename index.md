---
layout: default
title: Responsive Starter Demo
description: Fluid type, mobile-first breakpoints, container queries, and image helpers.
---

<section class="hero"></section>

<article class="grid">
  <div class="card container card--media-right" style="grid-column: span 12;">
    <img src="{{ '/img/card-800.jpg' | relative_url }}" alt="Sample card image" width="800" height="533" class="responsive-media">
    <div class="flow">
      <h2 style="font-size:var(--step-2);margin:0">Adaptive Card using Container Queries</h2>
      <p>This card switches to a two-column layout when its own container is wide enough.</p>
      <picture>
        <source type="image/avif"
                srcset="{{ '/img/card-400.avif'  | relative_url }} 400w,
                        {{ '/img/card-800.avif'  | relative_url }} 800w,
                        {{ '/img/card-1200.avif' | relative_url }} 1200w">
        <source type="image/webp"
                srcset="{{ '/img/card-400.webp'  | relative_url }} 400w,
                        {{ '/img/card-800.webp'  | relative_url }} 800w,
                        {{ '/img/card-1200.webp' | relative_url }} 1200w">
        <img src="{{ '/img/card-800.jpg' | relative_url }}" alt="Responsive demo"
            width="800" height="533"
            sizes="(max-width: 600px) 92vw, (max-width: 1200px) 50vw, 600px"
            loading="lazy" decoding="async" class="responsive-img">
      </picture>
      </div>
  </div>
</article>

<section class="flow">
  <h2>Responsive Table (stacks on small screens)</h2>
  <table class="table table--stack">
    <thead>
      <tr><th>Format</th><th>Best for</th><th>Notes</th></tr>
    </thead>
    <tbody>
      <tr>
        <td data-label="Format">AVIF</td>
        <td data-label="Best for">Photos / highest compression</td>
        <td data-label="Notes">Great size savings; keep JPG fallback.</td>
      </tr>
      <tr>
        <td data-label="Format">WebP</td>
        <td data-label="Best for">Photos & graphics</td>
        <td data-label="Notes">Excellent modern default.</td>
      </tr>
      <tr>
        <td data-label="Format">SVG</td>
        <td data-label="Best for">Logos, icons, line art</td>
        <td data-label="Notes">CSS-themable, crisp at any DPI.</td>
      </tr>
    </tbody>
  </table>
</section>

<style>
.hero { min-height: 50vh; }
@media (max-width: 48rem) {
  .hero { background: center/cover no-repeat image-set(
    url('{{ '/img/hero-m.webp' | relative_url }}') 1x, url('{{ '/img/hero-m@2x.webp' | relative_url }}') 2x
  );}
}
@media (min-width: 48rem) {
  .hero { background: center/cover no-repeat image-set(
    url('{{ '/img/hero-d.webp' | relative_url }}') 1x, url('{{ '/img/hero-d@2x.webp' | relative_url }}') 2x
  );}
}
</style>
