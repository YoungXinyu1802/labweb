---
title: Event
nav:
  order: 4
  tooltip: See the fun
---

# {% include icon.html icon="fa-solid fa-feather-pointed" %}Lab Event

Welcome to **Jennifer's Lab**! 🎉 We're a friendly, inclusive, and supportive group that loves exploring new ideas and having fun together. Here’s a peek into our lab life:

- **Weekly Lab Meeting**: Ideas, progress, and bubble tea! 🧋

- **Monthly Lab Dinners**: Delicious food and great conversations. 🍜

<div class="event-gallery">
  {% assign event = site.data.gallery | where: "category", "event" %}
  {% for image in event %}
    <div class="event-gallery-item">
      <img src="{{ image.src }}" alt="{{ image.caption }}" class="event-gallery-image" loading="lazy" />
      <div class="gallery-caption">
        <div>{{ image.caption }}</div>
        <div class="caption-details">{{ image.camera }} · {{ image.date }}</div>
      </div>
    </div>
  {% endfor %}
</div>

---

## Lab Dinners

<div class="gallery">
  {% assign dinners = site.data.gallery | where: "category", "dinner" %}
  {% for image in dinners %}
    <div class="gallery-item">
      <img src="{{ image.src | relative_url | uri_escape }}" alt="{{ image.caption }}" class="gallery-image" loading="lazy" />
      <div class="gallery-caption">
        <div>{{ image.caption }}</div>
        <div class="caption-details">{{ image.camera }} · {{ image.date }}</div>
      </div>
    </div>
  {% endfor %}
</div>


## Polaroid Memories

<div class="gallery">
  {% assign polaroids = site.data.gallery | where: "category", "polaroid" %}
  {% for image in polaroids %}
    <div class="gallery-item">
      <img src="{{ image.src | relative_url | uri_escape}}" alt="{{ image.caption }}" class="gallery-image" loading="lazy" />
      <div class="gallery-caption">
        <div>{{ image.caption }}</div>
        <div class="caption-details">{{ image.camera }} · {{ image.date }}</div>
      </div>
    </div>
  {% endfor %}
</div>


<style>
  .gallery {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: 16px;
    padding: 16px;
  }
  .gallery-item {
    overflow: hidden;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #f5f5f5;
    position: relative;
  }
  .gallery-image {
    max-width: 100%;
    max-height: 100%;
    width: auto;
    height: auto;
    transition: transform 0.3s ease;
  }
  .gallery-image:hover {
    transform: scale(1.05);
  }
  .gallery-caption {
    text-align: center;
    padding: 8px;
    font-size: 14px;
    color: #333;
    background-color: rgba(255, 255, 255, 0.8);
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    opacity: 0;
    transition: opacity 0.3s ease;
  }
  .gallery-item:hover .gallery-caption {
    opacity: 1;
  }
  .caption-details {
    font-size: 12px;
    color: #666;
    margin-top: 4px;
  }

  /* event gallery styling */
  .event-gallery {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(400px, 1fr)); /* Larger images */
    gap: 16px;
    padding: 16px;
  }
  .event-gallery-item {
    overflow: hidden;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #f5f5f5;
    position: relative;
  }
  .event-gallery-image {
    max-width: 100%;
    max-height: 100%;
    width: auto;
    height: auto;
    transition: transform 0.3s ease;
  }
  .event-gallery-caption {
    text-align: center;
    padding: 8px;
    font-size: 14px;
    color: #333;
    background-color: rgba(255, 255, 255, 0.8);
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    opacity: 0;
    transition: opacity 0.3s ease;
  }
  .event-gallery-item:hover .gallery-caption {
    opacity: 1;
  }
  .event-gallery-image:hover {
    transform: scale(1.05);
  }
</style>