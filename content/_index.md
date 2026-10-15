---
# Homepage. Each item under `sections` is one block on the page, shown in order.
title: ''
summary: ''
date: 2022-10-24
type: landing

sections:
  - block: resume-biography-3
    id: about
    content:
      # Profile details (name, role, interests, education, links) live in `data/authors/me.yaml`.
      username: me
      text: |-
        Welcome! I am a postdoctoral associate at the [Institute of Behavioral Science](https://ibs.colorado.edu) at the [University of Colorado Boulder](https://www.colorado.edu). In 2026, I received my Ph.D. from the [Department of Agricultural and Resource Economics](https://arec.umd.edu) at the [University of Maryland](https://umd.edu).

        I am an applied microeconomist specializing in environmental and resource economics, with a particular interest in the economics of water and energy resources. In my current work, I'm unpacking the economics of drought-induced water conservation mandates, investigating how lead pipe remediation efforts by water utilities impact health and behavioral outcomes, and designing cost-share subsidies for water quality improvements.
      button:
        text: Download CV
        url: /files/cv.pdf
      headings:
        about: Biography
        education: Education
        interests: Interests
    design:
      background:
        gradient_mesh:
          enable: true
      name:
        size: md
      avatar:
        size: medium
        shape: circle

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
      title: Publications
      filters:
        folders:
          - publications
        publication_type: article-journal
      count: 0
    design:
      view: citation

  - block: contact-info
    id: contact
    content:
      title: Contact
      visit_title: Office
      connect_title: Connect
      address:
        lines:
          - Jessor Building, 483 UCB
          - Boulder, CO 80309
          - United States
      email: derek.wietelman@colorado.edu
      social:
        - icon: academicons/google-scholar
          url: https://scholar.google.com/citations?user=4fMH-1cAAAAJ
        - icon: brands/github
          url: https://github.com/derekwietelman
      show_form: false
---
