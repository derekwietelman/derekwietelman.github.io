---
# CV page: a link to the CV file (static/files/cv.pdf) and a photo. Photo:
# `![description](cv/file.jpg "Caption")` on its own line. Image files go in
# `assets/media/cv/`. The "Last updated" month fills itself in from the date
# the CV file was last committed (layouts/_shortcodes/cv-updated.html).
title: CV
type: landing
# Keep it out of the theme's page list in the phone menu on paper pages.
sidebar:
  hidden: true
# Photo width for the image hook: full width less the side padding on phones,
# 624px (39rem, set in custom.css) on larger screens.
image_sizes: "(max-width: 671px) calc(100vw - 48px), 624px"

sections:
  - block: markdown
    id: cv
    content:
      title: CV
      text: |-
        Download the current version of my CV [here](/files/cv.pdf). Last updated: {{< cv-updated >}}.

        ![The Rio Grande in early-morning light, with the Sandia Mountains beyond the trees on the far bank](cv/rio-grande.jpg "An early-morning stroll along the Rio Grande, with the Sandia Mountains in the distance.")
---
