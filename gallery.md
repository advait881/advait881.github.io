---
layout: single
title: Gallery
permalink: /gallery/
---

<style>
.gallery-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 1.5rem;
  margin-top: 2rem;
}

.gallery-item {
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 4px 12px rgba(0,0,0,0.08);
  transition: transform 0.3s ease;
}

.gallery-item:hover {
  transform: scale(1.03);
}

.gallery-item img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
}

.caption {
  padding: 0.5rem;
  text-align: center;
  background-color: #f8f8f8;
  font-size: 0.95rem;
  font-style: italic;
}
</style>

## 📸 Photo Gallery

Explore moments from our retreats, workshops, and spiritual gatherings.

<div class="gallery-container">
  {% for image in site.data.gallery %}
  <div class="gallery-item">
    <img src="{{ image.url }}" alt="{{ image.alt }}">
    {% if image.caption %}
    <div class="caption">{{ image.caption }}</div>
    {% endif %}
  </div>
  {% endfor %}
</div>
