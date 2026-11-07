# Media Assets

Use this directory for your portrait and one representative image, GIF, or video per publication.

| Purpose | File | Where it appears |
| --- | --- | --- |
| Personal portrait | `portrait.jpg` | Home, above profile links |
| Counter-UAV paper figure | `counter-uav.png` | Selected Work |
| Browser icon | `favicon.svg` | Browser tab |

## Portrait

Replace `portrait.jpg` with a new photo using the same filename, or update the portrait image's `src` in `index.html`. The display crop is controlled by `.portrait` in `styles.css`; the original file is preserved.

## Publication Image or GIF

Replace the media block in the corresponding publication article. Use a descriptive `alt` value. Preserve the link to the full-size image when the figure includes small text.

```html
<figure class="publication-media">
  <a href="media/project-overview.gif" target="_blank" rel="noopener noreferrer">
    <img src="media/project-overview.gif"
         alt="Describe the method or result shown in this animation."
         loading="lazy">
  </a>
  <figcaption>Project overview</figcaption>
</figure>
```

## Publication Video

Use a browser-compatible MP4 (H.264) and explicit controls. The same layout supports `<video>` without changing the CSS. A poster is optional.

```html
<figure class="publication-media">
  <video controls playsinline preload="metadata" aria-label="Project demonstration">
    <source src="media/project-demo.mp4" type="video/mp4">
    <a href="media/project-demo.mp4">Download the project video</a>
  </video>
  <figcaption>Project demonstration</figcaption>
</figure>
```

Keep filenames short and lowercase. Commit the media file and the matching HTML change together.
