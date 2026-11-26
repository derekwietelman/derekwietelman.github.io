---
# Research page: working papers, then publications. Both lists come from the
# papers in `content/publications/`, sorted by their publication type.
title: Research
# Search-result and link-preview text for this page (not shown on the page).
description: "Working papers and peer-reviewed publications."
type: landing
# Keep it out of the theme's page list in the phone menu on paper pages.
sidebar:
  hidden: true

sections:
  - block: collection
    id: working-papers
    content:
      title: Working Papers
      filters:
        folders:
          - publications
        publication_type: article
      count: 0
    design:
      view: citation

  - block: collection
    id: publications
    content:
      title: Peer-Reviewed Publications
      filters:
        folders:
          - publications
        publication_type: article-journal
      count: 0
    design:
      view: citation
---
