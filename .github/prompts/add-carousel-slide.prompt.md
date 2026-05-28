---
description: Add a new carousel slide for a conference or event
---

Add a new carousel slide to the header carousel in `index.html`.

## Input

- **Event title**: ${input:title}
- **Subtitle**: ${input:subtitle}
- **Description**: ${input:description}
- **Image filename** (placed in `images/`): ${input:imageFilename}
- **Video/link URL** (optional): ${input:videoUrl}
- **Link button text** (optional, default "Watch talk"): ${input:buttonText}

## Instructions

1. **Add the background image CSS rule** in the inline `<style>` block in the header.
   - Determine the next `nth-child` number (count existing `.carousel-item:nth-child(n)` rules).
   - Add a new rule:
     ```css
     .carousel-item:nth-child({n}) {
         background-image: url('images/{imageFilename}');
         background-repeat: no-repeat;
         background-size: cover;
         background-position: center center;
     }
     ```

2. **Add a carousel indicator** in the `.carousel-indicators` list.
   - Add `<li data-mdb-target="#introCarousel" data-mdb-slide-to="{index}"></li>` where `{index}` is 0-based.

3. **Add the carousel item** as the last `.carousel-item` inside `.carousel-inner` (before the controls `<a>` elements):
   ```html
   <div class="carousel-item">
       <div class="d-flex justify-content-center align-items-center h-100 blur">
           <div class="text-white text-center" data-mdb-theme="dark">
               <h1 class="container">{title}</h1>
               <h5 class="container">{subtitle}</h5>
               <div class="container">
                   <p>{description}</p>
                   <!-- Include button only if videoUrl is provided -->
                   <a data-mdb-ripple-init class="btn btn-outline-light btn-lg"
                       href="{videoUrl}" target="_blank"
                       role="button">{buttonText}</a>
               </div>
           </div>
       </div>
   </div>
   ```
   - Omit the `<a>` button entirely if no video/link URL is provided.

4. Do not modify any existing slides or other content.
