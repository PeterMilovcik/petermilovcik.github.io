---
description: Add a new project card to the portfolio site
---

Add a new project to the Projects section in `index.html`.

## Input

- **Project name**: ${input:projectName}
- **Description**: ${input:description}
- **Link URL**: ${input:url}
- **Link text** (default "Try it"): ${input:linkText}

## Instructions

1. In `index.html`, locate the `<div class="projects">` container inside `<section id="projects">`.
2. Append a new `<div>` as the last child of the `.projects` container, using this structure:

```html
<div>
    <h3>{projectName}</h3>
    <p>{description}</p>
    <a href="{url}" target="_blank">{linkText}</a>
</div>
```

3. Use `target="_blank"` on the link.
4. Do not modify any other content.
